# Analyze your open source code for free

If you have your source code published on GitHub, you can analyze your ObjectScript code for free and check results in https://community.objectscriptquality.com.

You only need to create the file `.github/workflows/objectscript-quality.yml` in your project with following content:

```
name: objectscriptquality
on: push

jobs:
  linux:
    name: Linux build
    runs-on: ubuntu-latest

    steps:
    - name: Execute ObjectScript Quality Analysis
      run: wget https://raw.githubusercontent.com/litesolutions/objectscriptquality-jenkins-integration/master/iris-community-hook.sh && sh ./iris-community-hook.sh
```

That's all!! Now you only need to wait some minutes to get the results in https://community.objectscriptquality.com.