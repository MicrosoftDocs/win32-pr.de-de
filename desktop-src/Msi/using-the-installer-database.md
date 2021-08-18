---
description: Mit der Installer-Datenbank kann der Entwickler eines Installationspakets die Übertragung einer Anwendung von einer Quelle auf ein Zielimage steuern.
ms.assetid: 058cefcd-83dd-4a13-bd55-11d52f9d41f5
title: Verwenden der Installer-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec91d8982a8ddac47c96303f03a33e4c85cafa70c3ef480c660df42e72f8a84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996060"
---
# <a name="using-the-installer-database"></a>Verwenden der Installer-Datenbank

Mit der [Installer-Datenbank](installer-database.md) kann der Entwickler eines Installationspakets die Übertragung einer Anwendung von einer Quelle auf ein Zielimage steuern. Das Layout der Quell- und Zielimages der Anwendung wird in der [Directory-Tabelle](directory-table.md) angegeben, und die Aktionen, die die Anwendung installieren, werden in sechs Sequenztabellen angegeben:

-   [InstallUISequence-Tabelle](installuisequence-table.md)
-   [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)
-   [AdminUISequence-Tabelle](adminuisequence-table.md)
-   [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
-   [Tabelle "AdvtUISequence"](advtuisequence-table.md)
-   [Tabelle "AdvtExecuteSequence"](advtexecutesequence-table.md)

In den folgenden Abschnitten wird die Verwendung der [Installer-Datenbank](installer-database.md)beschrieben:

-   [Verwenden der Verzeichnistabelle](using-the-directory-table.md)
-   [Verwenden einer Sequenztabelle](using-a-sequence-table.md)
-   [Abrufen eines Datenbankhandle](obtaining-a-database-handle.md)
-   [Committen von Datenbanken](committing-databases.md)
-   [Importieren und Exportieren](importing-and-exporting.md)
-   [Zusammenführen von Datenbanken](merging-databases.md)
-   [Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen](naming-custom-tables-properties-and-actions.md)
-   [OLE-Einschränkungen für Streams](ole-limitations-on-streams.md)
-   [Arbeiten mit Abfragen](working-with-queries.md)
-   [Hinzufügen von Binärdaten zu einer Tabelle mithilfe von SQL](adding-binary-data-to-a-table-using-sql.md)
-   [Arbeiten mit Datensätzen](working-with-records.md)
-   [Arbeiten mit Ordnerspeicherorten](working-with-folder-locations.md)
-   [Angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md)
-   [Durchführen von Aktionen, die während des Entfernens ausgeführt werden sollen](conditioning-actions-to-run-during-removal.md)
-   [Aufrufen von Datenbankfunktionen aus Programmen](calling-database-functions-from-programs.md)
-   [Syntax der bedingten Anweisung](conditional-statement-syntax.md)
-   [Spaltendefinitionsformat](column-definition-format.md)
-   [Bestimmen, ob eine Spalte ein Primärschlüssel oder ein externer Schlüssel ist](determining-whether-a-column-is-a-primary-or-external-key.md)

 

 



