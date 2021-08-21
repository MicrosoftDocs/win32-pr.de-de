---
description: Die Tabellen der Systemtabellengruppe verfolgen die Tabellen und Spalten der Installationsdatenbank nach.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Systemtabellengruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c05bfd06bcff049d2aea847a2bb8d0c4c3fc3d1443a615f75912ac7d4f86d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623919"
---
# <a name="system-tables-group"></a>Systemtabellengruppe

Die Tabellen der Systemtabellengruppe verfolgen die Tabellen und Spalten der Installationsdatenbank nach.

-   Die [ \_ Tabelle Tables](-tables-table.md) verfolgt alle Tabellen in der Datenbank nach. Dies schließt Tabellen ein, die Sie möglicherweise für Ihre eigenen benutzerdefinierten Aktionen erstellt haben. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.
-   In [ \_ der Tabelle Spalten](-columns-table.md) werden Spalten in der Installationsdatenbank verfolgt. Temporäre Spalten werden derzeit von dieser Tabelle nicht nachverfolgt. Fragen Sie diese Tabelle ab, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.
-   In [ \_ Streams Tabelle werden](-streams-table.md) eingebettete OLE-Datenströme aufgeführt.
-   In [ \_ der Tabelle Speicher werden](-storages-table.md) eingebettete OLE-Datenspeicher aufgeführt.
-   Die [ \_ Validierungstabelle](-validation-table.md). In \_ der Tabelle Überprüfung werden die Typen und zulässigen Bereiche jeder Spalte in der Datenbank verfolgt. Die Validierungstabelle wird während des Datenbankvalidierungsprozesses verwendet, um sicherzustellen, dass alle Spalten berücksichtigt werden und \_ die richtigen Werte haben. Diese Tabelle ist nicht im Lieferumfang der Installer-Datenbank enthalten.

 

 



