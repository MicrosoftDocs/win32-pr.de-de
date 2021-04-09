---
description: Weitere Informationen finden Sie unter Hinzufügen von Tabellen zur Datenbank.
title: Hinzufügen von Tabellen zur Datenbank
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958665"
---
# <a name="adding-tables-to-the-database"></a>Hinzufügen von Tabellen zur Datenbank


_**Gilt für:** Windows | Windows Server_

## <a name="adding-tables-to-the-database"></a>Hinzufügen von Tabellen zur Datenbank

Tabellen sind eine heterogene Sammlung von Datensätzen, die die Daten in der Datenbank physisch und logisch gruppieren. Tabellen werden durch ihren Namen eindeutig identifiziert. Die Tabellen-ID ([JET_TABLEID](./jet-tableid.md)) ist ein Handle für einen Cursor, der zum Aktualisieren und Navigieren in Tabellen verwendet wird. Sie können mehrere [JET_TABLEID](./jet-tableid.md) in derselben Tabelle öffnen.

Eine vorhandene Tabelle wird im Aufruf von [jetopentable](./jetopentable-function.md)geöffnet, und es wird eine neue Tabelle ohne Zeilen oder Spalten mit [jetkreatetable](./jetcreatetable-function.md)erstellt. Zum atomischen Erstellen einer Tabelle mit einem anfänglichen Satz von Spalten und Indizes rufen Sie [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) oder [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)auf. Die anfängliche Größe der Tabelle wird im *lpages* -Parameter in [jetupatetable](./jetcreatetable-function.md) oder im **ulpages** -Member der [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur im Aufruf von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)angegeben. Tabellen werden automatisch vergrößert, wenn der Tabelle Daten hinzugefügt werden. Das Wachstum ist proportional zur anfangs Größe der Tabelle. Spalten können jederzeit mit [jetaddcolumn](./jetaddcolumn-function.md)der Tabelle hinzugefügt werden. Wenn die Anwendung nicht mehr auf die Tabelle zugreifen muss, kann der Cursor mit [jetclosetable](./jetclosetable-function.md)geschlossen werden. Die Tabelle kann durch einen Befehl von [jetdeletetable](./jetdeletetable-function.md)gelöscht werden.

Tabellen Vorgänge sollten innerhalb des Kontexts einer Transaktion ausgeführt werden.

## <a name="see-also"></a>Weitere Informationen

[Transaktionen](./transactions.md)
