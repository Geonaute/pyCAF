# Synopsis

pyCAF est un *framework* d'audit de sécurité de configuration. Il a vocation à accompagner l'auditeur en lui facilitant la manipulation des données pertinentes sur lesquelles il va pouvoir baser son expertise.

# Installation

Pour simplifier l'utilisation de pyCAF, il est recommandé d'utiliser ipython.


    # apt install ipython

Pour le programme s'initialise correctement et que le framework puisse être fonctionnel, il faut déposer le script `ressources/00-pyCAF.py` dans le répertoire `.ipython/profile_default/startup/` du répertoire `/home` de l'utilisateur. Il ne reste ensuite plus qu'à exécuter ipython avec ce fichier  (comportement par défaut s'il n'existe pas d'autre code dans le répertoire `startup`).


    $ ipython

À partir de là, les fichiers de configuration ont été chargés et le contexte d'utilisation de pyCAF (configuration et journalisation) initialisés. Il ne reste plus qu'à utiliser.

# API Reference

La documentation des APIs est disponible sur le wiki du projet (*work in progress*) :
* [documentation de l'API d'analyse](https://github.com/maximeolivier/pyCAF/wiki/Documentation-de-l%27API-d%27analyse "lien vers la documentation de l'API d'analyse")
* [documentation de l'API d'import](https://github.com/maximeolivier/pyCAF/wiki/Documentation-de-l%27API-d%27import "lien vers la documentation de l'API d'import")

La rédaction de cette documentation est en cours et donc incomplète.

# Tests

### Import d'une archive extraite d'un serveur linux

Ce test mentionne l'utilisation d'une archive qui résulte de l'exécution du script `extract_linux_0.1.sh`.


    In [1]: s = importer.Import_server_from_archive("/path/to/the/tar.bz2/archive", config)

### Exécution d'un scénario d'analyse sur le serveur


    In [2]: a = analyzer.AnalyzeServer(s, config)

# Licence

Ce code est publié sous licence GPLv3.