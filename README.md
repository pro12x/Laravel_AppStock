<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

## About AppStock
AppStock is a class staff job, created with the aim of helping with the management of stores, supermarkets and others. They consist of managing the inputs and outputs of each product. With this project we have the possibility of granting roles to the people we want to allow them to manage stocks with us.

Thank you, please send me your suggestions and proposals so that together we can develop the world of tomorrow

## Installing the project
* composer update
* cp .env.example .env
* php artisan vendor:publish -tag=laravel-assets --ansi --force
* php artisan key:generate --ansi

## Relation, Models, Controllers, Migrations
<table align="center">
    <tr>
        <th>#</th>
        <th>Models</th>
        <th>Controllers</th>
        <th>Migrations</th>
        <th>Relation</th>
    </tr>
    <tr>
        <td>1</td>
        <td>User</td>
        <td>UserController</td>
        <td>create_users_table</td>
        <td>ManyToMany(User, Role), OneToMany(User, Product)</td>
    </tr>
</table>
