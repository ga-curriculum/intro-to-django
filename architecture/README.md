# ![Intro to Django - Architecture](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

### Django's MVT architecture

Django uses Model-View-Template (MVT) architecture, which is similar to Model-View-Controller (MVC) architecture, but with some key differences. 

![Infographic of Django's MVT architecture design pattern](./assets/originals/ERD@2x(11).png)

#### MVC vs Django's MVT

| Concern | MVC | Django MVT |
|---|---|---|
| Database access | Model | Model |
| Code mapped to routes | Controller | View |
| Rendering of dynamic HTML | View | Template |


When developing with Django, we’ll just have to be careful to say:

- **view** instead of **controller**, and
- **template** instead of **view**


### Components of a Django project

This diagram visualizes the relationship between the different components of a Django project:

![Infographic of Django's MVT architecture design pattern](./assets/originals/ERD@2x(11).png)

One quirky thing about Django is how it names its high-level components - what we think of as a web **application**, Django calls a **project**.

Further, what we think of as part of an app’s functionality, or **modules**, Django refers to as **apps**.

A Django *project* can have many *apps*, and a Django *app* can belong to multiple *projects*. More on this later.


### Django's routing methodology

Because routing is so fundamental to developing web apps, it’s worthwhile knowing in advance an important difference between Express and Django’s routing methodology.

Web frameworks such as Express and Ruby on Rails, use both the HTTP verb & URL to define routes used to map requests to controller actions.

Other frameworks, such as Django and ASP.NET Core, use just the URL when defining a route, ignoring the HTTP verb.

That’s why the Python modules used to define routes in Django are named **`urls.py`** (see diagram above).