
# Basic PHP MVC

  

This is a simple PHP project structured around the **Model-View-Controller (MVC)** design pattern. The project demonstrates automatic routing, where the controller and action are determined dynamically from the URL, enabling a clean and extensible architecture.

  

## Key Features:

-  **Automatic Routing**: Routes are determined automatically from the URL. The first segment of the URL corresponds to the controller, and the second segment corresponds to the action.

-  **Model**: Handles data and business logic of the application.

-  **View**: Displays the user interface and presentation layer.

-  **Controller**: Handles user input, processes it, and returns the appropriate response.

  

## How Routing Works:

- The URL is parsed to extract the controller and action.

- The controller is instantiated dynamically, and the action is called.

- If no action is specified, the `index` action is used by default.

  

For example:

-  `http://yourdomain.com/teste/index` will call the `TesteController` and its `index` action.

-  `http://yourdomain.com/teste/anotherAction` will call the `TesteController` and its `anotherAction` method.

  

## Technologies Used:

- PHP (7.x or higher)

- Basic routing and URL handling

- PostgreSQL (pgsql) for database connection (can be changed to another database in `database.php`)

  

## Installation:

  

1. Clone the repository:

```bash

git clone https://github.com/RickCarletti/Basic_Project_PHP_MVC.git

```

  

2. Navigate to the project folder:

```bash

cd Basic_Project_PHP_MVC

```
3. Create the `config.php` file: 
    - Copy the `config_basic.php` file to `config.php`.
    - Edit `config.php` to add your database connection details (hostname, username, password, and database name).
 
 4. Database Connection: 
    - The default database connection is set for **PostgreSQL** (`pgsql`). You can change this by editing the `database.php` file and modifying the connection settings to match your desired database type.

 
5. Open the project in a local server environment (e.g., XAMPP, WAMP, or PHP's built-in server).
## Example Directory Structure:

```plaintext
Basic_Project_PHP_MVC/
│
├── app/
│   ├── Config/
│   |	├── config_basic.php (base to config.php)
│   |	├── config.php (ignored needed to work)
│   |	└── database.php
│   ├── Controllers/
│   |	├── BaseController.php
│   |	└── TesteController.php (template)
│   ├── Models/
│   |	└── Teste.php (template)
│   └── Views/
│   |	├── layout/
│   |	|	├──	footer.php
│   |	|	└──	header.php
│   |	├── teste/ (template)
│   |	|	├──	cadastrar.php (template)
│   |	|	├──	editar.php (template)
│   |	|	└──	index.php (template)
├── index.php
├── .gitignore
└── README.md
 ```

## How it Works:

- The router is defined in `index.php`, where the URL is parsed and used to determine the appropriate controller and action.

- Controllers handle the logic and invoke methods in the models.

- Views are rendered with the data provided by the controller.

  

## License:

This project is not licensed. You can freely use, edit, and distribute it as needed.	