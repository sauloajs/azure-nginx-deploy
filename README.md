# Configurações 
###WEBSITES_ENABLE_APP_SERVICE_STORAGE=true
- Alterar essa configuração dentro das variáveis de ambiente, ela permite que arquivos dentro do diretório /home sejam consistidos num storage para o App Service, conseguindo permanecer mesmo caso a máquina seja reiniciada/escalada.

###Versão do PHP 8.2
- As depêndencias serão instaladas nessa versão do php, para alterar a versão nos comando de build da pipeline (CI).

###Criar aquivo /home/default com as configurações para sobrescrever o padrão do Nginx
- No arquivo devem estar contidas todas as regras para redirecionamento da aplicação, ex: https://smitbr.visualstudio.com/SmartLoad/_git/Admin?path=/nginx.conf
https://laravel.com/docs/10.x/deployment#nginx

###Script de inicialização: cp /home/default /etc/nginx/sites-enabled/default; service nginx restart
- Este comando é responsável por sobrescrever as configurações padrão pelas corretas para o funcionamento da aplicação.
