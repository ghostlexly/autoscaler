![Alt text](preview.png "Preview of autoscaler for Linux")

# autoscaler

Run automatically your applications scaled via xpra.

This tool will create a shortcut of your actual app to run it always scaled with the autoscaler runtime binary.

### /!\ Caution : Do a backup of your app before

## Usage:
````
Usage: autoscaler [--restore] application

--restore  Restore the older binaries of an application
         and stop using autoscaler.

````

## Example with gimp

### create a new shortcut
````
sudo ./autoscaler gimp
````
Your app is now scaled for all next usages. You have to restart it for the changes to take effect.

### try the scaled app
````
gimp
````

### remove the autoscaling shortcut
````
sudo ./autoscaler --restore gimp
````

## Only runtime usage

You can call the runtime app from anywhere with this command.

````
autoscaler-runtime /usr/bin/gimp
````