---
description: Erstellen Sie eine Kopie des Beispielinstallationspakets Windows InstallerMNP2000.msi und benennen Sie diese Kopie MNP2000t.msi.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Anpassen einer ursprünglichen Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f02f176bb24b1792d9184ebc662a45c9dbfdb8df385b3fb481967c9c8a099a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075040"
---
# <a name="customizing-an-original-database"></a>Anpassen einer ursprünglichen Datenbank

Erstellen Sie eine Kopie des Beispielinstallationspakets Windows InstallerMNP2000.msi und benennen Sie diese Kopie MNP2000t.msi. In den folgenden Schritten passen Sie diese Datei mit einem Datenbanktabellen-Editor wie Orca an, der mit dem SDK bereitgestellt wird, oder einem anderen Datenbank-Editor.

Schließen Sie die neue Ressourcendatei für die Telefonliste Phone.txt Ordner Editor die anderen Quelldateien ein.



| Datei      | BESCHREIBUNG                             | Pfad zur Quelle                 | Pfad zum Ziel                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Eine Ressource für die Telefon \_ List-Funktion. | C: \\ \\ Editor \\phone.txt | \[ProgramFilesFolder \] \\ Red Park \_ \\phone.txt |



 

Verwenden Sie Ihren Datenbank-Editor, um der Dateitabelle einen Datensatz [für](file-table.md) MNP2000t.msi neue Datei hinzuzufügen.

[Dateitabelle](file-table.md)



| Datei      | Komponente\_ | FileName  | FileSize | Version | Sprache | Attribute | Sequenz |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Phone       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Wie im Abschnitt [Verwenden](using-transforms-to-add-resources.md)von Transformationen zum Hinzufügen von Ressourcen erläutert, sollte die Transformation der Installationsdatenbank mindestens eine neue Komponente hinzufügen, um die neue Telefonlistenfunktion zu enthalten. Verwenden Sie den Datenbank-Editor, um der Tabelle [Komponente](component-table.md) des -Editors den folgenden Datensatz MNP2000t.msi.

Die Telefon-Komponente sollte mit einer eindeutigen Komponenten-ID-GUID [identifiziert werden.](guid.md) Wenn Sie das Beispiel reproduzieren, verwenden Sie nicht die gleiche Komponenten-ID-GUID wie in der folgenden Tabelle. Verwenden Sie stattdessen ein Hilfsprogramm wie Guidgen.exe, um eine neue GUID zu generieren. Stellen Sie sicher, dass Sie eine GUID-Zeichenfolge verwenden, die mit dem Windows Installer [GUID-Datentyp](guid.md) konsistent ist.

[Komponententabelle](component-table.md)



| Komponente | Componentid                            | Verzeichnis\_ | Attribute | Bedingung | Keypath   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Phone     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | NOTEPADDIR  | 2          |           | Phone.txt |



 

Verwenden Sie Ihren Datenbank-Editor, um die Daten in der [Featuretabelle des](feature-table.md) MNP2000t.msi. Geben Sie 0 in die Spalte Ebene des Gate-Featuredatensatz ein. Dadurch werden das Gate-Feature und seine untergeordneten Features deaktiviert und diese Features auf der Benutzeroberfläche ausblendet. Beachten Sie, dass das Installationsprogramm keine Features mit der Ebene 0 installiert, da die [**INSTALLLEVEL-Eigenschaft**](installlevel.md) in der [Tabelle Eigenschaft](property-table.md)auf 3 festgelegt ist. Fügen Sie einen Datensatz für das neue Feature Telefon \_ Liste hinzu.

[Featuretabelle](feature-table.md)



| Feature     | Übergeordnetes \_ Feature | Titel         | BESCHREIBUNG                | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Kunst        |                 | Kunst          | Events in Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baseball    | Sport           | Baseball      | Baseball-Spiele             | 17      | 3     | SPORTDIR    | 32         |
| Konzert     | Kunst            | Konzert       | Concert events at Red Park | 21      | 3     | MEMODIR     | 2          |
| Tanz       | Kunst            | Tanz         | Sportereignisse in Red Park   | 23      | 3     | MEMODIR     | 2          |
| Fußball    | Sport           | Fußball      | Football-Spiele             | 19      | 3     | SPORTDIR    | 2          |
| Gate        |                 | Gate          | Red Park es Admissions      | 6       | 0     | NOTEPADDIR  | 0          |
| Hilfe        | Editor         | Hilfe          | Hilfedatei.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January     | Gate            | January       | Januar-Zulassungen         | 10      | 3     | MONDIR      | 2          |
| NewYears    | January         | New Years Day | New Years Day Admissions   | 11      | 3     | HOLDIR      | 2          |
| Editor     |                 | Editor       | Editor Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Infodatei      | Editor         | Infodatei        | Readme-Datei                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport       |                 | Sportereignisse  | Sportereignisse im Red Park   | 14      | 3     | NOTEPADDIR  | 0          |
| \_Telefon Liste |                 | Telefon Liste    | Telefon Liste                 | 24      | 3     | NOTEPADDIR  | 0          |



 

Fügen Sie der [Tabelle FeatureComponents des](featurecomponents-table.md) MNP2000t.msi.

[FeatureComponents-Tabelle](featurecomponents-table.md)



| Feature\_   | Komponente\_ |
|-------------|-------------|
| \_Telefon Liste | Phone       |



 

Fügen Sie in der Verknüpfungstabelle einen neuen [Datensatz hinzu,](shortcut-table.md) um eine Verknüpfung zum Feature Telefon \_ Liste zu erstellen.

[Verknüpfungstabelle](shortcut-table.md)



| Verknüpfung | Verzeichnis\_ | Name      | Komponente\_ | Ziel          | Argumente | BESCHREIBUNG | Hotkey | Symbol\_ | IconIndex | ShowCmd | WkDir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sPhone   | MENUDIR     | Phone.txt | Phone       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Fortsetzen](generating-a-customization-transform.md)

 

 



