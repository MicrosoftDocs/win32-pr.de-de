---
description: 'Weitere Informationen finden Sie hier: JET_RECORDLIST Struktur'
title: JET_RECORDLIST Struktur
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868372"
---
# <a name="jet_recordlist-structure"></a><span data-ttu-id="c912e-103">JET_RECORDLIST Struktur</span><span class="sxs-lookup"><span data-stu-id="c912e-103">JET_RECORDLIST Structure</span></span>


<span data-ttu-id="c912e-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c912e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recordlist-structure"></a><span data-ttu-id="c912e-105">JET_RECORDLIST Struktur</span><span class="sxs-lookup"><span data-stu-id="c912e-105">JET_RECORDLIST Structure</span></span>

<span data-ttu-id="c912e-106">Die **JET_RECORDLIST** -Struktur findet Datensätze, die sich in der Schnittmenge der angegebenen Index Bereiche befinden, wenn Sie mit der [jetintersectindexes](./jetintersectindexes-function.md) -Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c912e-106">The **JET_RECORDLIST** structure finds records that are in the intersection of specified index ranges when they are used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a><span data-ttu-id="c912e-107">Member</span><span class="sxs-lookup"><span data-stu-id="c912e-107">Members</span></span>

<span data-ttu-id="c912e-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="c912e-108">**cbStruct**</span></span>

<span data-ttu-id="c912e-109">Die Größe der **JET_RECORDLIST** Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="c912e-109">The size of the **JET_RECORDLIST** structure, in bytes.</span></span>

<span data-ttu-id="c912e-110">**TableID**</span><span class="sxs-lookup"><span data-stu-id="c912e-110">**tableid**</span></span>

<span data-ttu-id="c912e-111">Der Tabellen Bezeichner einer temporären Tabelle, die die Lesezeichen für die Ergebnisse der Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="c912e-111">The table identifier of a temporary table that contains the bookmarks for the results of the query.</span></span> <span data-ttu-id="c912e-112">Die Tabelle wird automatisch geschlossen, wenn für die aktuelle Transaktion ein Rollback mit [jetrollback](./jetrollback-function.md)durchgeführt wird. Andernfalls muss Sie mit [jetclosetable](./jetclosetable-function.md)geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c912e-112">The table will automatically be closed if the current transaction is rolled back with [JetRollback](./jetrollback-function.md); otherwise, it must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="c912e-113">**crecord**</span><span class="sxs-lookup"><span data-stu-id="c912e-113">**cRecord**</span></span>

<span data-ttu-id="c912e-114">Die Anzahl der Zeilen in der temporären Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c912e-114">The number of rows in the temporary table.</span></span>

<span data-ttu-id="c912e-115">**columnidbookmark**</span><span class="sxs-lookup"><span data-stu-id="c912e-115">**columnidBookmark**</span></span>

<span data-ttu-id="c912e-116">Der Spalten Bezeichner der Lesezeichen Spalte in der temporären Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c912e-116">The column identifier of the bookmark column in the temporary table.</span></span>

### <a name="remarks"></a><span data-ttu-id="c912e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c912e-117">Remarks</span></span>

<span data-ttu-id="c912e-118">Die temporäre Tabelle, die von **TableID** identifiziert wird, verfügt über eine einzelne Spalte.</span><span class="sxs-lookup"><span data-stu-id="c912e-118">The temporary table that is identified by **tableid** has a single column.</span></span> <span data-ttu-id="c912e-119">Diese einzelne Spalte enthält Lesezeichen, und jeder Datensatz sollte in einen Puffer der Größe JET_cbBookmarkMost Bytes passen.</span><span class="sxs-lookup"><span data-stu-id="c912e-119">That single column holds bookmarks, and each record should fit in a buffer of size JET_cbBookmarkMost bytes.</span></span>

### <a name="requirements"></a><span data-ttu-id="c912e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c912e-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c912e-121"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c912e-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c912e-122">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c912e-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c912e-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c912e-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c912e-124">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c912e-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c912e-125"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c912e-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c912e-126">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="c912e-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c912e-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c912e-127">See Also</span></span>

[<span data-ttu-id="c912e-128">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="c912e-128">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="c912e-129">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c912e-129">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c912e-130">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c912e-130">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c912e-131">Jetclosetable</span><span class="sxs-lookup"><span data-stu-id="c912e-131">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="c912e-132">Jetintersectindexes</span><span class="sxs-lookup"><span data-stu-id="c912e-132">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="c912e-133">Jetrollback</span><span class="sxs-lookup"><span data-stu-id="c912e-133">JetRollback</span></span>](./jetrollback-function.md)
