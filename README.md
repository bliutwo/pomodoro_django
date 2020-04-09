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

- [x] Find out why my web page isn't showing up

It looks like I need to ~~create a `urls.py` (or use the existing one) to~~...

Let's keep it simple here. I need to modify `views.py` and `urls.py`. Let's find out from the official tutorial how that's going to work.

- [x] Check the official Django tutorial for `urls.py` and `views.py`.

OK, so [according to this](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#write-your-first-view) I only ran `django-admin startproject pomodoro`, which creates the "project." This is the first step to creating the app. Next, I need to actually run the command that creates the app:

```bash
$ python manage.py startapp app
```

I named it "app" because it's too confusing to have multiple `pomodoro` folders.

- [x] Get a [working index page](http://127.0.0.1:8001/app/).
- [x] Import Pomodoro class into `models.py`

I was looking at [this section](https://docs.djangoproject.com/en/3.0/intro/tutorial02/) of the guide and it wasn't working as intended, specifically the step that requires this command:

```bash
$ python manage.py makemigrations polls
```

- [x] Fix problem described above (makemigrations not working)

Apparently in my `app/models.py` I didn't create my `Pomodoro` class based off of the `models.Model` class. Doing so fixed that problem. The next thing I need to do is to find out how to display my front-end:

- [x] Find out from guide or django-glicko how to display front-end

The way to display my front end was to create a folder in app called `templates/app` and then make an `index.html` file in there.

- [ ] Actually make two front-end pages, one for getting input, one for displaying things after input is gotten.

Maybe I don't need to make a Django page for this? Can I do this just using HTML/CSS/Javascript?

- [ ] Find out if I need business logic from `custom_pomodoro.py`.
- [ ] Front end
- [ ] Back end
- [ ] Put it on a Heroku app.
