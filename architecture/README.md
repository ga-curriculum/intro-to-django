# ![Intro to Django - Architecture](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

## Django's MVT architecture

Django adopts the Model-View-Template (MVT) architecture, a variant of the more widely known Model-View-Controller (MVC) architecture. While both architectures aim to separate concerns within an application, Django's MVT architecture has distinct roles for each component.

![Infographic of Django's MVT architecture design pattern](./assets/mvt.png)

- **Model:** Defines the data structure. These are Python classes that define the fields and behaviors of the data you’re storing. Django models can interact with a database seamlessly to retrieve, store, update, and delete data.

- **View:** Handles the business logic and is the bridge between models and templates. In Django, views retrieve data from the models and pass it to the templates. Views in Django perform roles similar to controllers in MVC, essentially directing traffic within the application.

- **Template:** Manages the presentation layer. Templates are HTML files which allow Python-like expressions for dynamic content generation. This separation from the actual business logic in views allows for cleaner, more maintainable code.

## MVC vs Django's MVT

| Concern                   | MVC        | Django MVT |
| ------------------------- | ---------- | ---------- |
| Database access           | Model      | Model      |
| Code mapped to routes     | Controller | View       |
| Rendering of dynamic HTML | View       | Template   |

### Practical Implications

When developing with Django, it's essential to adjust the terminology you use:

- `View` in Django corresponds to what is often called `Controller` in other MVC frameworks.
- `Template` in Django serves the function of the `View` component in MVC frameworks.

When developing with Django, we’ll just have to be careful to say **view** instead of **controller**, and **template** instead of **view**.

## Components of a Django Project

This diagram illustrates how different components interact within a Django project:

![Infographic of Django's MVT architecture design pattern](./assets/mvt.png)

### Terminology in Django

Django uses unique terminology for its components, which can initially be confusing:

- **Project**: In Django, what you might typically think of as a "web application" is referred to as a "project." This is the top-level container for your web application that houses the configuration and ties everything together.

- **Apps**: What are often considered as features or modules in other frameworks are called "apps" in Django. An app is a web application that does something – e.g., a blog, a database of public records, or a simple poll app. A project can contain multiple apps, and apps can be reusable in different projects.

A Django _project_ is a complete web site of multiple pages, while a Django _app_ is a web application that does something specific and can be plugged into any project.

### Understanding Django's Project and App Structure

| **Component** | **Description**                                                                                                                    |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Project**   | A full Django project is essentially a complete website containing configurations and applications that make the website function. |
| **Apps**      | Each app is a self-contained package that encapsulates specific functionality or features of a website.                            |

This modular approach makes it possible for Django apps to be highly reusable, migrating easily from one project to another or being maintained across multiple projects.

A Django _project_ can have many _apps_, and a Django _app_ can belong to multiple _projects_.

## Django's Routing Methodology

Routing is a core aspect of web development, as it determines how a web application responds to a client's request to a particular endpoint, which is a URL path in the web application.

### Comparison with Other Frameworks

Frameworks like Express and Ruby on Rails use both HTTP methods (GET, POST, etc.) and URL paths to define routes, allowing for different responses based on the method used. 

Conversely, Django and ASP.NET Core primarily use the URL path to define routes, omitting the HTTP method. This method simplifies routing but may require additional setup to handle multiple HTTP methods for the same URL path effectively.

### Django's Routing Files

Django's routing is managed through a module named **`urls.py`**, found in each app and sometimes at the project level. This module defines the URL patterns (routes) that direct web requests to the correct view functions based on the URL, organizing the routing process across the application.

