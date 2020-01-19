Instrukcja: 
  ====================================================  
1. Wejdź w wierszu poleceń w lokalizację folderu "forum", gdzie znajduje się plik manage.py
2. Uruchom serwer poleceniem "python manage.py runserver"
3. Można się zalogować oraz zarejestrować
4. Zakładka "About" jest tylko dla zalogowanych użytkowników
5. W zakładce "Home" widzimy posty, które można dodać przez shella (nie zdążyłem zrobić dodawanie postów na stronie)
a)Polecenie "python manage.py shell", będąc w folderze "forum"
b)wklejamy poniższy kod zmieniając "title" oraz "content". Można zmienić też username po zarejestrowaniu użytkownika na stronie

from blog.models import Post
from django.contrib.auth.models import User
me = User.objects.get(username='daniel')
Post.objects.create(author=me, title='Nowy tytul', content='Nowy Kontent')

c)Polecenie "exit()"
d)Polecenie "python manage.py runserver"
