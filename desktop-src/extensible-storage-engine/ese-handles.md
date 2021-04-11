---
description: 'Weitere Informationen zu: ESE-Handles'
title: ESE-Handles
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cc91a4586fc1619c55b5f45afbca39ce04c0c6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217732"
---
# <a name="ese-handles"></a>ESE-Handles


_**Gilt für:** Windows | Windows Server_

## <a name="ese-handles"></a>ESE-Handles

ESE-Handles werden zum Erstellen von Sitzungen und zum Zugreifen auf Datenbanken verwendet. Sie werden in einer Hierarchie verwaltet, was bedeutet, dass die Ausgabe einer Ebene verwendet wird, um auf Ressourcen auf der nächsten Ebene zuzugreifen.

Das Diagramm zeigt die Hierarchie von Handles und die entsprechenden Funktionen, die die Handles erstellen. Außerdem werden zusammen mit den-Funktionen die Handles angegeben, die im-Befehl zum Erstellen des neuen Handles verwendet werden.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Wie im Diagramm dargestellt, ist die Instanz das Stamm Handle und die Ebene, bei der die Datenbank im Fall einer unerwarteten Beendigung des Prozesses oder des herunter Fahrens des Systems wieder hergestellt wird. Der Instanzhandle, JET_INSTANCE, wird von [jetkreateinstance](./jetcreateinstance-function.md) und [JetCreateInstance2](./jetcreateinstance2-function.md)erstellt. Die nächste Ebene, die Sitzungs Ebene, ist der Transaktionskontext der Datenbank-Engine und der Ebene, unter der alle Daten Bank Vorgänge ausgeführt werden. Das Sitzungs handle, JET_SESID, wird im Kontext der-Instanz im Aufrufen von [jetbeginsession](./jetbeginsession-function.md)erstellt. Die Sitzungs-ID wird bei allen nachfolgenden Aufrufen von für den Zugriff auf Tabellen und Datenbanken verwendet. Wenn die Instanz von mehr als einem Thread gleichzeitig verwendet wird, muss jeder Thread sein eigenes Sitzungs Handle verwenden. Das Daten Bank Handle wird mithilfe des Sitzungs Handles erstellt und hauptsächlich zum Verwalten des Schemas der Datenbank verwendet. es kann jedoch auch zum Verwalten von Tabellen in der Datenbank verwendet werden. Daten Bank Handles können nur in der Sitzung verwendet werden, in der Sie erstellt werden. Das Handle für die Datenbank wird im Aufrufen von [jetkreatedatabase](./jetcreatedatabase-function.md) oder [jetopd](./jetopendatabase-function.md)erstellt. Tabellen werden mit der Datenbank-ID verknüpft, unter der Sie erstellt werden.

Der JET_TABLEID-Datentyp enthält ein Handle für einen Daten Bank Cursor. Sie wird verwendet, um Datensätze zu scannen, Datensätze zu suchen oder Datensätze zu aktualisieren und zu löschen. Das Tabellen Handle wird im Aufruf von [jetopentable](./jetopentable-function.md)oder [jetkreatetable](./jetcreatetable-function.md)erstellt. [Jetopentemptable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)und [JetOpenTempTable3](./jetopentemptable3-function.md) erstellen außerdem Tabellen-IDs für temporäre Tabellen, und [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) und [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) geben Tabellen-IDs in der out-Struktur zurück. Die in der Tabelle erstellten Spalten verfügen jeweils über einen eindeutigen Spalten Bezeichner oder column_id. Die Spalten-IDs werden in den Aufrufen von [jetaddcolumn](./jetaddcolumn-function.md)oder in Aufrufen von [jetopkotemptable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)oder [JetOpenTempTable3](./jetopentemptable3-function.md) für temporäre Tabellen erstellt. Spalten-IDs können auch für eine bestimmte Spalte nach Namen mit APIs wie [jetgettablecolumninfo](./jetgettablecolumninfo-function.md)abgerufen werden.
