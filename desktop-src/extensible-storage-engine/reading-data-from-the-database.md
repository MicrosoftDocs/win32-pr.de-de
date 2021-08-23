---
description: Weitere Informationen finden Sie unter Lesen von Daten aus der Datenbank.
title: Lesen von Daten aus der Datenbank
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7d33aa2640c07018186a5516d985fd4e46194d39cd4b12b7254f430f889e2484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780260"
---
# <a name="reading-data-from-the-database"></a>Lesen von Daten aus der Datenbank


_**Gilt für:** Windows | Windows Server_

## <a name="reading-data-from-the-database"></a>Lesen von Daten aus der Datenbank

Das Lesen von Daten aus der Datenbank sollte innerhalb einer Transaktion erfolgen.

Das folgende Verfahren zeigt, wie Sie einen einfachen Lesevorgang in der Datenbank ausführen.

### <a name="to-read-data-from-a-database"></a>So lesen Sie Daten aus einer Datenbank

1.  Rufen [Sie JetBeginTransaction](./jetbegintransaction-function.md) oder [JetBeginTransaction2](./jetbegintransaction2-function.md) mit der Sitzungs-ID auf, um die Transaktion zu starten.

2.  Bewegen Sie den Cursor in den gewünschten Datensatz, indem Sie [JetMove](./jetmove-function.md) mit JET_MoveFirst im *cRow-Parameter* aufrufen. Weitere Informationen zum Verschieben des Cursors finden Sie im Thema [Indizierung im Thema](./indexing-in-the-table.md) Tabelle.

3.  Rufen [Sie JetGetTableColumnInfo für](./jetgettablecolumninfo-function.md) den aktuellen Datensatz auf, JET_ColInfo im *InfoLevel-Parameter* angegeben ist, um die Spalten-ID für die Spalte abzurufen. Die Spalten-ID wird in der [JET_COLUMNDEF](./jet-columndef-structure.md) zurückgegeben.

4.  Lesen Sie die Daten aus der Spalte, indem [Sie JetRetrivorColumn](./jetretrievecolumn-function.md) mit der in Schritt 3 abgerufenen Spalten-ID im columnid-Parameter aufrufen. Der *parameter pvData* enthält den Datentyp, der in der in Schritt 3 abgerufenen JET_COLUMNDEF angegeben ist. [](./jet-columndef-structure.md)

5.  Rufen [Sie JetCommitTransaction auf,](./jetcommittransaction-function.md) um die Transaktion in die Datenbank zu übertragen.
