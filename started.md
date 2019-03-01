# Say Hello to ComplianceAsCode


## What will you learn

* ... the project overview, so you will get a clearer idea what is where, and what can you use the project for.
* ... how to build the content from the source (hence the name `ComplianceAsCode`), and you will examine what gets built.
* ... how to find where to search the source corresponding to a result.


## What have we done for you

1. We have cloned the [ComplianceAsCode repository](https://github.com/ComplianceAsCode/content.git) to the `content` directory.
1. We have installed dependencies that are required for the content build:

   * `cmake, `make`,
   * `openscap-utils`, and finally
   * `python3-pyyaml`, `python3-jinja2`.

1. We have edited the project's source code and introduced some typos there, so you can learn how to find and fix them.


## Hands-on


### Building the content

The ComplianceAsCode/content project uses `cmake` build system.
The build itself is based on Python, the `oscap` tool, and XSLT transforms.

To build the content, take the following steps:

1. Go to the `build` directory.
1. If it is the first build, or you are not exactly sure what were the last changes since the last build, re-run `cmake` by executing `cmake ..`.
1. Run `make <product>` to build the content you are interested in, or `make all` to build everything.
   Running `make` without arguments will build content for all products (i.e. it is the same as `make all`) that are available, which takes a lot of time.
1. After the build finishes, let's explore the built content.


TODO: Terminal output from successful build here.
TODO: A file listing here.


### Examine the guides

What people love about the project are HTML guides that are a great resource for those interested in of what rules a policy consists of.
In the `ComplianceAsCode` project, policies referred to as **security profiles**, and HTML guides are built to the `build/guides`.
Guide filenames have a `ssg-<product>-guide-<policy>.html` form, so the guide for the RHEL8 OSPP profile has the `ssg-rhel8-ospp.html` form.
Give it a try!

As a security policy is an ordered list of rules, guide is an ordered list of descriptions of those rules.
Rules are organized in a system of hierarchical groups.
Consider for example the `Set Password Minimum Length` [rule entry](file:///root/content/build/guides/ssg-rhel8-guide-ospp.html#xccdf_org.ssgproject.content_rule_accounts_password_pam_minlen).


TBContinued, see [workshop.md] for inspiration.
