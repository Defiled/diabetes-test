The goal is to run a succesfull prediction in the dockerized environment. However this fails for some reason. To replicate this follow these steps:

1. navigate to this project's directory in your terminal
2. login or open Docker
3. run `docker build -t test-server -f ./Dockerfile .`
4. then run `docker run -p 9000:9000 test-server`
5. navigate to `localhost:9000/run` to trigger a prediction with the hardcoded values specified `app.py`

Note: `app.py` is a mess because I've tried so many things to figure out what's causing it. Seems to be some kind of environment issue, but not sure what.

To rule out that the model, inputs, and script running the model are fine you can test the code locally by running:
`python3 local_test.py`

you should see an output
