---
description: Die Tabellen in der Gruppe Installationsprozedur steuern Aufgaben, die während der Installation von Standardaktionen und benutzerdefinierten Aktionen ausgeführt werden.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Gruppe "Tabellen für Installationsprozedur"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c66cc377fdf36969699f0e150fc30a02363ed24aa1848c4492917bffda7bc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633585"
---
# <a name="installation-procedure-tables-group"></a>Gruppe "Tabellen für Installationsprozedur"

Die Tabellen in der Gruppe Installationsprozedur steuern Aufgaben, die während der Installation von [Standardaktionen](standard-actions.md) und [benutzerdefinierten Aktionen](custom-actions.md)ausgeführt werden.

Einige Tabellen in dieser Gruppe steuern eine übergeordnete Aktion, indem sie eine Sequenz von Aktionen bereitstellen. Jede der folgenden Sequenztabellen steuert einen Teil einer übergeordneten Aktion.

-   [InstallUISequence-Tabelle](installuisequence-table.md)
-   [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)
-   [AdminUISequence-Tabelle](adminuisequence-table.md)
-   [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
-   [Tabelle "AdvtUISequence"](advtuisequence-table.md)
-   [Tabelle "AdvtExecuteSequence"](advtexecutesequence-table.md)

Es kann Situationen geben, in denen eine Installation etwas tun muss, was nicht nur mit [Standardaktionen](standard-actions.md)möglich ist. Um das größtmögliche Maß an Flexibilität zu bieten, bietet das Installationsprogramm Setupautoren die Möglichkeit, eigene benutzerdefinierte Aktionen zu erstellen. Wenn Sie über benutzerdefinierte Aktionen verfügen, sollten Sie sie beim Installationsprogramm registrieren, indem Sie die Tabelle CustomAction auffüllen.

Die [Tabelle CustomAction](customaction-table.md) bietet die Möglichkeit, benutzerdefinierten Code und Daten in den Installationsprozess zu integrieren. Der ausgeführte Code kann ein in der Datenbank enthaltener Stream, eine kürzlich installierte Datei oder eine vorhandene ausführbare Datei sein.

In den folgenden Tabellen werden die Funktionen des Installationsprogramms erweitert, um Dateien und Ordner während der Installation zu bearbeiten.

-   Die [Tabelle RemoveFile](removefile-table.md) enthält eine Liste der Dateien, die während der Installation entfernt werden.
-   Die [Tabelle RemoveIniFile](removeinifile-table.md) enthält die Informationen, die eine Anwendung aus .ini Dateien entfernen muss.
-   Die [Tabelle RemoveRegistry](removeregistry-table.md) enthält die Informationen, die aus der Systemregistrierung gelöscht werden, wenn die entsprechende Komponente installiert werden soll.
-   Die [Tabelle CreateFolder](createfolder-table.md) listet die Ordner auf, die während der Installation erstellt werden müssen. Obwohl das Installationsprogramm Ordner nach Bedarf erstellt, werden diese entfernt, sobald sie leer sind. Die Ordnerliste in der CreateFolder-Tabelle wird erst gelöscht, wenn die Komponente deinstalliert wurde.
-   Die [Tabelle MoveFile](movefile-table.md) enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis auf dem Computer des Benutzers in ein Zielverzeichnis verschoben oder kopiert werden sollen. Es ist nicht erforderlich, die Tabelle MoveFile zu verwenden, um die Dateien zu beschreiben, die den installierten Komponenten zugeordnet sind.

Um die erforderlichen Bedingungen einzurichten, die zum Initiieren der Installation erfüllt sein müssen, füllen Sie die LaunchCondition-Tabelle auf.

Die [LaunchCondition-Tabelle](launchcondition-table.md) enthält eine Liste von Bedingungen, die erfüllt sein müssen, damit die Aktion erfolgreich ausgeführt werden kann.

 

 



