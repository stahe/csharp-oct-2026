# Apprentissage du langage C# 14 avec .NET 10

📖 **Lire le tutoriel : [https://stahe.github.io/csharp-oct-2026/](https://stahe.github.io/csharp-oct-2026/)**

Ce cours apprend le langage [C#](https://learn.microsoft.com/fr-fr/dotnet/csharp/) 14 et la plateforme [.NET](https://dotnet.microsoft.com) 10 **par l'exemple** : plus de deux cents programmes (près de 300 fichiers C#), commentés ligne par ligne, dont les résultats d'exécution sont reproduits. Il part des bases du langage et va jusqu'à l'accès aux bases de données, la programmation réseau et les services web.

C'est la réécriture, pour C# 14 et .NET 10, du cours [Apprentissage du langage C# version 3.0 avec le framework .NET 3.5](https://stahe.github.io/csharp-mai-2008/) (2008) : même plan, mêmes exemples, même fil rouge, mais un code d'aujourd'hui. Tous les programmes compilent **sans erreur ni avertissement** avec le SDK .NET 10 et ont été exécutés ; les résultats reproduits dans le cours sont ceux de ces exécutions.

| Cours C# 3.0 (2008) | Cours C# 14 (2026) |
|---|---|
| C# 3.0, framework .NET 3.5, Windows seulement | C# 14, .NET 10 (LTS), Windows, Linux, macOS |
| Visual C# 2008 Express | VS Code + C# Dev Kit ou Visual Studio 2026, commande `dotnet` |
| projets et solutions `.sln` | applications fichier unique (`dotnet run prog.cs`), solutions `.slnx` |
| interfaces graphiques Windows Forms | chapitre supprimé (les interfaces sont aujourd'hui web) |
| LINQ « non abordé » | LINQ présenté en détail |
| `ArrayList`, `Hashtable`, `BinaryFormatter` | collections génériques, `System.Text.Json` |
| NUnit 2.4, Spring.NET | MSTest 4, Microsoft.Extensions.DependencyInjection |
| `BackgroundWorker`, modèle `BeginXxx` / `EndXxx` | `Task`, `async` / `await`, annulation, `IAsyncEnumerable` |
| SQL Server 2005, ODBC, OLE DB | MySQL 8 (Laragon), MySqlConnector, Entity Framework Core |
| `WebClient`, `WebRequest` | `HttpClient`, `TcpClient` / `TcpListener` asynchrones |
| services web SOAP ASMX | services web REST / JSON avec ASP.NET Core Minimal API |

## Le plan du cours

| Chapitre | Contenu |
|---|---|
| Installation | SDK .NET 10, VS Code / Visual Studio 2026, la commande `dotnet`, applications fichier unique, projets, solutions `.slnx` |
| Les bases du langage | types, littéraux, types nullables, conversions, tableaux, index et plages, opérateurs (`??`, `??=`), expressions `switch` et filtrage par motif, exceptions, énumérations, passage de paramètres, fonctions locales, tuples |
| Classes, structures, interfaces | propriétés (`init`, `required`, mot clé `field` de C# 14), héritage, polymorphisme, opérateurs, indexeurs, structures, interfaces, génériques, records, constructeurs primaires, membres d'extension de C# 14, types référence nullables |
| Classes .NET d'usage courant | chaînes, tableaux, collections, **LINQ**, fichiers texte et binaires, JSON, expressions régulières (`[GeneratedRegex]`) |
| Architectures en couches | couches [dao] / [metier] / [ui], tests unitaires **MSTest**, **injection de dépendances** |
| Délégués, lambdas et événements | `Func`, `Action`, expressions lambda, fermetures, événements, arbres d'expression |
| Les threads d'exécution | `Thread`, synchronisation (`Lock` de C# 13, `Monitor`, `Interlocked`…), collections concurrentes, `Parallel` |
| **La programmation asynchrone** (nouveau) | `Task`, `async` / `await`, `WhenAll`, annulation, progression, flux asynchrones, `Parallel.ForEachAsync`, `Channel<T>` |
| L'accès aux bases de données avec ADO.NET | MySQL, `MySqlConnector`, requêtes paramétrées et injection SQL, transactions, méthodes asynchrones, `DbProviderFactory` |
| **Entity Framework Core** (nouveau) | modèle, CRUD, LINQ traduit en SQL, relations, migrations, concurrence optimiste, SQL brut, injection de dépendances |
| Programmation Internet | TCP/IP, IPv6, clients et serveurs TCP asynchrones, HTTP, `HttpClient`, SMTP |
| Services web | REST / JSON avec ASP.NET Core Minimal API, clients console, client web JavaScript |

## Le fil rouge : un calcul d'impôt en 9 versions

Tout le cours construit, version après version, une application de **calcul de l'impôt sur le revenu** :

- **version 1** : un programme unique ; **version 2** : des classes et des interfaces ; **version 3** : les données lues dans un fichier texte ou JSON ;
- **versions 4 et 5** : une architecture en couches, testée avec MSTest et intégrée par injection de dépendances ;
- **versions 6 et 7** : les données dans une base MySQL, lues avec ADO.NET puis avec Entity Framework Core ;
- **version 8** : un serveur TCP de calcul de l'impôt et son client ;
- **version 9** : un service web REST, son client console et son client web.

## Technologies

C# 14 · .NET 10 · VS Code · Visual Studio 2026 · MSTest 4 · Microsoft.Extensions.DependencyInjection · System.Text.Json · MySQL 8 · MySqlConnector · Entity Framework Core 9 · Pomelo.EntityFrameworkCore.MySql · ASP.NET Core 10 · Laragon

## Prérequis

- Avoir déjà programmé dans un langage quelconque.
- Le [SDK .NET 10](https://dotnet.microsoft.com/download/dotnet/10.0) et un éditeur ([VS Code](https://code.visualstudio.com) avec l'extension C# Dev Kit, ou Visual Studio 2026) ; [Laragon](https://laragon.org) pour MySQL (chapitres sur les bases de données). Les instructions d'installation sont données dans le cours.

## Auteur

Ce cours et ses codes ont été rédigés par **Claude**, l'IA d'[Anthropic](https://www.anthropic.com) (octobre 2026), à la demande de Serge Tahé, à partir de son cours C# de 2008.

Réviseur : [Serge Tahé](https://stahe.github.io)
