---
description: Abhängig von der Anwendung erfordert die Lokalisierung möglicherweise das ändern oder Hinzufügen von Ressourcen, z. b. Dateien oder Registrierungs Schlüsseln.
ms.assetid: f5af0ecd-cb57-4858-88b4-4608893004f6
title: Hinzufügen lokalisierter Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7646499e4bb48e3df9fc1527bff1273e6b6784bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355668"
---
# <a name="adding-localized-resources"></a>Hinzufügen lokalisierter Ressourcen

Abhängig von der Anwendung erfordert die Lokalisierung möglicherweise das ändern oder Hinzufügen von Ressourcen, z. b. Dateien oder Registrierungs Schlüsseln. Die Lokalisierung der Beispielanwendung MNP2000 erfordert das Hinzufügen einer zusätzlichen Datei zum Paket, Fre.txt und den französischen Versionen von zwei vorhandenen Dateien: Help.txt und Readme.txt.

In diesem Fall wird empfohlen, das Paket so zu lokalisieren, dass die englische und die französische Version sicher auf dem Computer nebeneinander vorhanden sein können. Dies schließt die Installation von zwei verschiedenen Dateien mit identischen Dateinamen in dasselbe Verzeichnis ein. Da Help.txt und Readme.txt identische Dateinamen in den beiden Sprachversionen aufweisen, sollte das französische Paket diese Dateien in einem anderen Verzeichnis als das englische installieren.

Das französische Paket installiert Help.txt in einem neuen Unterverzeichnis des Ordners redpark (Französisch). Da durch das Hinzufügen von Fre.txt der ursprünglichen Hilfe Komponente eine Ressource hinzugefügt wird, muss sich der Komponenten Code für die Hilfe Komponente in den französischen und englischen Paketen unterscheiden. Weitere Informationen finden Sie in den Regeln für Komponenten Codes beim [Ändern des Komponenten Codes](changing-the-component-code.md).

Mit dem französischen Paket wird Readme.txt in das Verzeichnis Französisch installiert, sodass der Dateiname nicht mit der englischen Version in Konflikt steht. Die Datei Readme.txt wird mit der Notepad-Komponente installiert, aber für die Komponenten Regeln ist das Ändern des Komponenten Codes nicht erforderlich. In diesem Beispiel sollte der Komponenten Code von Notepad nicht geändert werden, da RedPark.exe, die in der [Registrierungs Tabelle](registry-table.md)angegebenen Registrierungs Werte von beiden Sprachversionen gemeinsam verwendet werden. Siehe [Hinzufügen von Registrierungsinformationen](adding-registry-information.md).

Entfernen Sie die englischen Versionen von Help.txt und Readme.txt aus den Quelldateien, und fügen Sie die neuen französischen Versionen Help.txt, Readme.txt und Fre.txt hinzu. Das lokalisierte Paket sollte die Installation von Dateien von der Quelle zum Ziel wie folgt zuordnen.



| Datei        | BESCHREIBUNG                  | Pfad zur Quelle                   | Pfad zum Ziel                                         |
|-------------|------------------------------|----------------------------------|--------------------------------------------------------|
| Redpark.exe | Ausführbare Datei des Text-Editors. | C: \\ Beispiel für \\ Notepad \\Redpark.exe | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Französisch \\Redpark.exe |
| Readme.txt  | Eine Informationsdatei.       | C: \\ Beispiel für \\ Notepad \\Readme.txt  | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Französisch \\Readme.txt  |
| Help.txt    | Hilfe manuell                  | C: \\ Beispiel für \\ Notepad \\Help.txt    | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Französisch \\Help.txt    |
| Fre.txt     | Telefonliste                   | C: \\ Beispiel für \\ Notepad \\Fre.txt     | \[ProgramFilesFolder \] \\ rotes \_ Park \\ Französisch \\Fre.txt     |



 

Verwenden Sie den Datenbank-Editor, der mit dem SDK bereitgestellt wird, oder einen anderen Editor, um die Verzeichnis Tabelle zu öffnen und einen Datensatz für die Installation des neuen Verzeichnisses (Französisch) hinzuzufügen.

[Verzeichnis Tabelle](directory-table.md)



| Verzeichnis                                        | Über \_ geordnetes Verzeichnis                                | DefaultDir        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [**TARGETDIR**](targetdir.md)                   |                                                  | SourceDir         |
| [**ProgramFilesFolder**](programfilesfolder.md) | [**TARGETDIR**](targetdir.md)                   | .                 |
| Argsdir                                          | Notepaddir                                       | Kunst: Ereignisse       |
| Holdir                                           | Mondir                                           | .: Feiertage        |
| Menudir                                          | Notepaddir                                       | Menü              |
| Mondir                                           | Notepaddir                                       | Tors              |
| Notepaddir                                       | [**ProgramFilesFolder**](programfilesfolder.md) | Roter \_ Park: Notepad |
| Sportdir                                         | Notepaddir                                       | Sport: Ereignisse     |
| Frenchdir                                        | Notepaddir                                       | Französisch:.          |



 

Verwenden Sie den Tabellen-Editor, um die Komponenten-ID der Hilfe Komponente in MNPFren.msi in eine neue GUID zu ändern.

[Komponenten Tabelle](component-table.md)



| Komponente | ComponentID                            | Verzeichnis\_ | Attribute | Bedingung | KEYPATH      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Ball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | Sportdir    | 2          |           | Baseball.txt |
| Konzert   | {76fa7a80-33F 6-11d3-91d8-00c04f d70856} | Argsdir     | 2          |           | Concert.txt  |
| Abhängigkeit     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | Argsdir     | 2          |           | Dance.txt    |
| Verbandes  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | Sportdir    | 2          |           | Football.txt |
| Hilfe      | {9ed21229-fe3c-4fe9-B01D-57e00224sd0b} | Notepaddir  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | Mondir      | 2          |           | January.txt  |
| Newyears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | Holdir      | 2          |           | NewYears.txt |
| Editor   | {19bed232-30ab-11d3-91d3-00c04f d70856} | Frenchdir   | 2          |           | Redpark.exe  |



 

Verwenden Sie den Tabellen-Editor, um der [Dateitabelle](file-table.md) MNPFren.msi Fre.txt hinzuzufügen. Geben Sie die langid für Französisch in das Sprachfeld für die lokalisierten Dateien ein. Alle anderen Dinge, die gleich sind, wenn die Datei, die installiert wird, eine andere Sprache als die Datei auf dem Computer hat, bevorzugt das Installationsprogramm die Datei mit der Sprache, die mit dem installierten Produkt übereinstimmt. Sprachneutrale Dateien werden nur als eine andere Sprache behandelt, sodass das Produkt, das installiert wird, erneut bevorzugt wird. Weitere Informationen finden Sie unter [Regeln für die Datei Versions](file-versioning-rules.md)Verwaltung.

[Dateitabelle](file-table.md)



| File         | Komponente\_ | FileName     | FileSize | Version | Sprache | Attribute | Sequenz |
|--------------|-------------|--------------|----------|---------|----------|------------|----------|
| Baseball.txt | Ball    | Baseball.txt | 1000     |         |          | 0          | 1        |
| Concert.txt  | Konzert     | Concert.txt  | 1000     |         |          | 0          | 1        |
| Dance.txt    | Abhängigkeit       | Dance.txt    | 1000     |         |          | 0          | 1        |
| Football.txt | Verbandes    | Football.txt | 1000     |         |          | 0          | 1        |
| Help.txt     | Hilfe        | Help.txt     | 1000     |         | 1036     | 0          | 1        |
| January.txt  | January     | January.txt  | 1000     |         |          | 0          | 1        |
| NewYears.txt | Newyears    | NewYears.txt | 1000     |         |          | 0          | 1        |
| Redpark.exe  | Editor     | Redpark.exe  | 45328    |         |          | 0          | 1        |
| Readme.txt   | Editor     | Readme.txt   | 1000     |         | 1036     | 0          | 1        |
| Fre.txt      | Hilfe        | Fre.txt      | 1000     |         | 1036     | 0          | 1        |



 

Dadurch wird die Beispiel Lokalisierung abgeschlossen.

 

 



