# Projeto Fusion 
****Projeto ficcional onde, a partir de um template bootstrap, implemento alguns experimentos com práticas do framework py Django.****

<hr>Aqui, separados por seções do site, explicarei, de forma superficial, o uso do Django nelas.

- Base:
  - O template base.html carrega dentro dele todas as Metatags e importações de arquivos estáticos. O arquivo index irá extender esse arquivo. 

- Index(*urls.py, views.py, models.py*):
  - Como o site possui apenas uma página, separei as seções em arquivos separados e os incluí no index com o comando {% include 'hero.html' %}, por questão de organização e facilidade na manutenção.

- Serviços, Recursos e Equipe(*views.py*):
  - Estas seções estão ligadas ao banco de dados (PostgreSQL) pois, no painel administrativo do Django, poderemos adicionar itens, que serão  adicionados ao grid automáticamente, somente fazendo a iteração no template html utilizando o código abaixo.
  ```python
  {% for item in itens %}
    <div>{{ item.propriedade }}</div>
  {% endfor %}
  ```
- Contato(*forms.py , views.py, settings.py*):
  -	Encarreguei a classe EmailMessage, do pacote django.core.mail.message, para fazer o trabalho pesado. :smile:

- Considerações finais sobre o projeto:
  - Estou gostando bastante de aprender mais sobre o framework e busco a cada dia melhorar com ele. 
  - Me desafiei a utilizar a view baseada em Class, ao invés de funções, e foi um caminho sem volta. A partir de agora, sempre farei dessa forma :smile:
  - Este lindo template foi baixado [UIDeck](http://uideck.com "UIDeck")
