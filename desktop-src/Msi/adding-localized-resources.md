---
description: Je nach Anwendung kann die Lokalisierung das Ändern oder Hinzufügen von Ressourcen wie Dateien oder Registrierungsschlüsseln erfordern.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Hinzufügen lokalisierter Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de37bfd3c216018f6c4a6f6866206020576153e55383a9d6b36e67533bbb3b6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829240"
---
# <a name="adding-localized-resources"></a>Hinzufügen lokalisierter Ressourcen

Je nach Anwendung kann die Lokalisierung das Ändern oder Hinzufügen von Ressourcen wie Dateien oder Registrierungsschlüsseln erfordern. Die Lokalisierung der Beispielanwendung MNP2000 erfordert das Hinzufügen einer zusätzlichen Datei zum Paket , Fre.txt und der französischen Version von zwei vorhandenen Dateien: Help.txt und Readme.txt.

Die bewährte Methode besteht in diesem Fall in der Lokalisierung des Pakets, damit die englische und die französische Version sicher auf dem Computer koexistieren können. Dies schließt ein, dass nie zwei verschiedene Dateien mit identischen Dateinamen in demselben Verzeichnis installiert werden. Da Help.txt und Readme.txt in den beiden Sprachversionen identische Dateinamen haben, sollte das französische Paket diese Dateien in einem anderen Verzeichnis als englisch installieren.

Das französische Paket installiert Help.txt in einem neuen Unterverzeichnis des Ordners RedPark, Französisch. Da das Fre.txt der ursprünglichen Hilfekomponente eine Ressource hinzufügt, muss der Komponentencode für die Hilfekomponente in den paketen Französisch und Englisch unterschiedlich sein. Weitere Informationen finden Sie in den Regeln für Komponentencodes unter [Ändern des Komponentencodes.](changing-the-component-code.md)

Das französische Paket installiert Readme.txt im Verzeichnis Französisch, sodass dieser Dateiname nicht mit der englischen Version in Konflikt steht. Die Datei Readme.txt wird mit der Editor installiert, die Komponentenregeln erfordern jedoch keine Änderung des Komponentencodes. In diesem Beispiel sollte der Komponentencode von Editor nicht geändert werden, da RedPark.exe, die in der [Registrierungstabelle](registry-table.md)angegebenen Registrierungswerte, von beiden Sprachversionen gemeinsam genutzt werden. Weitere Informationen [finden Sie unter Hinzufügen von Registrierungsinformationen.](adding-registry-information.md)

Entfernen Sie die englischen Versionen von Help.txt und Readme.txt aus den Quelldateien, und fügen Sie die neuen französischen Versionen von Help.txt, Readme.txt und Fre.txt. Das lokalisierte Paket sollte die Installation von Dateien von der Quelle zum Ziel wie folgt zuordnen.



| Datei        | Beschreibung                  | Pfad zur Quelle                   | Pfad zum Ziel                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | Ausführbare Text-Editor-Datei. | C: \\ \\ Editor \\Redpark.exe | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Redpark.exe |
| Readme.txt  | Eine Informationsdatei.       | C: \\ \\ Editor \\Readme.txt  | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Readme.txt  |
| Help.txt    | Hilfehandbuch                  | C: \\ \\ Editor \\Help.txt    | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Help.txt    |
| Fre.txt     | Telefon Liste                   | C: \\ \\ Editor \\Fre.txt     | \[ProgramFilesFolder \] \\ Red Park French \_ \\ \\Fre.txt     |



 

Verwenden Sie den Datenbank-Editor Orca, der mit dem SDK bereitgestellt wird, oder einen anderen Editor, um die Verzeichnistabelle zu öffnen und einen Datensatz für die Installation des neuen Verzeichnisses Französisch hinzuzufügen.

[Verzeichnistabelle](directory-table.md)



| Verzeichnis                                        | Übergeordnetes \_ Verzeichnis                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**Targetdir**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**Targetdir**](targetdir.md)                   | .                 |
| MEMODIR                                          | NOTEPADDIR                                       | Schrift: Events       |
| HOLDIR                                           | MONDIR                                           | .:Festtage        |
| MENUDIR                                          | NOTEPADDIR                                       | Menü              |
| MONDIR                                           | NOTEPADDIR                                       | Gate              |
| NOTEPADDIR                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Red \_ Park:Editor |
| SPORTDIR                                         | NOTEPADDIR                                       | Sport:Events     |
| FRENCHDIR                                        | NOTEPADDIR                                       | Französisch:.          |



 

Verwenden Sie den Tabellen-Editor, um die ComponentId der Hilfekomponente in MNPFren.msi in eine neue GUID zu ändern.

[Komponententabelle](component-table.md)



| Komponente | Componentid                            | Verzeichnis\_ | Attribute | Bedingung | Keypath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Konzert   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | MEMODIR     | 2          |           | Concert.txt  |
| Tanz     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | MEMODIR     | 2          |           | Dance.txt    |
| Fußball  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Hilfe      | {9ED21229-FE3C-4FE9-B01D-57E00224FD0B} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Editor   | {19BED232-30AB-11D3-91D3-00C04FD70856} | FRENCHDIR   | 2          |           | Redpark.exe  |



 

Verwenden Sie den Tabellen-Editor, um der [Dateitabelle](file-table.md) von MNPFren.msi Fre.txt hinzuzufügen. Geben Sie die LANGID für Französisch in das Feld Sprache für die lokalisierten Dateien ein. Alle anderen Punkte sind gleich. Wenn die installierte Datei eine andere Sprache als die Datei auf dem Computer aufweist, bevorzugt das Installationsprogramm die Datei mit der Sprache, die dem zu installierenden Produkt entspricht. Sprachneutrale Dateien werden als eine andere Sprache behandelt, sodass das zu installierende Produkt wieder bevorzugt wird. Weitere Informationen finden Sie unter [Dateiversionsierungsregeln.](file-versioning-rules.md)

[Dateitabelle](file-table.md)



| Datei         | Komponente\_ | FileName     | FileSize | Version | Sprache | Attribute | Sequenz |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Baseball    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Konzert     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Tanz       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Fußball    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Hilfe        | Help.txt     | 1000     |         | 1036     | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | NewYears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Editor     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Editor     | Readme.txt   | 1000     |         | 1036     | 0          | 1        |
| Fre.txt      | Hilfe        | Fre.txt      | 1000     |         | 1036     | 0          | 1        |



 

Dadurch wird die Beispiellokalisierung abgeschlossen.

 

 



