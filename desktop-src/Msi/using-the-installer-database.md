---
description: Die Installer-Datenbank ermöglicht es dem Entwickler eines Installationspakets, die Übertragung einer Anwendung von einem Quell-in ein Zielimage zu steuern.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Verwenden der Installer-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb22b9c66547c849b4c9cbd012e78b22d9301756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350234"
---
# <a name="using-the-installer-database"></a>Verwenden der Installer-Datenbank

Die [Installer-Datenbank](installer-database.md) ermöglicht es dem Entwickler eines Installationspakets, die Übertragung einer Anwendung von einem Quell-in ein Zielimage zu steuern. Das Layout der Quell-und Ziel Images der Anwendung wird in der [Verzeichnis](directory-table.md) Tabelle angegeben, und die Aktionen, mit denen die Anwendung installiert wird, werden in sechs Sequenz Tabellen angegeben:

-   [InstallUISequence](installuisequence-table.md) -Tabelle
-   [InstallExecuteSequence](installexecutesequence-table.md) -Tabelle
-   [AdminUISequence](adminuisequence-table.md) -Tabelle
-   [AdminExecuteSequence](adminexecutesequence-table.md) -Tabelle
-   [Advtuisequence](advtuisequence-table.md) -Tabelle
-   [AdvtExecuteSequence](advtexecutesequence-table.md) -Tabelle

In den folgenden Abschnitten wird beschrieben, wie die [Installer-Datenbank](installer-database.md)verwendet wird:

-   [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md)
-   [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md)
-   [Abrufen eines Daten Bank Handles](obtaining-a-database-handle.md)
-   [Commit für Datenbanken](committing-databases.md)
-   [Importieren und Exportieren](importing-and-exporting.md)
-   [Daten Bank Zusammenführung](merging-databases.md)
-   [Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen](naming-custom-tables-properties-and-actions.md)
-   [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)
-   [Arbeiten mit Abfragen](working-with-queries.md)
-   [Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Arbeiten mit Datensätzen](working-with-records.md)
-   [Arbeiten mit Ordner Standorten](working-with-folder-locations.md)
-   [Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
-   [Während des Entfernens auszuführende Aufbereitungs Aktionen](conditioning-actions-to-run-during-removal.md)
-   [Aufrufen von Datenbankfunktionen von Programmen](calling-database-functions-from-programs.md)
-   [Syntax der bedingten Anweisung](conditional-statement-syntax.md)
-   [Spalten Definitions Format](column-definition-format.md)
-   [Bestimmen, ob eine Spalte ein Primärschlüssel oder ein externer Schlüssel ist](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



