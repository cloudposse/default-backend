![Cloud Posse](https://cloudposse.com/logo-300x69.png)

# default-backend ![Build Status](https://g.codefresh.io/api/badges/build?repoOwner=cloudposse&repoName=default-backend&branch=master&pipelineName=default-backend&accountName=cloudposse) [![Slack Community](https://slack.cloudposse.com/badge.svg)](https://slack.cloudposse.com)

This is a default-backend server powered by Nginx. It's purpuse is to serve as a default backend for an ALB default target group with the [`terraform-aws-alb`](https://github.com/cloudposse/terraform-aws-alb) module	, much the way a [`nginx-default-backend`](https://github.com/cloudposse/charts/blob/master/incubator/nginx-default-backend/) is used with ingress controllers for kubernetes.

The default backend is an HTTP service that handles all URL paths and hosts that the ALB does not understand (i.e., all the requests that are not mapped with an Ingress).

Basically, a default backend reponds to two URLs:

- `/healthz` that returns 200
- `/` that returns 404

## Demo

![Screenshot](docs/demo.png)

## Usage

```
docker run -p 1234:80 clouposse/default-backend:latest
```

## Help

**Got a question?**

File a GitHub [issue](https://github.com/cloudposse/default-backend/issues), send us an [email](mailto:hello@cloudposse.com) or reach out to us on [Slack](https://slack.cloudposse.com).

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/cloudposse/default-backend/issues) to report any bugs or file feature requests.

### Developing

If you are interested in being a contributor and want to get involved in developing this project, we would love to hear from you! Shoot us an [email](mailto:hello@cloudposse.com).

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

**NOTE:** Be sure to merge the latest from "upstream" before making a pull request!


## License

[APACHE 2.0](LICENSE) © 2018 [Cloud Posse, LLC](https://cloudposse.com)

See [LICENSE](LICENSE) for full details.

    Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.


## About

This project is maintained and funded by [Cloud Posse, LLC][website].

![Cloud Posse](https://cloudposse.com/logo-300x69.png)

Like it? Please let us know at <hello@cloudposse.com>

We love [Open Source Software](https://github.com/cloudposse/)!

See [our other projects][community]
or [hire us][hire] to help build your next cloud platform.

  [website]: https://cloudposse.com/
  [community]: https://github.com/cloudposse/
  [hire]: https://cloudposse.com/contact/


## Contributors

| [![Erik Osterman][erik_img]][erik_web]<br/>[Erik Osterman][erik_web] | [![Andriy Knysh][andriy_img]][andriy_web]<br/>[Andriy Knysh][andriy_web] |[![Igor Rodionov][igor_img]][igor_web]<br/>[Igor Rodionov][igor_img]|[![Sarkis Varozian][sarkis_img]][sarkis_web]<br/>[Sarkis Varozian][sarkis_web] |
|-------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|

[erik_img]: http://s.gravatar.com/avatar/88c480d4f73b813904e00a5695a454cb?s=144
[erik_web]: https://github.com/osterman/
[andriy_img]: https://avatars0.githubusercontent.com/u/7356997?v=4&u=ed9ce1c9151d552d985bdf5546772e14ef7ab617&s=144
[andriy_web]: https://github.com/aknysh/
[igor_img]: http://s.gravatar.com/avatar/bc70834d32ed4517568a1feb0b9be7e2?s=144
[igor_web]: https://github.com/goruha/
[sarkis_img]: https://avatars3.githubusercontent.com/u/42673?s=144&v=4
[sarkis_web]: https://github.com/sarkis/
