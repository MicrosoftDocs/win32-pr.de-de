---
description: Die Tabellen in der Installationsprozedur Gruppe steuern Tasks, die während der Installation durch Standard Aktionen und benutzerdefinierte Aktionen ausgeführt werden.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Gruppe "Installationsprozedur Tabellen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349758"
---
# <a name="installation-procedure-tables-group"></a>Gruppe "Installationsprozedur Tabellen"

Die Tabellen in der Installationsprozedur Gruppe steuern Tasks, die während der Installation durch [Standard Aktionen](standard-actions.md) und [benutzerdefinierte Aktionen](custom-actions.md)ausgeführt werden.

Einige der Tabellen in dieser Gruppe steuern eine auf hoher Ebene durch Bereitstellung einer Aktions Sequenz. Jede der folgenden Sequenz Tabellen steuert einen Teil einer Aktion auf hoher Ebene.

-   [InstallUISequence-Tabelle](installuisequence-table.md)
-   [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)
-   [AdminUISequence-Tabelle](adminuisequence-table.md)
-   [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
-   [Advtuisequence-Tabelle](advtuisequence-table.md)
-   [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)

Es kann Situationen geben, in denen eine Installation etwas durchführen muss, das nur [Standard Aktionen](standard-actions.md)verwendet werden kann. Um das höchste Maß an Flexibilität zu bieten, bietet das Installationsprogramm Setup Autoren die Möglichkeit, eigene benutzerdefinierte Aktionen zu erstellen. Wenn Sie über benutzerdefinierte Aktionen verfügen, sollten Sie diese beim Installer registrieren, indem Sie die Tabelle CustomAction auffüllen.

Die [Tabelle CustomAction](customaction-table.md) bietet die Möglichkeit, benutzerdefinierten Code und Daten in den Installationsprozess zu integrieren. Der Code, der ausgeführt wird, kann ein in der Datenbank enthaltener Stream, eine zuletzt installierte Datei oder eine vorhandene ausführbare Datei sein.

In den folgenden Tabellen werden die Funktionen des Installers zum Bearbeiten von Dateien und Ordnern während der Installation erweitert.

-   Die [Tabelle RemoveFile](removefile-table.md) enthält eine Liste von Dateien, die während der Installation entfernt werden.
-   Die [removeinifile-Tabelle](removeinifile-table.md) enthält die Informationen, die eine Anwendung aus INI-Dateien entfernen muss.
-   Die [removeregistry-Tabelle](removeregistry-table.md) enthält die Informationen, die aus der Systemregistrierung gelöscht werden, wenn die entsprechende Komponente für die Installation ausgewählt ist.
-   In der Tabelle "| [atefolder](createfolder-table.md) " sind die Ordner aufgelistet, die während der Installation erstellt werden müssen. Obwohl das Installationsprogramm Ordner erstellt, wenn Sie benötigt werden, werden diese entfernt, sobald Sie leer sind. Die Ordnerliste in der Tabelle "upatefolder" wird erst gelöscht, wenn die Komponente deinstalliert wurde.
-   Die [Tabelle "muvefile](movefile-table.md) " enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis auf dem Computer des Benutzers in ein Zielverzeichnis verschoben oder kopiert werden sollen. Es ist nicht erforderlich, die Tabelle "muvefile" zu verwenden, um die Dateien zu beschreiben, die den Komponenten zugeordnet sind, die Sie installieren.

Um die erforderlichen Bedingungen einzurichten, die erfüllt sein müssen, um die Installation zu initiieren, füllen Sie die LaunchCondition-Tabelle auf.

Die [LaunchCondition-Tabelle](launchcondition-table.md) enthält eine Liste mit Bedingungen, die alle erfüllt sein müssen, damit die Aktion erfolgreich ausgeführt werden kann.

 

 



