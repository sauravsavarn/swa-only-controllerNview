# Read Me First
This example shows Spring's Handling of Web Request

Spring comes with a powerful web framework known as Spring MVC. At the center of Spring MVC is the concept of a controller, a class that handles requests and responds with information of some sort. <u>In the case of a browser-facing application, a controller responds by optionally populating model data and passing the request on to a view to produce HTML that’s returned to the browser</u>.

##### NOTE

* This class is annotated with @Controller. On its own, @Controller doesn’t do much. Its primary purpose is to identify this class as a component for com- ponent scanning. Because HomeController is annotated with @Controller, Spring’s component scanning automatically discovers it and creates an instance of Home- Controller as a bean in the Spring application context.
* The home() method is as simple as controller methods come. It’s annotated with @GetMapping to indicate that if an HTTP GET request is received for the root path /, then this method should handle that request. It does so by doing nothing more than returning a String value of home.
* This value is interpreted as the logical name of a view. How that view is imple- mented depends on a few factors, but because Thymeleaf is in your classpath, you can define that template with Thymeleaf.


### How Thymeleaf Template is picked by ViewResolver

The template name is derived from the logical view name by prefixing it with /templates/ and postfixing it with .html. The resulting path for the template is /templates/home.html. Therefore, you’ll need to place the template in your project at /src/main/resources/templates/home.html.

