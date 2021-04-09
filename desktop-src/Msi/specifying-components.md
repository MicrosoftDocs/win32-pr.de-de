---
description: Der Windows Installer installiert und entfernt Blöcke von Ressourcen, die als Windows Installer Komponenten bezeichnet werden. Weitere Informationen finden Sie Untergruppe "core tables" und Komponenten und Funktionen.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Angeben von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98cb254498236b85ab5c2bc0df3bd32892227b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862911"
---
# <a name="specifying-components"></a>Angeben von Komponenten

Der Windows Installer installiert und entfernt Blöcke von Ressourcen, die als [Windows Installer Komponenten](windows-installer-components.md)bezeichnet werden. Weitere Informationen finden Sie unter [Gruppe "Core Tables](core-tables-group.md) " und [Komponenten und Funktionen](components-and-features.md).

In diesem Abschnitt fügen Sie der Komponenten [Tabelle](component-table.md) , die Sie unter [Importieren einer leeren Datenbank](importing-a-blank-database.md)erstellt haben, Informationen zu den Komponenten hinzu, die vom Notepad-Beispiel verwendet werden. Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md) und [Definieren von Installationsprogramm Komponenten](defining-installer-components.md).

Das Notepad-Beispiel verwendet acht Komponenten zum Steuern von Ressourcen.



| Komponente | Ressourcen                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Ball  | Baseball.txt, sbaseball                                                                                               |
| Konzert   | Concert.txt, sconcert                                                                                                 |
| Abhängigkeit     | Dance.txt, sdance                                                                                                     |
| Verbandes  | Football.txt, sfußball                                                                                               |
| Hilfe      | Help.txt, sHelp                                                                                                       |
| January   | January.txt, sjanuary                                                                                                 |
| Newyears  | NewYears.txt, snewyears                                                                                               |
| Editor   | Redpark.exe, Readme.txt, sInfo Me, SNotepad, **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Notepad Sample** |



 

Jede Komponente sollte mit einer eindeutigen Komponenten-ID- [GUID](guid.md)identifiziert werden. Wenn Sie das Beispiel reproduzieren, sollten Sie die gleichen Komponenten-ID-GUIDs in der folgenden Tabelle nicht wieder verwenden. Verwenden Sie stattdessen ein Dienstprogramm, z. b. Guidgen.exe, um neue GUIDs für die Komponenten zu generieren.

Stellen Sie sicher, dass Sie eine GUID-Zeichenfolge verwenden, die mit dem Datentyp Windows Installer GUID konsistent ist. Weitere Informationen finden Sie unter [Ändern des Komponenten Codes](changing-the-component-code.md) und [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md)

Geben Sie mithilfe von Orca oder einem anderen Daten Bank Editor die folgenden Daten in die leere [Komponenten Tabelle](component-table.md) MNP2000.msi ein. Verwenden Sie die unten gezeigten GUIDs in der Spalte ComponentID in Ihrem Beispiel nicht.



| Komponente | ComponentID                            | Verzeichnis\_ | Attribute | Bedingung | KEYPATH      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Ball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | Sportdir    | 2          |           | Baseball.txt |
| Konzert   | {76fa7a80-33F 6-11d3-91d8-00c04f d70856} | Argsdir     | 2          |           | Concert.txt  |
| Abhängigkeit     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | Argsdir     | 2          |           | Dance.txt    |
| Verbandes  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | Sportdir    | 2          |           | Football.txt |
| Hilfe      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | Notepaddir  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | Mondir      | 2          |           | January.txt  |
| Newyears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | Holdir      | 2          |           | NewYears.txt |
| Editor   | {19bed232-30ab-11d3-91d3-00c04f d70856} | Notepaddir  | 2          |           | Redpark.exe  |



 

Das Quell-und Zielverzeichnis für jede Komponente wird durch den in die Spalte Verzeichnis eingegebenen Wert angegeben \_ . Das Installationsprogramm löst den Speicherort dieses Verzeichnisses mithilfe der Informationen in der Verzeichnis Tabelle auf. Das Installationsprogramm verwendet die Schlüssel Pfad Dateien, die in der KEYPATH-Spalte angegeben sind, um jede Komponente zu erkennen. Die Attribute für die Remote Ausführung werden im Beispiel festgelegt, sodass die Komponenten von der Quelle ausgeführt oder lokal ausgeführt werden können.

[Fortsetzen](specifying-files-and-file-attributes.md)

 

 



