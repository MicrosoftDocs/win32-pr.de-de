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
# <a name="adding-tables-to-the-database"></a><span data-ttu-id="83989-103">Hinzufügen von Tabellen zur Datenbank</span><span class="sxs-lookup"><span data-stu-id="83989-103">Adding Tables to the Database</span></span>


<span data-ttu-id="83989-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="83989-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="adding-tables-to-the-database"></a><span data-ttu-id="83989-105">Hinzufügen von Tabellen zur Datenbank</span><span class="sxs-lookup"><span data-stu-id="83989-105">Adding Tables to the Database</span></span>

<span data-ttu-id="83989-106">Tabellen sind eine heterogene Sammlung von Datensätzen, die die Daten in der Datenbank physisch und logisch gruppieren.</span><span class="sxs-lookup"><span data-stu-id="83989-106">Tables are a heterogeneous collection of records that physically and logically group the data in the database.</span></span> <span data-ttu-id="83989-107">Tabellen werden durch ihren Namen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="83989-107">Tables are uniquely identified by their name.</span></span> <span data-ttu-id="83989-108">Die Tabellen-ID ([JET_TABLEID](./jet-tableid.md)) ist ein Handle für einen Cursor, der zum Aktualisieren und Navigieren in Tabellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83989-108">The table ID ([JET_TABLEID](./jet-tableid.md)) is a handle to a cursor that is used to update and navigate tables.</span></span> <span data-ttu-id="83989-109">Sie können mehrere [JET_TABLEID](./jet-tableid.md) in derselben Tabelle öffnen.</span><span class="sxs-lookup"><span data-stu-id="83989-109">You may open multiple [JET_TABLEID](./jet-tableid.md) on the same table.</span></span>

<span data-ttu-id="83989-110">Eine vorhandene Tabelle wird im Aufruf von [jetopentable](./jetopentable-function.md)geöffnet, und es wird eine neue Tabelle ohne Zeilen oder Spalten mit [jetkreatetable](./jetcreatetable-function.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="83989-110">An existing table is opened in the call to [JetOpenTable](./jetopentable-function.md), and a new table is created without rows or columns with [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="83989-111">Zum atomischen Erstellen einer Tabelle mit einem anfänglichen Satz von Spalten und Indizes rufen Sie [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md) oder [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)auf.</span><span class="sxs-lookup"><span data-stu-id="83989-111">To atomically create a table with an initial set of columns and indices, call [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="83989-112">Die anfängliche Größe der Tabelle wird im *lpages* -Parameter in [jetupatetable](./jetcreatetable-function.md) oder im **ulpages** -Member der [JET_TABLECREATE](./jet-tablecreate-structure.md) Struktur im Aufruf von [jetkreatetablecolumnindex](./jetcreatetablecolumnindex-function.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="83989-112">The initial size of the table is given in the *lPages* parameter in [JetCreateTable](./jetcreatetable-function.md) or the **ulPages** member of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="83989-113">Tabellen werden automatisch vergrößert, wenn der Tabelle Daten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="83989-113">Tables grow automatically when data is added to the table.</span></span> <span data-ttu-id="83989-114">Das Wachstum ist proportional zur anfangs Größe der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="83989-114">The growth is proportional to the initial size of the table.</span></span> <span data-ttu-id="83989-115">Spalten können jederzeit mit [jetaddcolumn](./jetaddcolumn-function.md)der Tabelle hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="83989-115">Columns may be added to the table at any time with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="83989-116">Wenn die Anwendung nicht mehr auf die Tabelle zugreifen muss, kann der Cursor mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="83989-116">When the application no longer needs to access the table, the cursor can be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="83989-117">Die Tabelle kann durch einen Befehl von [jetdeletetable](./jetdeletetable-function.md)gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="83989-117">The table may be deleted via a call to [JetDeleteTable](./jetdeletetable-function.md).</span></span>

<span data-ttu-id="83989-118">Tabellen Vorgänge sollten innerhalb des Kontexts einer Transaktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="83989-118">Table operations should be performed within the context of a transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="83989-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83989-119">See Also</span></span>

[<span data-ttu-id="83989-120">Transaktionen</span><span class="sxs-lookup"><span data-stu-id="83989-120">Transactions</span></span>](./transactions.md)
