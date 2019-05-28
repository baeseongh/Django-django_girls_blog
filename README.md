# Django-django_girls_blog


### 장고걸스 튜토리얼 : 심화 (Django Girls Tutorial: Extensions)
#### 숙제 : 안전한 웹사이트 만들기

- login, logout 기능 구현시 아래와 코드 수정 필요
    - 장고 버전에 따른 상이함 존재 (최신 버전 장고에서는 아래와 같이 진행 합니다.) 

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

#### 숙제 : 댓글 모델 만들기

- Comment 모델 구현시 아래와 같이 코드 수정 필요

app/models.py
<pre>
class Comment(models.Model):
    post = models.ForeignKey('blog.Post', related_name='comments', on_delete=models.CASCADE) 
</pre>

#### 옵션의 내용은 진행하지 않았음.

#### 변동사항
- 본인 댓글의 수정이 가능하게 함.
- 댓글에 작성자 이름이 들어가게 함.

#### 차후 수정해야할 것
- 댓글 작성 및 수정을 detail 페이지에서 할 수 있도록
- 회원가입 기능 구현
