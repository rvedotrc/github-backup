Backs up all of a github user's public repositories.

Requirements:

  bash
  git
  perl
  perl YAML::Syck
  wget

  e.g. on Ubuntu,
    sudo apt-get install bash git perl libyaml-syck-perl wget

Execution:

  ./backup-public-repositories-for-user $GITHUB_USER

In detail:

  ./backup-public-repositories-for-user $GITHUB_USER [$DIRECTORY]
    Back up all of a user's public repositories to a given directory (default:
    var/repos/$GITHUB_USER).

  ./backup-public-repository $GITHUB_USER $REPO_NAME $DIRECTORY
    Back up a single public repository.  Clone if $DIRECTORY doesn't yet
    exist; pull if it does.

  ./list-public-repositories-for-user $GITHUB_USER
    List the names of a user's public repositories, one per line

  ./repos.$GITHUB_USER.yaml
    Used to store the list of a user's public repositories

  ./var/repos/$GITHUB_USER/$REPO_NAME
    Default backup location

