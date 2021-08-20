---
description: Weitere Informationen finden Sie unter ESE-Handles.
title: ESE-Handles
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5177de8b7fbc07d592bb599941a1fd02810bbbf81e16b65cd15c6ebdfd75d3d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786295"
---
# <a name="ese-handles"></a>ESE-Handles


_**Gilt für:** Windows | Windows Server_

## <a name="ese-handles"></a>ESE-Handles

ESE-Handles werden verwendet, um Sitzungen zu erstellen und auf Datenbanken zu zugreifen. Sie werden in einer Hierarchie verwaltet, was bedeutet, dass die Ausgabe einer Ebene für den Zugriff auf Ressourcen auf der nächsten Ebene verwendet wird.

Das folgende Diagramm zeigt die Hierarchie von Handles und die entsprechenden Funktionen, die die Handles erstellen. Zusammen mit den Funktionen werden auch die Handles angegeben, die im Aufruf zum Erstellen des neuen Handles verwendet werden.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Wie im Diagramm dargestellt, ist die -Instanz das Stammhand handle und die Ebene, auf der die Datenbank im Falle einer unerwarteten Beendigung des Prozesses oder des Herunterfahrens des Systems wiederhergestellt wird. Das Instanzhandl JET_INSTANCE wird von [JetCreateInstance](./jetcreateinstance-function.md) und [JetCreateInstance2 erstellt.](./jetcreateinstance2-function.md) Die nächste Ebene, die Sitzungsebene, ist der Transaktionskontext der Datenbank-Engine und die Ebene, unter der alle Datenbankvorgänge ausgeführt werden. Das Sitzungshand JET_SESID wird im Kontext der -Instanz im Aufruf von [JetBeginSession erstellt.](./jetbeginsession-function.md) Die Sitzungs-ID wird in allen nachfolgenden Aufrufen für den Zugriff auf Tabellen und Datenbanken verwendet. Wenn die Instanz von mehr als einem Thread gleichzeitig verwendet wird, muss jeder Thread sein eigenes Sitzungshand handle verwenden. Das Datenbankhand handle wird mithilfe des Sitzungshandpunkts erstellt und hauptsächlich zum Verwalten des Schemas der Datenbank verwendet, kann aber auch zum Verwalten von Tabellen innerhalb der Datenbank verwendet werden. Datenbankhandles können nur in der Sitzung verwendet werden, in der sie erstellt werden. Das Handle für die Datenbank wird im Aufruf von [JetCreateDatabase](./jetcreatedatabase-function.md) oder [JetOpenDatabase erstellt.](./jetopendatabase-function.md) Tabellen werden der Datenbank-ID zugeordnet, unter der sie erstellt werden.

Der JET_TABLEID Datentyp enthält ein Handle für einen Datenbankcursor. Es wird verwendet, um Datensätze zu überprüfen, Datensätze zu durchsuchen oder Aktualisierungs- und Löschdatensätze zu erstellen. Das Tabellenhandl wird im Aufruf von [JetOpenTable](./jetopentable-function.md)oder [JetCreateTable erstellt.](./jetcreatetable-function.md) [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)und [JetOpenTempTable3](./jetopentemptable3-function.md) erstellen auch Tabellen-IDs für temporäre Tabellen, und [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) und [JetCreateTableColumnIndex2 geben](./jetcreatetablecolumnindex2-function.md) Tabellen-IDs in der out-Struktur zurück. Die in der Tabelle erstellten Spalten verfügen jeweils über einen eindeutigen Spaltenbezeichner COLUMN_ID. Die Spalten-IDs werden in den Aufrufen von [JetAddColumn](./jetaddcolumn-function.md)oder in Aufrufen von [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)oder [JetOpenTempTable3](./jetopentemptable3-function.md) für temporäre Tabellen erstellt. Spalten-IDs können auch für eine bestimmte Spalte nach Namen mit APIs wie [JetGetTableColumnInfo abgerufen werden.](./jetgettablecolumninfo-function.md)
