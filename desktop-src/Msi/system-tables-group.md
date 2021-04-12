---
description: In den Tabellen der Gruppe Systemtabellen werden die Tabellen und Spalten der-Installations Datenbank nachverfolgt.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: System Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130269"
---
# <a name="system-tables-group"></a>System Tabellen Gruppe

In den Tabellen der Gruppe Systemtabellen werden die Tabellen und Spalten der-Installations Datenbank nachverfolgt.

-   In der [ \_ Tabelle](-tables-table.md) Tabellen werden alle Tabellen in der-Datenbank nachverfolgt. Dies schließt Tabellen ein, die Sie möglicherweise für Ihre eigenen benutzerdefinierten Aktionen erstellt haben. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.
-   In der [ \_ Spalten Tabelle](-columns-table.md) werden die Spalten in der-Installations Datenbank nachverfolgt. Temporäre Spalten werden zurzeit von dieser Tabelle nicht nachverfolgt. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.
-   In der [ \_ Tabelle Streams](-streams-table.md) werden eingebettete OLE-Datenströme aufgelistet.
-   In der [ \_ Tabelle Storages](-storages-table.md) werden eingebettete OLE-Datenspeicher aufgelistet.
-   Die [ \_ Validierungs Tabelle](-validation-table.md). \_In der Validierungs Tabelle werden die Typen und die zulässigen Bereiche aller Spalten in der Datenbank nachverfolgt. Die \_ Validierungs Tabelle wird während des Daten Bank Überprüfungsprozesses verwendet, um sicherzustellen, dass alle Spalten berücksichtigt werden und die richtigen Werte aufweisen. Diese Tabelle wird nicht mit der Installer-Datenbank ausgeliefert.

 

 



