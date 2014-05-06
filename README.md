XuetangX Server
===============

http://xuetangxserver.sinaapp.com/


**NOTE**: Remember to CHANGE POST TO GET after dev


Design
------

- xuetangx  => main

- ^student/ -- ^verify/$    POST email, password => true/false
            |- ^info/$      POST email, password => name, nickname

- ^courses/ -- ^selected$   POST email, password => all selected courses
            |- ^upcoming/$  POST email, password => upcoming courses
            |- ^current/$   POST email, password => current courses
            |- ^past/$      POST email, password => past courses
            |- ^search/$    POST category, started, hasTA => satisfied courses
            |- ^about/$     POST url => course introduction page
            |- ^info/$      POST email, password, url => course main page
            |- ^ware/$      POST email, password, url => courseware page

```
response header:
    'valid':
    - false => Request format error
    - true
      => 'error':
      + true  => Server error
      + false
        => 'authen':
        - fasle => Email/password error
        - true  => ...
```


APIs
----

### student

#### verify (atually, no extra field is needed)

    POST { 'email': str, 'password': str }
    => { 'student.verify': bool }

#### info

    POST { 'email': str, 'password': str }
    => { 'student.name': str, 'student.nickname': str }


### courses

#### selected

    POST { 'email': str, 'password': str }
    =>

#### upcoming

    POST { 'email': str, 'password': str }
    =>

#### current

    POST { 'email': str, 'password': str }
    =>

#### past

    POST { 'email': str, 'password': str }
    =>

#### search

    POST { 'email': str, 'password': str }
    =>

#### about

    POST { 'email': str, 'password': str }
    =>

#### info

    POST { 'email': str, 'password': str }
    =>

#### ware

    POST { 'email': str, 'password': str }
    =>

