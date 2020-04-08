# Webapp Version of Pomodoro App

I have a [Python script](https://github.com/bliutwo/pomodoro/) version of the app, but it's not easy to install and therefore not accessible for most users. 

Moreover, I want to be able to full screen applications while running this app for my personal use in a cross-platform manner.

## TODO:

The main goal is to get a working version of this app.

- [x] Import base `Pomodoro.py` class
- [x] Find out from [Glicko-django](https://github.com/bliutwo/django-glicko2) what I need for a working website.
- [x] Where do I put the front-end stuff?

That stuff in `django-glicko2` went into `templates/glicko` but I'm not sure if that's the proper structure we need. **Maybe check the tutorial?**

- [x] Check the official Django tutorial for front-end stuff.
      
According to [this page](https://docs.djangoproject.com/en/3.0/intro/reusable-apps/#reusability-matters), the structure of the `polls` app looks like this:

```
mysite/
    manage.py
    polls/
        models.py
        templates/
            polls/
                index.html 
```

Because of that, I'll be wanting to create a directory in `pomodoro` called `templates`, and then a directory inside `templates` called `pomodoro`.

- [x] Create a directory in `pomodoro` called `templates`, and then a directory inside `templates` called `pomodoro`.

Why isn't my web page showing up? I'm still getting the default "yay, you successfully installed and ran your page."

- [ ] Find out why my web page isn't showing up

- [ ] Find out if I need business logic from `custom_pomodoro.py`.
- [ ] Front end
- [ ] Back end
- [ ] Put it on a Heroku app.
