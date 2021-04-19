---
description: Die Verknüpfungs Tabelle und die zugehörigen Tabellen der Installations Datenbank enthalten Informationen, die für die Installation von Verknüpfungen erforderlich sind. Weitere Informationen finden Sie in der Gruppe "Programm Informationstabellen" und unter Bearbeiten der
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Angeben von Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29edf10a51827880a67826320d7f8415e70ea52a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348329"
---
# <a name="specifying-shortcuts"></a>Angeben von Verknüpfungen

Die Verknüpfungs [Tabelle](shortcut-table.md) und die zugehörigen Tabellen der Installations Datenbank enthalten Informationen, die für die Installation von Verknüpfungen erforderlich sind. Weitere Informationen finden Sie in der [Gruppe "Programm Informationstabellen](program-information-tables-group.md) " und unter [Bearbeiten](editing-installer-shortcuts.md)der

In diesem Abschnitt fügen Sie Informationen hinzu, die angekündigte und nicht angekündigte Verknüpfungen für das Notepad-Beispiel angeben.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die Verknüpfungs Tabelle ein.

[Verknüpfungs Tabelle](shortcut-table.md)



| Abkürzung  | Verzeichnis\_ | Name         | Komponente\_ | Ziel             | Argumente | BESCHREIBUNG | Hotkey | Symbol\_         | IconIndex | ShowCmd | Wkdir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sbaseball | Menudir     | Baseball.txt | Ball    | Ball           |           |             |        | Orca- \_icon.exe |           |         |       |
| sconcert  | Menudir     | Concert.txt  | Konzert     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sdance    | Menudir     | Dance.txt    | Abhängigkeit       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sfußball | Menudir     | Football.txt | Verbandes    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | Menudir     | Help.txt     | Hilfe        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sjanuar  | Menudir     | January.txt  | January     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| snewyears | Menudir     | NewYears.txt | Newyears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| SNotepad  | Menudir     | Redpark.exe  | Editor     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sInfo   | Menudir     | Readme.txt   | Editor     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

Die Beispiel Installation erfordert die Installation einer angekündigten Verknüpfung für das Baseball Feature. Hierfür muss ein Schlüssel für die Symboltabelle in der Symbol Spalte der Verknüpfungs Tabelle angegeben werden \_ . Im Rahmen dieses Beispiels können Sie das Symbol für den mit dem Windows Installer SDK bereitgestellten Daten Bank Editor für Orca kopieren. Exportieren Sie die [Symboltabelle](icon-table.md) aus Orca.msi, und führen Sie diese Tabelle dann mithilfe von Orca oder einem anderen Mergetool in der MNP2000.msi Datenbank zusammen. Von Orca wird auch ein Verzeichnis mit dem Namen Icon im Verzeichnis erstellt, das MNP2000.msi enthält, und die binäre Symbol Datei "Orca \_icon.exe. ibd" wird hinzugefügt. Informationen finden Sie in der Datenspalte in der Symboltabelle. Die fertige Symboltabelle sollte wie folgt aussehen, wenn Sie in Orca angezeigt wird.

[Symboltabelle](icon-table.md)



| Name           | Daten            |
|----------------|-----------------|
| Orca- \_icon.exe | \[Binärdaten\] |



 

[Fortsetzen](specifying-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bearbeiten von Installationsprogramm Kombinationen](editing-installer-shortcuts.md)
</dt> </dl>

 

 



