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
# <a name="reading-data-from-the-database"></a><span data-ttu-id="a5a5d-103">Lesen von Daten aus der Datenbank</span><span class="sxs-lookup"><span data-stu-id="a5a5d-103">Reading Data from the Database</span></span>


<span data-ttu-id="a5a5d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a5a5d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="reading-data-from-the-database"></a><span data-ttu-id="a5a5d-105">Lesen von Daten aus der Datenbank</span><span class="sxs-lookup"><span data-stu-id="a5a5d-105">Reading Data from the Database</span></span>

<span data-ttu-id="a5a5d-106">Das Lesen von Daten aus der Datenbank sollte innerhalb einer Transaktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-106">Reading data from the database should be performed within a transaction.</span></span>

<span data-ttu-id="a5a5d-107">Im folgenden Verfahren wird gezeigt, wie ein einfacher Lesevorgang in der-Datenbank durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-107">The following procedure shows how to perform a simple read operation in the database.</span></span>

### <a name="to-read-data-from-a-database"></a><span data-ttu-id="a5a5d-108">So lesen Sie Daten aus einer Datenbank</span><span class="sxs-lookup"><span data-stu-id="a5a5d-108">To read data from a database</span></span>

1.  <span data-ttu-id="a5a5d-109">Aufrufen von [jetbegintransaction](./jetbegintransaction-function.md) oder [JetBeginTransaction2](./jetbegintransaction2-function.md) mit der Sitzungs-ID, um die Transaktion zu starten.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-109">Call [JetBeginTransaction](./jetbegintransaction-function.md) or [JetBeginTransaction2](./jetbegintransaction2-function.md) with the session ID to start the transaction.</span></span>

2.  <span data-ttu-id="a5a5d-110">Bewegen Sie den Cursor in den gewünschten Datensatz, indem Sie [jetmove](./jetmove-function.md) mit JET_MoveFirst im Parameter " *cRow* " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-110">Move the cursor to the desired record by calling [JetMove](./jetmove-function.md) with JET_MoveFirst in the *cRow* parameter.</span></span> <span data-ttu-id="a5a5d-111">Weitere Informationen zum Verschieben des Cursors finden Sie im Thema [Indizierung in der Tabelle](./indexing-in-the-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a5a5d-111">For more information on how to move the cursor, see the [Indexing in the Table](./indexing-in-the-table.md) topic.</span></span>

3.  <span data-ttu-id="a5a5d-112">Rufen Sie [jetgettablecolumninfo](./jetgettablecolumninfo-function.md) für den aktuellen Datensatz mit JET_ColInfo im *infolevel* -Parameter fest, um die Spalten-ID für die Spalte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-112">Call [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) on the current record with JET_ColInfo specified in the *InfoLevel* parameter to retrieve the column ID for the column.</span></span> <span data-ttu-id="a5a5d-113">Die Spalten-ID wird in der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-113">The column ID is returned in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>

4.  <span data-ttu-id="a5a5d-114">Lesen Sie die Daten aus der Spalte, indem Sie [jetretrievecolumschlag](./jetretrievecolumn-function.md) mit der in Schritt 3 im columnid-Parameter abgerufenen Spalten-ID aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-114">Read the data from the column by calling [JetRetrieveColumn](./jetretrievecolumn-function.md) with the column ID retrieved in step 3 in the columnid parameter.</span></span> <span data-ttu-id="a5a5d-115">Der *pvData* -Parameter enthält den Typ der Daten, die in der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur angegeben sind, die in Schritt 3 abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-115">The *pvData* parameter contains the type of data specified in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure retrieved in step 3.</span></span>

5.  <span data-ttu-id="a5a5d-116">Ruft [jetcommittransaction](./jetcommittransaction-function.md) auf, um die Transaktion an die Datenbank zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a5a5d-116">Call [JetCommitTransaction](./jetcommittransaction-function.md) to commit the transaction to the database.</span></span>
