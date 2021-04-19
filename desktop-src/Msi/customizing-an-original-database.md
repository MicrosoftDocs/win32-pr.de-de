---
description: Erstellen Sie eine Kopie der Beispiel Windows Installer-Installationspakets MNP2000.msi, und benennen Sie diese Kopie MNP2000t.msi um.
ms.assetid: 1251d377-7143-4a6b-81d0-0915f952be10
title: Anpassen einer ursprünglichen Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3222ebce146e891c7b16c70eb78f0f26b95727c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355498"
---
# <a name="customizing-an-original-database"></a>Anpassen einer ursprünglichen Datenbank

Erstellen Sie eine Kopie der Beispiel Windows Installer-Installationspakets MNP2000.msi, und benennen Sie diese Kopie MNP2000t.msi um. In den folgenden Schritten passen Sie diese Datei mit einem Datenbanktabellen-Editor wie z. b. Orca an, der mit dem SDK bereitgestellt wird, oder mit einem anderen Daten Bank Editor.

Fügen Sie die neue Ressourcen Datei für die Telefonliste Phone.txt in den Ordner Notepad mit den anderen Quelldateien ein.



| Datei      | BESCHREIBUNG                             | Pfad zur Quelle                 | Pfad zum Ziel                               |
|-----------|-----------------------------------------|--------------------------------|----------------------------------------------|
| phone.txt | Eine Ressource für das Telefon \_ Listen Feature. | C: \\ Beispiel für \\ Notepad \\phone.txt | \[Ordner "ProgramFilesFolder \] \\ Red \_ Park \\phone.txt" |



 

Verwenden Sie den Datenbank-Editor, um der [Dateitabelle](file-table.md) MNP2000t.msi einen Datensatz für die neue Datei hinzuzufügen.

[Dateitabelle](file-table.md)



| File      | Komponente\_ | FileName  | FileSize | Version | Sprache | Attribute | Sequenz |
|-----------|-------------|-----------|----------|---------|----------|------------|----------|
| Phone.txt | Phone       | Phone.txt | 1000     |         |          | 0          | 1        |



 

Wie im Abschnitt: [Verwenden von Transformationen zum Hinzufügen von Ressourcen](using-transforms-to-add-resources.md)erläutert, sollte die Transformation der Installations Datenbank eine oder mehrere neue Komponenten hinzufügen, um die neue Telefonlisten Funktion zu enthalten. Fügen Sie den folgenden Datensatz mit dem Datenbank-Editor der [Komponenten Tabelle](component-table.md) MNP2000t.msi hinzu.

Die Telefon Komponente sollte mit einer eindeutigen Komponenten-ID- [GUID](guid.md)identifiziert werden. Wenn Sie das Beispiel reproduzieren, verwenden Sie nicht dieselbe Komponenten-ID-GUID wie in der folgenden Tabelle. Verwenden Sie stattdessen ein Dienstprogramm wie Guidgen.exe, um eine neue GUID zu generieren. Stellen Sie sicher, dass Sie eine GUID-Zeichenfolge verwenden, die mit dem Datentyp Windows Installer [GUID](guid.md) konsistent ist.

[Komponenten Tabelle](component-table.md)



| Komponente | ComponentID                            | Verzeichnis\_ | Attribute | Bedingung | KEYPATH   |
|-----------|----------------------------------------|-------------|------------|-----------|-----------|
| Phone     | {D152A1EC-9F7A-4E45-B0DC-ED6EE5D829F8} | Notepaddir  | 2          |           | Phone.txt |



 

Verwenden Sie den Datenbank-Editor, um die Daten in der [Featuretabelle](feature-table.md) MNP2000t.msi zu ändern. Geben Sie in der Spalte Ebene des Gates-Funktionsdaten Satzes den Wert 0 ein. Dadurch werden die Gate-Funktion und ihre untergeordneten Funktionen deaktiviert und diese Features aus der Benutzeroberfläche ausgeblendet. Beachten Sie, dass das Installationsprogramm keine Funktionen mit der Ebene 0 installiert, da die [**INSTALLLEVEL**](installlevel.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)auf 3 festgelegt ist. Fügen Sie einen Datensatz für das neue Telefon \_ Listen Feature hinzu.

[Funktions Tabelle](feature-table.md)



| Funktion     | Über \_ geordnetes Element | Titel         | BESCHREIBUNG                | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|-------------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Grafiken        |                 | Grafiken          | Kunstveranstaltungen im red Park.   | 20      | 3     | Notepaddir  | 0          |
| Ball    | Sport           | Ball      | Baseball Spiele             | 17      | 3     | Sportdir    | 32         |
| Konzert     | Grafiken            | Konzert       | Konzertveranstaltungen im roten Park | 21      | 3     | Argsdir     | 2          |
| Abhängigkeit       | Grafiken            | Abhängigkeit         | Tanz Ereignisse im red Park   | 23      | 3     | Argsdir     | 2          |
| Verbandes    | Sport           | Verbandes      | Fußballspiele             | 19      | 3     | Sportdir    | 2          |
| Tors        |                 | Tors          | Zulassung von Red Park      | 6       | 0     | Notepaddir  | 0          |
| Hilfe        | Editor         | Hilfe          | Hilfedatei.                 | 5       | 3     | Notepaddir  | 1          |
| January     | Tors            | January       | Januar-Zuweisungen         | 10      | 3     | Mondir      | 2          |
| Newyears    | January         | Neuer Arbeitstag | Eintritts Zeit für neue Jahre   | 11      | 3     | Holdir      | 2          |
| Editor     |                 | Editor       | Editor für Notepad             | 1       | 3     | Notepaddir  | 0          |
| Infodatei      | Editor         | Infodatei        | Infodatei                | 3       | 3     | Notepaddir  | 0          |
| Sport       |                 | Sport Veranstaltungen  | Sport Veranstaltungen im roten Park   | 14      | 3     | Notepaddir  | 0          |
| Telefon \_ Liste |                 | Telefonliste    | Telefonliste                 | 24      | 3     | Notepaddir  | 0          |



 

Fügen Sie der [FeatureComponents-Tabelle](featurecomponents-table.md) MNP2000t.msi den folgenden Datensatz hinzu.

[FeatureComponents-Tabelle](featurecomponents-table.md)



| Funktion\_   | Komponente\_ |
|-------------|-------------|
| Telefon \_ Liste | Phone       |



 

Fügen Sie einen neuen Datensatz in die Verknüpfungs [Tabelle](shortcut-table.md) ein, um eine Verknüpfung mit der Telefon \_ Listenfunktion zu erstellen.

[Verknüpfungs Tabelle](shortcut-table.md)



| Abkürzung | Verzeichnis\_ | Name      | Komponente\_ | Ziel          | Argumente | BESCHREIBUNG | Hotkey | Symbol\_ | IconIndex | ShowCmd | Wkdir |
|----------|-------------|-----------|-------------|-----------------|-----------|-------------|--------|--------|-----------|---------|-------|
| sphone   | Menudir     | Phone.txt | Phone       | \[\#Phone.txt\] |           |             |        |        |           |         |       |



 

[Fortsetzen](generating-a-customization-transform.md)

 

 



