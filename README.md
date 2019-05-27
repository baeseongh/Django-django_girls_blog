# Django-django_girls_blog


### 장고걸스 튜토리얼 : 심화 (Django Girls Tutorial: Extensions)
#### 숙제 : 안전한 웹사이트 만들기

- logi, logout 기능 구현 코드 수정 필요 

poject/urls.py
<pre>
path('account/login/', views.LoginView.as_view(template_name="registration/login.html"), name ='login'),

path('accounts/logout', views.LogoutView.as_view(template_name="/"), name='logout'),
</pre>

project/sttings.py
<pre>
LOGIN_REDIRECT_URL = '/'
LOGOUT_REDIRECT_URL = '/'
</pre>