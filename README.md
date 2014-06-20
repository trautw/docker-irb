docker-irb
==========

#Introduction#
Call a interactive ruby shell

#Installation#
Call
`thor :image_build`

#Usage#
`./d-irb`

#Options#
You can set e.g. `export DOCKER_HOST="tcp://docker-box.example.com:4243"` in `env.properties`

The file `etc/timezone` contains the timezone you whish to use. You have to rebuild the image after changing it.
