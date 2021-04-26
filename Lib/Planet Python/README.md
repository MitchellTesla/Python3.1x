Planet Python

Last update: April 26, 2021 04:40 PM UTC

April 26, 2021
Zato Blog
Checking your Zato version details
The seemingly simple zato --version command packs in several interesting details that are helpful in understanding what Zato version one currently uses - let’s find out what they all mean.

General pattern
When you run zato --version, it will return output similar to what is below.

$ zato --version
$ Zato 3.2+rev.ef895c1b2-py3.6.9-ubuntu.18.04-bionic
λ zato --version
λ Zato 3.2+rev.13074a556-py3.9.4-windows-10-10.0.19042-sp0-Professional


Each time, the output follows the same, general pattern:

zato --version pattern
Major version - this is a major Zato version that you use, e.g. 3.1, 3.2 and similar. Each major version has its own branch on GitHub whose name is in the format of support/[major.version], e.g. support/3.2 for Zato 3.2.

Git commit ID - the exact Git commit ID (revision) that this Zato installation is built from. The commit is taken from the support branch indicated by the major version field. This lets you compare if you have the newest revision for the particular support branch. Simply go to GitHub, select the support branch and check if there are any newer commits. If there are, run update.sh to bring your installation to the latest revision.

Python version - the Python version that your Zato installation uses.

Operating system - the name of the operating system that the command is executed on. It will be “windows” for Windows systems and a distribution’s name for Linux systems.

OS Version - more details about the operating system’s version. How much is returned depends on the system - Windows installations return particulars, such as the service pack in use, while Linux systems do not return such details.

OS Codename (optional) - some systems have a codename, e.g. Bionic for Ubuntu 18.04 or Focal for Ubuntu 20.04. The field will not exist unless a given OS has a codename.

Note that the output from the command does not change whether Zato is installed directly in a given system or via Vagrant or Docker / Kubernetes. For instance, an Ubuntu system running under Docker quickstart will be identified simply as Ubuntu.



More examples
Here are more examples taken from systems that Zato 3.2 currently supports.

Windows
Note below that the system is Windows Server 2019 but it is still reported as Windows 10 because this is what the OS reports and it is the “ServerDatacenter” part that identifies it as a server edition.

λ zato --version
λ Zato 3.2+rev.13074a556-py3.9.4-windows-10-10.0.17763-sp0-ServerDatacenter
Ubuntu
$ zato --version
$ Zato 3.2+rev.ef895c1b2-py3.8.2-ubuntu.20.04-focal
RHEL / CentOS
$ zato --version
$ Zato 3.2+rev.ef895c1b2-py3.6.8-rhel.8.3-ootpa
SUSE
Note that, in the case of Suse, there is no OS codename because the system does not report any.

$ zato --version
$ Zato 3.2+rev.ef895c1b2-py3.8.2-sles.15.2
Debian
$ zato --version
$ Zato 3.2+rev.ef895c1b2-py3.7.3-debian.10-buster


So, now, you know how to check your version of Zato and what each part of the output means.

Next steps
Start the tutorial to learn more technical details about Zato, including its architecture, installation and usage. After completing it, you will have a multi-protocol service representing a sample scenario often seen in banking systems with several applications cooperating to provide a single and consistent API to its callers.

Visit the support page if you would like to discuss anything about Zato with its creators

Para aprender más sobre las integraciones de Zato y API en español, haga clic aquí

April 26, 2021 04:40 PM UTC
