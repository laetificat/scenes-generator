# Home Assistant Scenes Generator

This script will create a unified scenes.yaml file and uses the filename of
the file as a scene name, this way you can duplicate scenes easily.

For example:
You have a movie.yaml file which sets your lights to 10%, and with alexa you
can call "Alexa, tell Home Assistant I want to watch a movie". This is fine, but
sometimes you want to change it up a little. So you can make a symlink to the
movie.yaml and call it netflix.yaml, now you can use Alexa to say "I want to
watch Netflix" without actually duplicating the scene manually.
Every change made in movie.yaml will copy over to netflix.yaml, but you have
to run this script every time you change or add a scene.

To use this script:
1. Place it into a directory containing your scenes and only scenes!
2. Edit the SCENES_DIR variable
3. Edit your Home Assistant configuration file to use the scenes.yaml file
4. Run this script with bash generate_scenes.sh
It outputs the names of the scenes so you can easily copy and pase them into
the alexa console.

Remember, back up your original scene files, especially if you have one called
scenes, this script removes this file on every run!
