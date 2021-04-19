---
description: 'Weitere Informationen finden Sie unter: Lesen von Daten aus der Datenbank'
title: Lesen von Daten aus der Datenbank
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362519"
---
# <a name="reading-data-from-the-database"></a>Lesen von Daten aus der Datenbank


_**Gilt für:** Windows | Windows Server_

## <a name="reading-data-from-the-database"></a>Lesen von Daten aus der Datenbank

Das Lesen von Daten aus der Datenbank sollte innerhalb einer Transaktion erfolgen.

Im folgenden Verfahren wird gezeigt, wie ein einfacher Lesevorgang in der-Datenbank durchgeführt wird.

### <a name="to-read-data-from-a-database"></a>So lesen Sie Daten aus einer Datenbank

1.  Aufrufen von [jetbegintransaction](./jetbegintransaction-function.md) oder [JetBeginTransaction2](./jetbegintransaction2-function.md) mit der Sitzungs-ID, um die Transaktion zu starten.

2.  Bewegen Sie den Cursor in den gewünschten Datensatz, indem Sie [jetmove](./jetmove-function.md) mit JET_MoveFirst im Parameter " *cRow* " aufrufen. Weitere Informationen zum Verschieben des Cursors finden Sie im Thema [Indizierung in der Tabelle](./indexing-in-the-table.md) .

3.  Rufen Sie [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) für den aktuellen Datensatz mit JET_ColInfo im *infolevel* -Parameter fest, um die Spalten-ID für die Spalte abzurufen. Die Spalten-ID wird in der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur zurückgegeben.

4.  Lesen Sie die Daten aus der Spalte, indem Sie [jetretrievecolumschlag](./jetretrievecolumn-function.md) mit der in Schritt 3 im columnid-Parameter abgerufenen Spalten-ID aufrufen. Der *pvData* -Parameter enthält den Typ der Daten, die in der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur angegeben sind, die in Schritt 3 abgerufen wurde.

5.  Ruft [jetcommittransaction](./jetcommittransaction-function.md) auf, um die Transaktion an die Datenbank zu übergeben.
