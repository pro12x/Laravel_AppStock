<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

## About AppStock (Laravel 9)
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
    <tr>
        <td>2</td>
        <td>Role</td>
        <td>RoleController</td>
        <td>create_roles_table</td>
        <td>ManyToMany(Role, User)</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Product</td>
        <td>ProductController</td>
        <td>create_products_table</td>
        <td>ManyToOne(Product, User), OneToMany(Product, Entry), OneToMany(Product, Output), ManyToOne(Product, Category)</td>
    </tr>
    <tr>
        <td>4</td>
        <td>Category</td>
        <td>CategoryController</td>
        <td>create_categories_table</td>
        <td>OneToMany(Category, Product)</td>
    </tr>
    <tr>
        <td>5</td>
        <td>Entry</td>
        <td>EntryController</td>
        <td>create_entries_table</td>
        <td>ManyToOne(Entry, Product)</td>
    </tr>
    <tr>
        <td>6</td>
        <td>Output</td>
        <td>OutputController</td>
        <td>create_outputs_table</td>
        <td>ManyToOne(Output, Product)</td>
    </tr>
</table>
