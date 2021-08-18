---
description: Der Windows Installer installiert und entfernt Ressourcenblöcke, die als Installationskomponenten Windows werden. Weitere Informationen finden Sie unter Kerntabellengruppe und Komponenten und Features.
ms.assetid: e51dffed-d1cb-4a12-8615-0c0f612f993b
title: Angeben von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2264784d3edaad5b46017e3d337f8abfec66e1b60d18ba54388b03beddb13b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628000"
---
# <a name="specifying-components"></a>Angeben von Komponenten

Der Windows Installer installiert und entfernt Ressourcenblöcke, die als Windows [Installer Components bezeichnet werden.](windows-installer-components.md) Weitere Informationen finden Sie unter [Core Tables Group](core-tables-group.md) and Components and [Features](components-and-features.md).

In diesem Abschnitt fügen Sie Der Komponententabelle, die Sie [](component-table.md) in Importieren einer leeren Datenbank erstellt haben Editor Informationen zu den komponenten hinzu, die vom beispiel [verwendet werden.](importing-a-blank-database.md) Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten und](organizing-applications-into-components.md) Definieren von [Installerkomponenten.](defining-installer-components.md)

Das Editor verwendet acht Komponenten, um Ressourcen zu steuern.



| Komponente | Ressourcen                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| Baseball  | Baseball.txt, sBaseball                                                                                               |
| Konzert   | Concert.txt, sConcert                                                                                                 |
| Tanz     | Dance.txt, sDance                                                                                                     |
| Fußball  | Football.txt, sFootball                                                                                               |
| Hilfe      | Help.txt, sHelp                                                                                                       |
| January   | January.txt, sJanuary                                                                                                 |
| NewYears  | NewYears.txt, sNewYears                                                                                               |
| Editor   | Redpark.exe, Readme.txt, sReadme, sNotepad, **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Editor Sample** |



 

Jede Komponente sollte mit einer eindeutigen Komponenten-ID-GUID [identifiziert werden.](guid.md) Wenn Sie das Beispiel reproduzieren, sollten Sie nicht die gleichen Komponenten-ID-GUIDs in der folgenden Tabelle wiederverwenden. Verwenden Sie stattdessen ein Hilfsprogramm wie Guidgen.exe, um neue GUIDs für Ihre Komponenten zu generieren.

Stellen Sie sicher, dass Sie eine GUID-Zeichenfolge verwenden, die mit dem Windows Installer GUID-Datentyp konsistent ist. Weitere Informationen finden Sie unter [Ändern des Komponentencodes](changing-the-component-code.md) und [Was geschieht, wenn die Komponentenregeln verletzt werden?](what-happens-if-the-component-rules-are-broken.md)

Verwenden Sie Orca oder einen anderen Datenbank-Editor, um die folgenden Daten in die leere [Komponententabelle der](component-table.md) MNP2000.msi. Verwenden Sie die unten in der Spalte ComponentId des Beispiels gezeigten GUIDs nicht wieder.



| Komponente | Componentid                            | Verzeichnis\_ | Attribute | Bedingung | Keypath      |
|-----------|----------------------------------------|-------------|------------|-----------|--------------|
| Baseball  | {F54ABAC0-33F2-11D3-91D7-00C04FD70856} | SPORTDIR    | 2          |           | Baseball.txt |
| Konzert   | {76FA7A80-33F6-11D3-91D8-00C04FD70856} | MEMODIR     | 2          |           | Concert.txt  |
| Tanz     | {CCF834A1-33F8-11D3-91D8-00C04FD70856} | MEMODIR     | 2          |           | Dance.txt    |
| Fußball  | {CCF834A0-33F8-11D3-91D8-00C04FD70856} | SPORTDIR    | 2          |           | Football.txt |
| Hilfe      | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| January   | {CF0BC690-33C9-11D3-91D6-00C04FD70856} | MONDIR      | 2          |           | January.txt  |
| NewYears  | {A42D9140-33D8-11D3-91D6-00C04FD70856} | HOLDIR      | 2          |           | NewYears.txt |
| Editor   | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

Das Quell- und Zielverzeichnis für jede Komponente wird durch den In die Spalte Verzeichnis eingegebenen Wert \_ angegeben. Das Installationsprogramm löst den Speicherort dieses Verzeichnisses mithilfe der Informationen in der Directory-Tabelle auf. Das Installationsprogramm verwendet die in der KeyPath-Spalte angegebenen Schlüsselpfaddateien, um jede Komponente zu erkennen. Die Remoteausführungsattribute werden im Beispiel festgelegt, sodass die Komponenten aus der Quelle oder lokal ausgeführt werden können.

[Fortsetzen](specifying-files-and-file-attributes.md)

 

 



