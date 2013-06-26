# Databus

NREL works off of this repository for databus development.  

There is also documentation(and support available) located at http://buffalosw.com/products/databus/databus-documentation/

If you are an organization that supports databus, contact databus@nrel.gov and we will add you to the list of organizations that offer services for supporting, installing or third party services around databus.  Current organizations are

http://buffalosw.com

QUESTIONS: If you have technical/development questions, please post them on stackoverflow.com with the tag databus.  If you have user related questions, email databus@nrel.gov until we have a user forum setup(we are in the process of setting this up right now)

## Getting Started

```sh
$ git clone git@github.com:deanhiller/databus.git
$ cd databus
$ ./build.sh build
$ cd webapp
$ ./play run
```

The app should be running at: [http://localhost:9000/](http://localhost:9000/). Login with:
* username: dhiller2
* password: nreliscool   

<br>
## Unit Tests - Gradle

The build must be run at least once in order to acquire needed dependencies.  From main databus directory:
```sh
$ cd ${CLONE_DIR}/databus
$ ./build.sh build
```
Once the normal build is run, kick off unit tests with:
```sh
$ ./build.sh runSDITests
```

<br>
## Setting up the Project - Eclipse

In order to use Eclipse for this project, a couple commands must be executed before importing into the IDE.
```sh
$ cd ${CLONE_DIR}/databus
$ ./build.sh build
$ cd webapp
$ ./play eclipsify
```

Doing these 2 steps will ensure that:
- Project dependencies have been correctly resolved
- Play's framework has correctly been set up for the Eclipse IDE

To import into Eclipse, just open Import->Existing Projects into Workspace and use the following path as the root directory:
```sh
${CLONE_DIR}/databus/webapp
```
