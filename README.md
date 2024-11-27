
innowise_hackathon
______________________________________________________________________________________________

_______________________________________________________________________________________________
      сайт где размещена мобильная версия 
      
     i v a k h n e n k o v i t a l i .c o m


    https://www.ivakhnenkovitali.com/




_________________________________________________________________
[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&lines=Quantum+Coders+!)](https://git.io/typing-svg)  


 HappeningNow  "происходит сейчас"

![FireShot Capture 273 - Бутстрап - localhost](https://github.com/user-attachments/assets/9965e939-b42b-4d74-a19c-4cfb763aad66)




























________________________________________________________________________________



__________________________________________________________________

 текст
___________________________________________________________________


















[![Typing SVG](https://readme-typing-svg.herokuapp.com?color=%2336BCF7&lines=Код+!)](https://git.io/typing-svg)  и используемые техналогии________


HTML — основа веб-страницы. Он определяет структуру контента и компоненты:

<!DOCTYPE html> — указывает на используемую версию HTML5.
Теги <head> и <body>:
В <head> размещаются метаданные страницы, ссылки на стили и шрифты.
В <body> описывается содержимое страницы (текст, изображения, формы, видео).
2. CSS (Cascading Style Sheets)
CSS используется для оформления и стилизации веб-страницы:

Подключенные стили:
bootstrap.css, bootstrap-grid.css, bootstrap-reboot.css, bootstrap-utilities.css — библиотеки Bootstrap для базовой стилизации, сетки и утилит.
main.css — кастомные стили для индивидуального дизайна.
Внешние шрифты:
Подключение через Google Fonts: Open Sans и Raleway.
3. Bootstrap Framework
Bootstrap — это CSS/JS-фреймворк, упрощающий создание адаптивных интерфейсов:

Сетка (Grid system):
Использование классов container, row, col-md-*, что обеспечивает адаптивное поведение элементов на разных устройствах.
Компоненты:
Навигационная панель (navbar): включает лого, ссылки и кнопку-меню для мобильных устройств.
Кнопки (button): стилизованные элементы управления.
Таблицы (ratio): для встраивания видео с соблюдением пропорций.
4. JavaScript
JavaScript добавляет интерактивность и динамическое поведение:

Подключенные скрипты:
jquery-3.6.3.js — библиотека jQuery для упрощенной работы с DOM, AJAX и событиями.
bootstrap.js — скрипты Bootstrap, добавляющие функционал (например, выпадающие меню и модальные окна).
Пример: функционал кнопки навигации для мобильных устройств (navbar-toggler).
5. Шрифты и иконки
Использование Google Fonts для улучшения визуального стиля текста.
Иконки (например, изображение кнопки с облаком) используются для наглядности.
6. Медиа (Видео и изображения)
Видео:
Встроенный YouTube-плеер (через тег <iframe>).
Изображения:
Подключены через тег <img> с атрибутом class="img-fluid" для адаптивного масштабирования.
7. Формы
HTML-форма в разделе "Contact Us" позволяет пользователям вводить данные:

Поля для имени, email и сообщения.
Кнопка для отправки формы.
8. Адаптивность
Использование адаптивного дизайна через CSS-систему сеток и медиазапросы делает страницу удобной для просмотра на мобильных и настольных устройствах.










___________________________________________________________________________________
Кухня - все в одном месте
Кушайте с удовольствием, без лишних хлопот.

VIDEO-- Кухни-cafe

[https://www.youtube.com/watch?v=0ABftQLyHfs](https://www.youtube.com/watch?v=0ABftQLyHfs)




__________________________________________________________________________________________

код используемые технологии____кухня-кафе

____________________________________________________________

.nav-li.float-left{
   float: left;}

.nav-li a{
   display: block;                   
   text-align: center;               
   text-decoration: none;
   color: white;
   padding: 14px 16px;
}

.nav-li a:hover:not(.active){
   background-color: dimgray;}

.active {
   background-color: green;}


В JspConstant  пропиши констант menu.jsp
    public static final String INDEX_JSP = "/index.jsp";

Создадим стартовую страницу index.jsp и подключим на нее файл menu.jsp с помощью директивы jsp:include.

<%@ page import="by.itclass.constants.JspConstants" %>
<%@ page contentType="text/html;charset=UTF-8" language="java" %>
<html>
  <head>
    <title>Pizza_2211</title>
    <link rel="stylesheet" href="/css/styles.css">
  </head>
  <body>
    <jsp:include page="<%=JspConstants.MENU_JSP%>"/>
    <img class="default-image" src="<%=JspConstants.BACKGROUND_IMAGE%>">
   <h1 style="position:absolute; top:50%; width:100%; text-align:center;">
               The most tasty pizza!!!
    </h1>
  </body>
</html>

Добавим в файл JspConstants путь к картинке 

public static final String BACKGROUND_IMAGE = "/img/pizza-dinner.jpg";


Добавим стили для картинки

.default-image {    
	width: 100%;  
      opacity: 0.5;
}
Для картинок создадим отдельную директорию img и поместим туда бэкграунд картинку...

Также подключим файл menu.jsp и поместим картинку на страницы login.jsp  и  registration.jsp
Стр11 и 12

<jsp:include page="<%=JspConstants.MENU_JSP%>"/>
<img class="default-image" src="<%=JspConstants.BACKGROUND_IMAGE%>">

И чтобы не было зазоров по бокам добавим стиль для элемента body

body {
    margin: 0px;
}
Итак мы реализовали работу с пользователями, которая состоит из 3-х блоков – логин, регистрация и выход. 

Приступим к написанию непосредственно нашей пиццерии... 

Создадим таблицу, в которой будем хранить позиции меню нашей пиццерии

CREATE TABLE foodItem (
   id int NOT NULL AUTO_INCREMENT PRIMARY KEY,
   foodTypeId int NOT NULL,
   name varchar(50) NOT NULL,
   price double NOT NULL
);

INSERT INTO foodItem (foodTypeId, name, price) VALUES
   	(1, 'Margherita', 15.99), (1, 'Napoletana', 17.99),
   	(1, 'Carbonara', 25.99), (1, 'Peperoni', 25.99),
   	(2, 'Beer', 9.50), (2, 'Cola', 2.50),
   	(2, 'Tea', 3.50), (2, 'Coffee', 9.50);


Создадим таблицы, в которых будет храниться заказы и позиции из этого заказа

CREATE TABLE orders (
   id varchar(50) NOT NULL PRIMARY KEY,
   date date NOT NULL,
   userId int NOT NULL,
   address varchar(50) NOT NULL,   
   FOREIGN KEY (userId) REFERENCES user (id)
                    ON DELETE CASCADE ON UPDATE RESTRICT
);

CREATE TABLE orderItem (
   orderId varchar(50) NOT NULL,
   itemId int NOT NULL,
   quantity int NOT NULL,
   FOREIGN KEY (orderId) REFERENCES orders (id)
                    ON DELETE CASCADE ON UPDATE RESTRICT,
   FOREIGN KEY (itemId) REFERENCES foodItem (id)
                    ON DELETE CASCADE ON UPDATE RESTRICT            
);
По традиции начнем с модели, в пакете  model.entities создадим класс FoodItem

@AllArgsConstructor
@Data
@EqualsAndHashCode
public class FoodItem {
    private int id;
    private int type;
    private String name;
    private double price;
}

Дополним наше menu.jsp несколькими кнопками, которые будут показываться только авторизованному пользователю, нажав на которые он сможет посмотреть меню, предлагаемое пиццерией. (Pizza и Drinks)

<li class="nav-li float-left">
    <a href="<%=ApplicationConstants.PIZZAS_MENU%>">Pizza</a></li>
<li class="nav-li float-left">
    <a href="<%=ApplicationConstants.DRINKS_MENU%>">Drink</a></li>

И соответственно добавим в класс ApplicationConstants эти ссылки:

public static final String MENU_CONTROLLER = "/menu";
public static final String PIZZAS_MENU = "/menu?foodType=1";
public static final String DRINKS_MENU = "/menu?foodType=2";

Две последние ссылки сделаны так нарочно... нам нужно пнуть сервлет и передать всего одн параметр... этот параметр передаем не с помощью формы, а напрямую в URL.

Как и с пользователем начнем писать наш код начиная с уровня DAO

public class FoodDao {
    private static FoodDao dao;

    private FoodDao() {	ConnectionManager.init(); }

    public static FoodDao getInstance() {
        return Objects.isNull(dao) ? new FoodDao() : dao;
    }

    public List<FoodItem> getFoodItemsByType(int foodType) {
       var items = new ArrayList<FoodItem>();
       try (var cn = ConnectionManager.getConnection();
            var ps = cn.prepareStatement(SELECT_FOOD_ITEMS_BY_TYPE)){
          ps.setInt(1, foodType);
          var resultSet = ps.executeQuery();
          while (resultSet.next()) {
             var id = resultSet.getInt(ID_COL);
             var name = resultSet.getString(NAME_COL);
             var price = resultSet.getDouble(PRICE_COL);
             items.add(new FoodItem(id, foodType, name, price));
          }
       } catch (SQLException e) { 
          e.printStackTrace();
       }
       return items;
    }
}
Дополним файл DbConstants

psfs PRICE_COL = "price";
psfs SELECT_FOOD_ITEMS_BY_TYPE = "SELECT id, name, price FROM foodItem 
                                  WHERE foodTypeId = ?";
Соответственно service для сервлета:

public class FoodService {
   private static FoodService service;
   private FoodDao dao;

   private FoodService() { dao = FoodDao.getInstance(); }
 
   public static FoodService getInstance() {
      return Objects.isNull(service) ? new FoodService() : service;
   }
    
   public List<FoodItem> getFoodItemsByType(int foodType) {
      return dao.getFoodItemsByType(foodType);
   }
}

И когда вся логика по извлечению написана, приступим к сервлету, который нам будет доставать из базы данных айтемы, в зависимости от их типа. В пакете controllers.food создадим класс MenuController...

Инициализацию сервиса также вынесем в абстракный сервлет

@WebServlet(value = MENU_CONTROLLER)
public class MenuController extends AbstractController {
  @Override
  protected void doPost(HttpServletRequest req, HttpServletResponse
                         resp) throws ServletException, IOException {
    var foodType = Integer.parseInt(req.getParameter(FOOD_TYPE_PARAM));
    var items = foodService.getFoodItemsByType(foodType);
    enrichRequest(req, foodType, items);
    forward(req, resp, HOME_JSP);
  }

  private void enrichRequest(HttpServletRequest req, int foodType, 
                             List<FoodItem> items) {
    switch (foodType) {
      case 1 -> req.setAttribute(PIZZA_ATTR, items);
      case 2 -> req.setAttribute(DRINK_ATTR, items);
    }
  }
}
Дополним класс JspConstants новыми константами

public static final String FOOD_TYPE_PARAM = "foodType";
public static final String PIZZA_ATTR = "pizzas";
public static final String DRINK_ATTR = "drinks";

Я выбрал для получения меню способ запроса, вместо хранения его в сессии... мне показалось это более логичным. 
Поскольку мы хотим давать возможность просматривать меню только авторизованным пользователям то сервлет форвардит наш запрос на home страничку. 
Напишем же код, который покажет полученные данные. Не забываем, что файл home.jsp у нас уже создан... просто поменяем его содержимое

<body>
 <jsp:include page="<%=JspConstants.MENU_JSP%>"/>
 <h2>Hello ${user.name}</h2>
 <h1>Some content can be placed here... i.e. slider...<h2>
 <c:if test="${not empty pizzas}">
   <h2>Today we propose next pizzas:</h2>
   <c:forEach var="pizza" items="${pizzas}">
     <div class="food-item-box">
       <img class="small-image" src="/img/${pizza.name}.jpg" alt="pizza">
       <p>Name: ${pizza.name}</p>
       <p>Price: ${pizza.price} byn.</p>
     </div>
   </c:forEach>
 </c:if>
 <c:if test="${not empty drinks}">
   <h2>Today we propose next drinks:</h2>
   <c:forEach var="drink" items="${drinks}">
     <div class="food-item-box">
       <img class="small-image" src="/img/${drink.name}.jpg" alt="drink">
       <p>Name: ${drink.name}</p>
       <p>Price: ${drink.price} byn.</p>
     </div>
   </c:forEach>
 </c:if>
</body>

Добавим прекрасных стилей, для более-менее красивого показа

.food-item-box {  
   background-color: lightgray;      width: 200px;
   height: 251px;                    border: 3px solid green;
   padding: 15px;                    margin: 25px;
   display: inline-block;            vertical-align: top; }

.small-image {  width: 200px; }


Конечно, показать меню – это достижение... но было бы прикольно и добавить чего-нить в корзину... 
Чтобы нам было чего добавлять – напишем класс OrderItem в пакете model.entities. Данный класс будет хранить соответствие определенному заказу некоторого пункта меню, а также количество заказанных продуктов 

@Data
@EqualsAndHashCode
@RequiredArgsConstructor
public class OrderItem {
    private String orderId;
    private final FoodItem item;
    private final int quantity;
}

Возможность заказать продукт организуем в виде форм, которые поместим на нашу home.jsp страницу в каждый айтем меню. 
Для пиццы 

<form method="post" action="<%=ApplicationConstants.CART_CONTROLLER%>">
  <input type="hidden" name="<%= JspConstants.CARD_ACTION_PARAM%>" 
  	value="addToCard">
  <input type="hidden" name="<%= JspConstants.FOOD_ID_PARAM%>"
     value="${pizza.id}">
  <input type="hidden" name="<%=JspConstants.FOOD_TYPE_PARAM%>" value="1">
  <input type="hidden" name="<%= JspConstants.FOOD_NAME_PARAM%>" 
     value="${pizza.name}">
  <input type="hidden" name="<%= JspConstants.FOOD_PRICE_PARAM%>"
     value="${pizza.price}">
  <input type="number" name="<%=JspConstants.FOOD_QUANTITY_PARAM%>" 
     required>
  <input type="submit" value="Add to Cart">
</form>

Для напитков 

<form method="post" action="<%=ApplicationConstants.CART_CONTROLLER%>">
  <input type="hidden" name="<%= JspConstants.CARD_ACTION_PARAM%>" 
  	value="addToCard">
  <input type="hidden" name="<%= JspConstants.FOOD_ID_PARAM%>"
     value="${drink.id}">
  <input type="hidden" name="<%=JspConstants.FOOD_TYPE_PARAM%>" value="2">
  <input type="hidden" name="<%= JspConstants.FOOD_NAME_PARAM%>" 
     value="${drink.name}">
  <input type="hidden" name="<%= JspConstants.FOOD_PRICE_PARAM%>"
     value="${drink.price}">
  <input type="number" name="<%=JspConstants.FOOD_QUANTITY_PARAM%>" 
     required>
  <input type="submit" value="Add to Cart">
</form>

Стили для форм
input[type=number] {
   width: 45px;                      padding: 5px; }

.food-item-box input[type=submit] {
   width: 100px;                     height: 30px;
   background-color: green;          border: none;
   color: white;                     padding: 5px;
   text-decoration: none;            margin-left: 35px;
   cursor: pointer; }

Данныя форма будет отправлять на сервлет сведения о заказанном продукте и его количестве, таким образом формируя корзину заказа. 

Поместим в класс ApplicationConstants адрес нового контроллера

public static final String CART_CONTROLLER = "/cart";

Дополним класс JspConstants новыми константами

public static final String FOOD_ID_PARAM = "id";
public static final String FOOD_NAME_PARAM = "name";
public static final String FOOD_PRICE_PARAM = "price";
public static final String FOOD_QUANTITY_PARAM = "quantity";
public static final String CARD_ACTION_PARAM = "cardAction";   
public static final String ORDER_ITEMS_ATTR = "orderItems";

Вновь сначала напишем сервис и по привычке инициализируем его в абстрактном контроллере 

public class CartService {
   private static CartService service;

   public static CartService getInstance() {
      return service == null ? new CartService() : service; }

   public List<OrderItem> processCard(HttpSession session, 
                                    String cardAction, OrderItem item){
      Object orderItems = session.getAttribute(ORDER_ITEMS_ATTR);
      List<OrderItem> items = !Objects.isNull(orderItems)
          ? (List<OrderItem>) orderItems
          : new ArrayList<>();
      switch (cardAction) {
         case "addToCard" -> items.add(item);
         case "removeFromCart" -> items.remove(item);
      }
      return items;
   }
}
Поскольку айтемы хранятся в сесии и обращения к внешней БД нету, то не нужно ДАО. 
А вот и сам сервлет, его кстати напишем в пакете controllers/order

@WebServlet(value = CART_CONTROLLER)
public class CartController extends AbstractController {
  @Override
  protected void doPost(HttpServletRequest req, HttpServletResponse resp){
    var id = Integer.parseInt(req.getParameter(FOOD_ID_PARAM));
    var foodType = Integer.parseInt(req.getParameter(FOOD_TYPE_PARAM));
    var foodName = req.getParameter(FOOD_NAME_PARAM);
    var foodPrice= Double.parseDouble(req.getParameter(FOOD_PRICE_PARAM));
    var foodQuant=Integer.parseInt(req.getParameter(FOOD_QUANTITY_PARAM));
    var cardAction = req.getParameter(CARD_ACTION_PARAM);
    var item = new OrderItem(
              new FoodItem(id, foodType, foodName, foodPrice), foodQuant);
    var session = req.getSession();
    var items = cartService.processCard(session, cardAction, item);
    session.setAttribute(ORDER_ITEMS_ATTR, items);
    if ("addToCard".equals(cardAction)) {
       redirectToMenuPage(resp, foodType);
    } else {
       redirect(resp, CART_JSP);
    }
  }
  private void redirectToMenuPage(HttpServletResponse resp, int foodType){
    switch (foodType) {
      case 1 -> redirect(resp, PIZZAS_MENU);
      case 2 -> redirect(resp, DRINKS_MENU);
    }
  }
}

Дополним наше меню  menu.jsp
<li class="nav-li">
       <a href="<%=JspConstants.CART_JSP%>">Cart</a></li>

Файл констант (JspConstants)
public static final String CART_JSP = "/jsp/cart.jsp";

И приступим к написанию странички, на которой мы сможем видеть нашу корзину и иметь возможность удалить из корзины айтемы (для упрощения я не обращал внимания на количество можете сами сделать), тем более мы ее только что объявили в константах.

<body>
  <jsp:include page="<%=JspConstants.MENU_JSP %>"/>
  <h2>Hello ${user.name}</h2>
  <c:choose>
    <c:when test="${not empty orderItems}">
      <h2>Yours order items: </h2>
      <c:forEach var="item" items="${orderItems}">
        <div class="cart-item-container">
          <img class="cart-img" src="/img/${item.item.name}.jpg">
          <h3 class="cart-text">You ordered ${item.quantity} 
               ${item.item.name} by ${item.item.price} byn. Amount is
               ${item.quantity * item.item.price}</h3>
<form method="post" action="<%=ApplicationConstants.CART_CONTROLLER%>">
   <input type="hidden" name="<%= JspConstants.CARD_ACTION_PARAM %>" 
        value="removeFromCart">
   <input type="hidden" name="<%= JspConstants.FOOD_ID_PARAM %>" 
        value="${item.item.id}">
   <input type="hidden" name="<%= JspConstants.FOOD_TYPE_PARAM %>" 
        value="${item.item.type}">
   <input type="hidden" name="<%= JspConstants.FOOD_NAME_PARAM %>" 
        value="${item.item.name}">
   <input type="hidden" name="<%= JspConstants.FOOD_PRICE_PARAM %>" 
        value="${item.item.price}">
   <input type="hidden" name="<%= JspConstants.FOOD_QUANTITY_PARAM %>" 
        value="${item.quantity}">
   <input type="submit" value="Remove from Cart">
</form>
        </div>
      </c:forEach>
      Сюда добавить order – чутка дальше будет
    </c:when>
    <c:otherwise>
      <p>You have no items in the order</p>
    </c:otherwise>
  </c:choose>
</body>
Стили:

.cart-item-container {
   height: 80px; }

.cart-img {   
   height: 60px;                     float: left;
   border: 1px solid black;          margin: 5px 50px 10px 0px; }

.cart-text {
   margin: 0 0 10px; }

.cart-item-container input[type=submit] {
   width: 140px;                     height: 35px;
   background-color: green;          border: none;
   color: white;                     padding: 10px 10px;
   text-decoration: none;            margin: 0px 3px;
   cursor: pointer; }

Все действия по добавлению и удалению позиций корзины пока происходят в сессии, созданной для пользователя...  на странице корзины мы также сделаем возможность сабмитнуть наш заказ, предварительно введя адрес доставки – обратим внимание, что это поле сделано реквайред. 
                          


________________________________________________________________

[https://github.com/ivakhnenkovitali/final_project_2211](https://github.com/ivakhnenkovitali/final_project_2211)
















