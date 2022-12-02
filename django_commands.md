## Django Commands

```bash
# install pipenv
pip install pipenv
```

```bash
# create venv
pipenv shell
```

```bash
# install django
pipenv install django
```

```bash
# install python-decouple
pipenv install python-decouple
# create .env file and move SECRET_KEY
```

```bash
# create pollster project
django-admin startproject pollster
cd pollster
```

```bash
# run server
python manage.py runserver
```

```bash
# run initial migrations
python manage.py migrate
```

```bash
# create polls app
python manage.py startapp polls
```

create polls model

```bash
# create polls migrations
python manage.py makemigrations polls
```

```bash
# run migrations
python manage.py migrate
```

```bash
# using the python shell
python manage.py shell

>>>  from polls.models import Question, Choice
>>>  from django.utils import timezone
>>>  Question.objects.all()
>>>  q = Question(question_text="What is your favorite Python Framework?", pub_date=timezone.now())
>>>  q.save()
>>>  q.id
>>>  q.question_text
>>>  Question.objects.all()
>>>  Question.objects.filter(id=1)
>>>  Question.objects.get(pk=1)
>>>  q = Question.objects.get(pk=1)
>>>  q.choice_set.all()
>>>  q.choice_set.create(choice_text='Django', votes=0)
>>>  q.choice_set.create(choice_text='Flask', votes=0)
>>>  q.choice_set.create(choice_text='Flask', votes=0)
>>>  q.choice_set.all()
>>>  quit()
```

```bash
# create superuser
python manage.py createsuperuser
```

update polls admin for question and choice
update polls view with functions
create polls url
add path to pollster url
create global templates folder to store index.html
amend settings for global templates
create base.html
update index.html in polls template
create detail views and urls
create results views and urls
create detail and results templates in polls
create vote views and urls
create navbar partial

create pages app

set up zingcharts in results.html
create results_data views and urls
