#Spring Web MVC Framework
##MVC Architecture
The Model-View-Controller (MVC) architecture is an architectural pattern that divides an application into three different logical components. Each component handles specific development aspects of an application. It is an industry-standard web development framework used for creating scalable and extensible projects.

###MVC Components
![MVC Components](https://www.tutorialspoint.com/mvc_framework/images/model_view_controller.jpg)
**Model**: It corresponds to all the data-related logic that the user works with. It is connected to the database. It responds to controller requests and provides the needed data to the controller.
**View**: It is used for the UI logic of an application. It generates HTML output that the user's browser can interpret. The views are created by the data collected from the model component through the controller.
**Controller**: It contains the business logic of an application. It acts as an interface between Model and View components. It tells the model what needs to be done. It processes the data received from the model and sends it to view and explains how to represent it to the user.

##Spring MVC Framework
A spring MVC is a Java framework that is used to build web applications. The framework is designed around a DispatcherServlet which handles all the HTTP requests and responses. DispatcherServlet is a class that receives the incoming request and maps it to the right resources such as controllers, models, and views.

###Understanding flow of Spring Web MVC
![Workflow of Spring Web MVC *DispatchServlet*]
The incoming HTTP request is intercepted by the *DispatcherServlet*.
*DispatcherServlet* consults the HandleMapping to call the appropriate *Controller*.
The *Controller* takes the request and calls the appropriate service methods based GET or POST method. The service method will set model data based on defined business logic and returns the view name to the *DispatcherServlet*.
The *DispatcherServlet* checks the entry of *ViewResolver* in the XML file and invokes the specified view.
Once the view is finalized, the *DispatcherServlet* passes the model data to the view which is finally rendered on the browser.

> The components HandlerMapping, Controller, and ViewResolver are parts of WebApplicationContext which is an extension of the plainApplicationContext with some extra features necessary for web applications.

###Advantages of Spring MVC Framework
*1. Separate roles* - It separates each role, where the model object, controller, ViewResolver, command object, DspatcherServlet, etc. can be fulfilled by a specialized object.
*2. Light-weight* - It uses a lightweight servelet container to develop and deploy your application.
*3. Powerful Configuration* - It provides a robust configuration for both framework and application classes that includes easy referencing across contexts, such as from web controllers to business objects and validators.
*4. Rapid development* - The Spring MVC facilitates fast and parallel development.
*5. Reusable business code* - It allows us to use the existing business objects.
*6. Easy to test* - In Spring, generally we create JavaBeans classes that enable you to inject test data using the setter methods.
*7. Flexible Mapping* - It provides the specific mapping that easily redirects the page.

###Steps for creating a project in Spring MVC
*Step 1*. Provide project information and configuration in the pom.xml file
*Step 2*. Create a controller class
To create a controller class we use two annotations:
	@Controller annotation marks this class as a controller
	@Requestmapping annotation is used to map the class with a specified URL
*Step 3*. Provide the entry of controller in the web.xml file
*Step 4*. Define the bean in xml file present in the WEB-INF directory
*Step 5*. Display the message returned by the controller in JSP Page
*Step 6*. Start the server and deploy the project

##Refrences
[https://www.tutorialspoint.com/spring/spring_web_mvc_framework.htm](https://www.tutorialspoint.com/spring/spring_web_mvc_framework.htm)
[https://www.javatpoint.com/spring-mvc-tutorial](https://www.javatpoint.com/spring-mvc-tutorial)
[https://www.tutorialspoint.com/mvc_framework/mvc_framework_introduction.htm](https://www.tutorialspoint.com/mvc_framework/mvc_framework_introduction.htm)
