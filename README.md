# ECE-2022-Ing4-Finance-IA1-Gr02
Bienvenue sur le d�p�t du TP Sudoku.

Chaque groupe est invit� � cr�er un [Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) de ce d�p�t principal muni d'un compte sur Github, et d'indiquer dans le fil de suivi de projet du groupe sur le forum son adresse. 

Vous pourrez ensuite travailler de fa�on collaborative sur ce fork  en  [attribuant les permissions d'�ditions](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository) aux autres membres du groupe, en clonant votre fork sur vos machines, par le biais de validations (commits), de push pour remonter les validations sur le server, et de pulls/tirages sur les machines locales des utilisateurs du groupe habilit�s sur le fork. 

Le plus simple sera d'utiliser les [outils int�gr�s � Github](https://docs.microsoft.com/fr-fr/visualstudio/version-control/git-with-visual-studio?view=vs-2019) directement disponible depuis l'environnement [Visual Studio](https://visualstudio.microsoft.com/fr/downloads/). Id�alement, pr�f�rez Visual Studio Community 2019 ou Visual Studio pour Mac � Visual Studio Code, qui est plus versatile, mais sans doute moins adapt� � ce projet. Si vous choisissez toutefois d'utiliser Visual Studio Code, il vous faudra suivre les instructions fournies [pour la prise en charge de c#](https://code.visualstudio.com/docs/languages/csharp) ou [pour celle de .Net](https://code.visualstudio.com/docs/languages/dotnet), et sans doute installer des extensions comme [celle permettant de charger des solutions](https://marketplace.visualstudio.com/items?itemName=fernandoescolar.vscode-solution-explorer). 

Une fois le travail effectu� et remont� sur le fork, vous pourrez cr�er une pull-request depuis le fork vers le d�p�t principal pour fusion et �valuation.

Le fichier de solution "Sudoku.sln" constitue l'environnement de base du travail et s'ouvre dans Visual Studio Community (attention � bien ouvrir la solution et ne pas rester en "vue de dossier").
En l'�tat, la solution contient:
- Un r�pertoire Puzzles contenant 3 fichiers de Sudokus de difficult�s diff�rentes
- Un projet Sudoku.Shared: il consitue la librairie de base de l'application et fournit la d�finition de la classe repr�sentant un Sudoku (GridSudoku) et l'interface � impl�menter par les solvers de sudoku (ISolverSudoku).
- Un projet Sudoku.Z3Solvers qui fournit plusieurs exemples de solvers utilisant la librairie z3 gr�ce au package Nuget correspondant, et qui illustre �galement l'utilisation de Python depuis le langage c# via  [Python.Net](https://pythonnet.github.io/) gr�ce aux packages Nuget correspondants.
- Un projet Sudoku.Benchmark de Console permettant de tester les solvers de Sudoku de fa�on individuels ou dans le cadre d'un Benchmark comparatif. Ce projet r�f�rence les projets de solvers, et c'est celui que vous devez lancer pour tester votre code.

Il s'agira pour chaque groupe de travail, sur le mod�le du projet z3 en exemple, de commencer par:

- [rajouter � la solution votre propre projet](https://docs.microsoft.com/fr-fr/visualstudio/get-started/tutorial-projects-solutions?view=vs-2019), typiquement une biblioth�que de classes en c# au format .Net standard 2.1,
- munir votre projet des librairies n�cessaires, sous forme de [r�f�rences](https://docs.microsoft.com/fr-fr/visualstudio/ide/managing-references-in-a-project?view=vs-2019) ou de packages [Nuget](https://docs.microsoft.com/fr-fr/nuget/consume-packages/install-use-packages-visual-studio). Votre projet devrait poss�der une r�f�rence vers le projet partag� contenant la d�finition de la classe d'une grille de Sudoku et de l'interface d'un solver de Sudoku.
- Cr�er votre classe de Solver (qui n'a pas besoin d'�tre enti�rement fonctionnelle lors de vos premiers archivages) impl�mentant l'interface partag�e.
- faire r�f�rencer votre projet par celui de l'application de Console Benchmark pour le rendre votre solver disponible dans le menu.

Pour ce qui est du Workflow de collaboration:

- Effectuez r�guli�rement une validation/commit pour baliser votre travail localement,
- puis un push pour le remonter vos validations sur votre fork et le partager avec les camarades de votre groupe, qui pourront le r�cup�rer sur leurs propres environnements avec un tirage/pull.
- Lorsque votre environnement est stable (la solution compile sans erreurs et les autres projets ne sont pas affect�s par le v�tre), effectuez une [pull-request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)/requ�te de tirage vers le d�p�t principal pour partager votre travail avec moi et les autres groupes, ainsi que dans l'autre sens � n'importe quel moment que pour r�cup�rer les derni�res mises � jours remont�es par vos camarades sur le d�p�t principal (dont je m'assurerai de la bonne stabilit�). Pour effectuer et valider des pull requests dans un sens ou dans l'autre, vous pouvez utiliser l'[interface de github](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork), ou encore [celle de Visual Studio](https://visualstudio.developpez.com/actu/261500/Pull-Requests-pour-Visual-Studio-une-fonctionnalite-collaborative-devoilee-avec-Visual-Studio-2019-pour-gerer-les-demandes-de-tirage-dans-l-EDI/).
- Vous serez invit� � vous �valuer entre autre sur votre capacit� � participer au projet global en partageant r�guli�rement votre travail et en r�cup�rant celui partag� par les autres groupes. Tout cela sera visible dans la page Insights/Network de v�tre d�p�t ou du d�p�t principal.

Concernant enfin vos sujets respectifs et vos �ventuelles questions sp�cifiques, je vous invite � utiliser le fil de discussion de votre groupe dans le forum du projet.