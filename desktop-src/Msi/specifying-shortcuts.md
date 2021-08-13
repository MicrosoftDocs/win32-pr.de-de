---
description: Die Verknüpfungstabelle und die zugehörigen Tabellen der Installationsdatenbank enthalten Informationen, die zum Installieren von Verknüpfungen erforderlich sind. Weitere Informationen finden Sie unter Program Information Tables Group (Programminformationstabellen) und Editing Installer Shortcuts (Verknüpfungen zum Bearbeiten des Installationsprogramms).
ms.assetid: 0f3adf78-e650-414f-b85d-b53b986eafda
title: Angeben von Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67b43a104ee05b3711ac98395098acf9393faab8e046296e58d93df4d6b9218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624684"
---
# <a name="specifying-shortcuts"></a>Angeben von Verknüpfungen

Die [Verknüpfungstabelle](shortcut-table.md) und die zugehörigen Tabellen der Installationsdatenbank enthalten Informationen, die zum Installieren von Verknüpfungen erforderlich sind. Weitere Informationen finden Sie unter [Program Information Tables Group (Programminformationstabellen)](program-information-tables-group.md) und Editing Installer [Shortcuts (Verknüpfungen des Bearbeitungsinstallationsprogramms).](editing-installer-shortcuts.md)

In diesem Abschnitt fügen Sie Informationen hinzu, die angekündigte und nicht angekündigte Verknüpfungen für das Editor Beispiel angeben.

Öffnen Sie in Ihrem Datenbank-Editor MNP2000.msi, und geben Sie die folgenden Daten in die Tabelle Verknüpfung ein.

[Verknüpfungstabelle](shortcut-table.md)



| Verknüpfung  | Verzeichnis\_ | Name         | Komponente\_ | Ziel             | Argumente | Beschreibung | Hotkey | Symbol\_         | IconIndex | ShowCmd | WkDir |
|-----------|-------------|--------------|-------------|--------------------|-----------|-------------|--------|----------------|-----------|---------|-------|
| sBaseball | MENUDIR     | Baseball.txt | Baseball    | Baseball           |           |             |        | orca \_icon.exe |           |         |       |
| sConcert  | MENUDIR     | Concert.txt  | Konzert     | \[\#Concert.txt\]  |           |             |        |                |           |         |       |
| sDance    | MENUDIR     | Dance.txt    | Tanz       | \[\#Dance.txt\]    |           |             |        |                |           |         |       |
| sFootball | MENUDIR     | Football.txt | Fußball    | \[\#Football.txt\] |           |             |        |                |           |         |       |
| sHelp     | MENUDIR     | Help.txt     | Hilfe        | \[\#Help.txt\]     |           |             |        |                |           |         |       |
| sJanuary  | MENUDIR     | January.txt  | January     | \[\#January.txt\]  |           |             |        |                |           |         |       |
| sNewYears | MENUDIR     | NewYears.txt | NewYears    | \[\#NewYears.txt\] |           |             |        |                |           |         |       |
| sNotepad  | MENUDIR     | Redpark.exe  | Editor     | \[\#Redpark.exe\]  |           |             |        |                |           |         |       |
| sReadme   | MENUDIR     | Readme.txt   | Editor     | \[\#Readme.txt\]   |           |             |        |                |           |         |       |



 

Die Beispielinstallation muss die Installation einer angekündigten Verknüpfung für das Baseball-Feature aktivieren. Dies erfordert die Angabe eines Schlüssels für die Symboltabelle in der \_ Symbolspalte der Verknüpfungstabelle. Für dieses Beispiel können Sie das Symbol für den Orca-Datenbank-Editor kopieren, der mit dem Windows Installer SDK bereitgestellt wird. Exportieren Sie die [Tabelle Symbol](icon-table.md) aus Orca.msi, und führen Sie diese Tabelle dann mit orca oder einem anderen Mergetool in die MNP2000.msi-Datenbank zusammen. Orca erstellt außerdem ein Verzeichnis mit dem Namen Icon in dem Verzeichnis, das MNP2000.msi enthält, und fügt die Binärdatendatei orca \_icon.exe.ibd hinzu. Weitere Informationen finden Sie in der Spalte Daten in der Tabelle Symbol. Die fertige Symboltabelle sollte bei der Anzeige in Orca wie folgt aussehen.

[Symboltabelle](icon-table.md)



| Name           | Daten            |
|----------------|-----------------|
| orca \_icon.exe | \[Binärdaten\] |



 

[Fortsetzen](specifying-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bearbeiten von Installerverknüpfungen](editing-installer-shortcuts.md)
</dt> </dl>

 

 



