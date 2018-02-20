# Burndown charts – BS-Team

We currently create our burndown charts with [trollolo](https://github.com/openSUSE/trollolo).
Installation of trollolo and configuration of [trello](https://trello.com) API credentials is
documented [here](https://github.com/openSUSE/trollolo#installation). Use trollolo >= 0.0.14, otherwise you won't be able to use some of the documented commands. Make sure you use Ruby 2.2-2.4.1, as currently Trollolo is not working with other Ruby versions.

## Starting a new Sprint

- Run:

  ```shell
  trollolo burndown --new-sprint --plot-to-board
  ```

  This command will automatically upload the burndown chart to Trello (you need to use a token with write rights).


## Updating the burndown chart

- Run:

  ```shell
  trollolo burndown --plot-to-board
  ```

  
## Other commands
  
- In case you need to regenerate the image without changing the data for a concrete Sprint (for example if you manually modify the data file) run:

  ```shell
  trollolo plot SPRINT-NUMBER
  ```
  
  This command doesn't automatically upload the burndown chart.


### Note

You can use the `burndown` command without the `--plot-to-board` command, if for any reason you need to update the yaml file without ploting and uploading the images. You can also use `burndown` with the `--plot` option to update the yaml file, plot the image, but without uploading the plotted image to Trello.
    