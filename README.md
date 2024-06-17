A dockerized version on the [Symfony CLI](https://symfony.com/download) command.

## Usage - Create your new Symfony application
```bash
# Create the project directory
mkdir supercoolwidgets.xyz

# Create the symfony application inside the project directory
docker run --rm \
    -v ./supercoolwidgets.xyz:/app \
    -v ${HOME}/.gitconfig:/root/.gitconfig \
    -w /app \
    chrisshennan/symfony-cli new --webapp /app
```

Note: We're mounting your hosts global `.gitconfig` into the container via `-v ${HOME}/.gitconfig:/root/.gitconfig` as the Symfony CLI sets up the git repository and needs to know who you are i.e. the git configuration values for `user.name` and `user.email`.

## Further Information

See https://chrisshennan.com/blog/creating-symfony-applications-with-symfony-cli-and-docker