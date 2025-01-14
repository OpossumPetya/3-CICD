## Homework 1
*[#homework]() [#cicd1]()*
1. Create a dummy pileline:
- Open gitlab.
- Import [course project](https://github.com/tdevopsschool/course-project/tree/main) into your personal gitlab space.
- Create a pipeline with 3 stages “build – test – deploy” with dummy `echo` scripts.
2. Send screenshot of the pipeline to the course chat with homework's hashtags.

### Links 1
- [Gitlab docs](https://docs.gitlab.com)
- [Registering Gitlab Runner](https://docs.gitlab.com/runner/register/index.html)
- [Import project to Gitlab by URL](https://docs.gitlab.com/ee/user/project/import/repo_by_url.html)

Additional information:
- [Martin Fowler’s CI](https://martinfowler.com/articles/continuousIntegration.html)
- [Martin Fowler’s CD](https://martinfowler.com/bliki/ContinuousDelivery.html)
- [CD SAFE](https://v46.scaledagileframework.com/continuous-delivery-pipeline)

## Homework 2-1
*[#homework]() [#cicd2_1]()*
1. Build applcaitions:
- Configure `.gitlab-ci.yml` to build applications in build stage without dockerization.
- Keep built `.jar` files as job artifacts with expiration in 1 hour.
2. Send screenshots of artifacts to the course chat with homework's hashtags.

### Links 2-1
- [.gitlab-ci.yml file](https://docs.gitlab.com/ee/ci/yaml/gitlab_ci_yaml.html)
- [Predefined variables](https://docs.gitlab.com/ee/ci/variables/predefined_variables.html)
- [Gitlab job artifacts](https://docs.gitlab.com/ee/ci/pipelines/job_artifacts.html)

## Homework 2-2
*[#homework]() [#cicd2_2]()*
1. Keep gradle cache for build jobs.
2. When added – send, with homework's hashtags, the lines from jobs logs that show cache is created and stored.

### Links 2-2
- [Gitlab caching](https://docs.gitlab.com/ee/ci/caching/)

## Homework 3-1
*[#homework]() [#cicd3_1]()*
1. Dockerize applications:
- Add new stage **dockerization**.
- Create jobs use **dind service** to package jar files from build stage and push images.
- Image tag names should start with `dind-` and end with short commit hash.
2. Addinitionally you need to add a docker config as Gitlab file variable DOCKER_CONFIG to push images in Gitlab registry. You will need predefined Gitlab variables for that.
3. Send screenshots of using dind in `gitlab-ci.yml` with homework's hashtags.

### Links 3-1
- [Use Docker-in-Docker](https://docs.gitlab.com/ee/ci/docker/using_docker_build.html)
- [Use Docker to build Docker images](https://docs.gitlab.com/ee/ci/docker/using_docker_build.html)

Additional
- [Docker breakout privilege escalation](https://book.hacktricks.xyz/linux-hardening/privilege-escalation/docker-breakout/docker-breakout-privilege-escalation)
- [Understanding Docker container escapes](https://blog.trailofbits.com/2019/07/19/understanding-docker-container-escapes)

## Homework 3-2
*[#homework]() [#cicd3_2]()*
1. Dockerize applications with Kaniko:
- Image tag names should start with `kaniko-` and end with short commit hash
- Compare the two approaches, which one is faster
1. Send screenshots with all dockerization jobs (dind and Kaniko) in `gitlab-ci.yml` with homework's hashtags.
2. Remove DIND dockerization and keep Kaniko as best practice.

### Links 3-2
- [Kaniko docs](https://github.com/GoogleContainerTools/kaniko)
- [Using Kaniko to build Docker images](https://docs.gitlab.com/ee/ci/docker/using_kaniko.html)

## Homework 4-1
*[#homework]() [#cicd4_1]()*
1. Rewrite **.gitlab-ci.yml** to use `include` directive:
- Create new repo for CI yml files
- Move CI from course project repo into new CI repo
- Use **include** to inject CI from new project into course project
2. Screenshots with files of new CI and course project repositories should be sent to the course chat with homework's hashtags.

### Links 4-1
- [Gitlab anchors](https://docs.gitlab.com/ee/ci/yaml/yaml_optimization.html#anchors)
- [Gitlab extends](https://docs.gitlab.com/ee/ci/yaml/yaml_optimization.html#use-extends-to-reuse-configuration-sections)
- [Gitlab CI include](https://docs.gitlab.com/ee/ci/yaml/includes.html)
- [Use extends and include together](https://docs.gitlab.com/ee/ci/yaml/yaml_optimization.html#use-extends-and-include-together)

## Homework 4-2
*[#homework]() [#cicd4_2]()*

*You will use this workpiece later in Kubernetes module*

1. Add dummy deploy jobs for “dev” and “prod” environments:
- Add any URLs for both environments
- Add a condition for deploying the application to the production environment only from the master branch, using **rules:**
  - Add a variable with different values, depending on the environment for which a job is being started
  - Protect the variable for Production environment
  - Use `echo` to confirm the result
2. Screenshot with deployed environments (**Deployments** -> **Environments**) should be sent to the course chat with homework's hashtags.

### Links 4-2
- [Environments and deployments](https://docs.gitlab.com/ee/ci/environments/)

## Additional links
- [API resources](https://docs.gitlab.com/ee/api/api_resources.html)
