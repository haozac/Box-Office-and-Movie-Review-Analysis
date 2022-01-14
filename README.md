<h1 align='center'>Box Office and Movie Review Analysis</h1>

## Introduction 
This is an Assignment from Forward School: **Box Office and Movie Review Analysis from Worldwide**

This repository is a project to carry out the analysis of box office from the worldwide and then, lead to the analysis of movie review to investigate why the movie is favourable by many people and achieve the highest box office of all time. The results of this analysis will be showcased in a Django dashboard. There are 2 contrinutors for this repository: Zac and Jason from ADS 2021 Dec Cohurt. 

This project cover 2 parts, which is Web Scrapping and Deployment Data Visualisation into Django

## Web Scrapping 
Data scrapping is done by using selenium and Beautiful Soup via Jupyter Notebook. The data for this project are originated from **The Numbers: Where Data and the Movie Business Meet** (box office data) and **IMDB** (movie reviews data)
    - For the box office analysis, 100 datas from **[The-Number](https://www.the-numbers.com/movie/budgets/all)** website was scrapped and analysed by Jason.
    - For the movie reviews analysis, 3000 reviews from **[IMDB](https://www.imdb.com/title/tt0499549/reviews?ref_=tt_urv)** website was scrapped and analysed by Zac.

After scrapping all the data, we save all the results into csv file and all the graphs are later showcased inside the Django website. 
    
## Deployment Data into Django
![ alt text ](\Picture for ReadMe.jpg "Dashboard")

In order to showcase our result in Django, an open-source **[Django Dashboard](https://appseed.us/admin-dashboards/django)** generated by AppSeed is used , with several feature like register and login function. This dashboard is ready-for-used to help us create a stunning dashboard to showcase our results. 

Here is how to start the entire dashboard from your side.

### ✨ Quick Start in `Anaconda`

> Get the code

```bash
$ git clone https://github.com/haozac/Box-Office-and-Movie-Review-Analysis
```

> Create new environment in Anaconda

```bash
$ Go to Environments
$ click **Create** button and select your latest python version
$ click the **Play** button and select **Open Terminal**
```

### ✨ How to use it

```bash
$ # Get the code
$ git clone https://github.com/haozac/Box-Office-and-Movie-Review-Analysis
$ cd Assignment Django
$ cd dashboard
$
$ # Install modules - SQLite Storage
$ pip3 install -r requirements.txt
$
$ # Create tables
$ python manage.py makemigrations
$ python manage.py migrate
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
$
$ # Start the app - custom port
$ # python manage.py runserver 0.0.0.0:<your_port>
$
$ # Access the web app in browser: http://127.0.0.1:8000/
```

> Note: To use the app, please access the registration page and create a new user. After authentication, the app will unlock the private pages.

### ✨ Code-base structure

The project is coded using a simple and intuitive structure presented bellow:

```bash
< PROJECT ROOT >
|
|-- core/                               # Implements app configuration
|    |-- settings.py                    # Defines Global Settings
|    |-- wsgi.py                        # Start the app in production
|    |-- urls.py                        # Define URLs served by all apps/nodes
|
|-- apps/
|    |
|    |-- home/                          # A simple app that serve HTML files
|    |    |-- views.py                  # Serve HTML pages for authenticated users
|    |    |-- urls.py                   # Define some super simple routes  
|    |
|    |-- authentication/                # Handles auth routes (login and register)
|    |    |-- urls.py                   # Define authentication routes  
|    |    |-- views.py                  # Handles login and registration  
|    |    |-- forms.py                  # Define auth forms (login and register) 
|    |
|    |-- static/
|    |    |-- <css, JS, images>         # CSS files, Javascripts files
|    |
|    |-- templates/                     # Templates used to render pages
|         |-- includes/                 # HTML chunks and components
|         |    |-- navigation.html      # Top menu component
|         |    |-- sidebar.html         # Sidebar component
|         |    |-- footer.html          # App Footer
|         |    |-- scripts.html         # Scripts common to all pages
|         |
|         |-- layouts/                   # Master pages
|         |    |-- base-fullscreen.html  # Used by Authentication pages
|         |    |-- base.html             # Used by common pages
|         |
|         |-- accounts/                  # Authentication pages
|         |    |-- login.html            # Login page
|         |    |-- register.html         # Register page
|         |
|         |-- home/                      # UI Kit Pages
|              |-- index.html            # Index page
|              |-- 404-page.html         # 404 page
|              |-- *.html                # All other pages
|
|-- requirements.txt                     # Development modules - SQLite storage
|
|-- .env                                 # Inject Configuration via Environment
|-- manage.py                            # Start the app - Django default start script
|
|-- ************************************************************************
```

> The bootstrap flow

- Django bootstrapper `manage.py` uses `core/settings.py` as the main configuration file
- `core/settings.py` loads the app magic from `.env` file
- Redirect the guest users to Login page
- Unlock the pages served by *app* node for authenticated users

Hope you enjoy the repository. Thanks! 