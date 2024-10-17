# Moonshine

## Setup

* Install `uv` for Python environment management
  
  - Follow instructions [here](https://github.com/astral-sh/uv)

* Create and activate virtual environment
  
  ```shell
    $ uv venv env_moonshine
    $ source env_moonshine/bin/activate
  ```

* Install the `useful-moonshine` package from this github repo
  
  ```shell
  $ uv pip install useful-moonshine@git+https://github.com/usefulsensors/moonshine.git
  ```
  
  * _Note for UsefulSensors: Since the repo is not public yet, installing from the github URI is not possible yet. Do this instead:_
  
  * ```shell
    $ git clone git@github.com:usefulsensors/moonshine.git
    $ cd moonshine
    $ uv pip install -e .
    $ cd ../
    # Make sure you are out of the current directory too, as you
    # don't want moonshine in your path (import moonshine in python
    # will mistakenly use the wrong path)
    ```

* Test transcribing an audio file
  
  ```shell
  $ python
  >>> import moonshine
  >>> moonshine.transcribe('ever_tried_10s.wav')
  ['Ever tried ever failed, no matter try again fail again fail better.']
  ```


