# Задача

Необходимо разработать императивный pipeline. Pipeline должен уметь заменять пароли для учётных записей в зашифрованном файле.

# Требования

1. Pipeline должен состоять из 5 стейджей
    - cтейдж клонирования репозитория, содержащего зашифрованный файл([https://github.com/shukalov/test_encr_file](https://github.com/shukalov/test_encr_file));
    - стейдж клонирования роли Ansible([https://github.com/shukalov/sb_encr_ansible](https://github.com/shukalov/sb_encr_ansible));
    - стейдж генерации нового пароля и записи его в файл ролью Ansible;
    - стейдж коммита изменённого файл в репозиторий;
    - стейдж отправки отчёта на e-mail.
2. Pipeline должен использовать shared library(https://github.com/shukalov/jenkins-shared)
3. E-mail для отчёта, scm адреса для репозиториев с файлом паролей и ролью ansible указываются в property файле, расположенном в resources
4. УЗ, для которой необходимо сменить пароль должна указываться как входной параметр для job’ы
5. Код pipeline  и shared library должны храниться в scm
