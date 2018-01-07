# NAME

mitlm-docker - [MIT Language Modeling Toolkit](https://github.com/mitlm/mitlm) installed in a docker image and accessible through a command line interface.

# INSTALLATION AND USAGE

The docker image is available in docker hub, see the respective [docker hub page](https://hub.docker.com/r/mauvilsa/mitlm/).

To install first pull the docker image tag of your choosing, using a command such as:

    docker pull mauvilsa/mitlm:TAG

The image could be used for extending it but it also provides a command line interface so that the toolkit tools can be used from the host system like any other command.

## Command line interface

First you need to copy the command line interface script to some directory in your path.

    docker run --rm -u $(id -u):$(id -g) -v $HOME:$HOME mauvilsa/mitlm:TAG bash -c "cp /usr/local/bin/mitlm-docker $HOME/bin"

Then the docker image needs to be tagged as mitlm:active to indicate to the command line interface which is the image tag to use.

    docker tag mauvilsa/mitlm:TAG mitlm:active

After this, the tool can be used like any other command, i.e.

    mitlm-docker --help
    mitlm-docker COMMAND [ARGUMENTS]

The MIT License (MIT)

Copyright (c) 2018-present, Mauricio Villegas <mauricio_ville@yahoo.com>
