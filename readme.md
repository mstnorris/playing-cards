# Playing Cards

### Installation

1. Change directory to wherever you install Laravel projects

    ```
    cd ~/path/to/laravel/projects
    ```

2. Clone this repository

    ```
    git clone git@github.com:mstnorris/playing-cards.git playing-cards
    ```

3. Add "192.168.10.10 playing-cards.dev" to your `/etc/hosts` file
4. Add the following to your `Homestead.yaml` file

    ```
    sites:
        - map: playing-cards.dev
          to: /home/vagrant/path/to/laravel/projects/playing-cards/public
    databases:
        - playing-cards
    ````

5. Provision your homestead box (either change directory to where homestead is installed and run

    ```
    vagrant provision
    ```

  Or if you have a global `homestead` command, use that:

  ```
  homestead provision
  ```

6. Change directory into the `playing-cards` project

    ```
    cd playing-cards
    ```

7. Install composer dependencies

    ```
    composer install
    ```

8. Install node dependencies

    ```
    npm install
    ```

9. Run the "vendor" task - Laravel Elixir (gulp)

    ```
    gulp vendor
    ```

10. Then run your own "gulp" task - Laravel Elixir (gulp) 

    ```
    gulp
    ```

11. Run the database migrations and seeders

    ```
    php artisan migrate --seed
    ```

12. Visit "playing-cards.dev" in your browser, you're now good to go.