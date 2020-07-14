## jx-pipeline log

Display a build log

***Aliases**: logs*

### Usage

```
jx-pipeline log [flags]
```

### Synopsis

Display a build log

### Examples

  # Display a build log - with the user choosing which repo + build to view
  jx get build log
  
  # Pick a build to view the log based on the repo cheese
  jx get build log --repo cheese
  
  # Pick a pending Tekton build to view the log based
  jx get build log -p
  
  # Pick a pending Tekton build to view the log based on the repo cheese
  jx get build log --repo cheese -p
  
  # Pick a Tekton build for the 1234 Pull Request on the repo cheese
  jx get build log --repo cheese --branch PR-1234
  
  # View the build logs for a specific tekton build pod
  jx get build log --pod my-pod-name

### Options

```
      --branch string            Filters the branch
      --build string             The build number to view
      --context string           Filters the context of the build
  -c, --current                  Display logs using current folder as repo name, and parent folder as owner
      --fail-with-pod            Return an error if the pod fails
  -f, --filter string            Filters all the available jobs by those that contain the given text
  -g, --giturl string            The git URL to filter on. If you specify a link to a github repository or PR we can filter the query of build pods accordingly
  -h, --help                     help for log
  -o, --owner string             Filters the owner (person/organisation) of the repository
  -p, --pending                  Only display logs which are currently pending to choose from if no build name is supplied
      --pod string               The pod name to view
  -r, --repo string              Filters the build repository
  -t, --tail                     Tails the build log to the current terminal (default true)
  -w, --wait                     Waits for the build to start before failing
  -d, --wait-duration duration   Timeout period waiting for the given pipeline to be created (default 5m0s)
```

### Options inherited from parent commands

```
  -b, --batch-mode   Runs in batch mode without prompting for user input
      --verbose      Enables verbose output. The environment variable JX_LOG_LEVEL has precedence over this flag and allows setting the logging level to any value of: panic, fatal, error, warn, info, debug, trace
```

### SEE ALSO

* [jx-pipeline](jx-pipeline.md)	 - commands for working with Jenkins X Pipelines

###### Auto generated by spf13/cobra on 3-Jul-2020