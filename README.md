# Nexus
- A utility package designed to read .env files and inject environment variables into your PHP application.

## Description
- Nexus provides an easy and configuration-free method for loading environment variables from a .env file. It’s a lightweight and user-friendly solution to manage environment settings in your application.

## Features
- Load environment variables from a `.env` file into your application.
- Access environment variables using `getenv()`, `$_ENV`, or `$GLOBALS`.
- No configuration required.
- No dependencies.
- Lightweight.
- Easy to use.
- Works with PHP 7.4 and above.
- Works with any PHP framework, library, or application.

## Installation
```bash
composer require josegarcia/nexus
```

## Usage
```php
use Garcia\Nexus;

$filePath = __DIR__ . '/.env.test'; // Assuming .env is present for testing purposes

// Create a temporary .env file for testing
file_put_contents($filePath, "TEST_VAR=123\nANOTHER_VAR=abc");

// Load the .env file
Nexus::load($filePath);

// Check if environment variables are set
echo getenv('TEST_VAR') . "\n";
echo $_ENV['ANOTHER_VAR'] . "\n";
echo $GLOBALS['TEST_VAR'] . "\n";
echo getenv('ANOTHER_VAR') . "\n";
```

