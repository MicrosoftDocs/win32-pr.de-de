---
description: 'Weitere Informationen finden Sie hier: JET_ENUMCOLUMNID Struktur'
title: JET_ENUMCOLUMNID Struktur
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526084"
---
# <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="46c56-103">JET_ENUMCOLUMNID Struktur</span><span class="sxs-lookup"><span data-stu-id="46c56-103">JET_ENUMCOLUMNID Structure</span></span>


<span data-ttu-id="46c56-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="46c56-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="46c56-105">JET_ENUMCOLUMNID Struktur</span><span class="sxs-lookup"><span data-stu-id="46c56-105">JET_ENUMCOLUMNID Structure</span></span>

<span data-ttu-id="46c56-106">Die **JET_ENUMCOLUMNID** -Struktur listet eine bestimmte Gruppe von Spalten und optional einen bestimmten Satz von Werten für diese Spalten auf, wenn die [jetenumeratecolumns](./jetenumeratecolumns-function.md) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46c56-106">The **JET_ENUMCOLUMNID** structure enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="46c56-107">[Jetenreeratecolenns](./jetenumeratecolumns-function.md) gibt ein Array von **JET_ENUMCOLUMNID** Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="46c56-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNID** structures.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a><span data-ttu-id="46c56-108">Member</span><span class="sxs-lookup"><span data-stu-id="46c56-108">Members</span></span>

<span data-ttu-id="46c56-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="46c56-109">**columnid**</span></span>

<span data-ttu-id="46c56-110">Die aufzuzählenden Spalten-ID.</span><span class="sxs-lookup"><span data-stu-id="46c56-110">The column ID to enumerate.</span></span>

<span data-ttu-id="46c56-111">Wenn die Spalten-ID 0 (null) ist, wird die Enumeration dieser Spalte übersprungen und ein entsprechender Slot im Ausgabe Array von [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) Strukturen mit dem Spalten Status JET_wrnColumnSkipped generiert.</span><span class="sxs-lookup"><span data-stu-id="46c56-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="46c56-112">**ctagsequence**</span><span class="sxs-lookup"><span data-stu-id="46c56-112">**ctagSequence**</span></span>

<span data-ttu-id="46c56-113">Identifiziert optional ein Array von Spaltenwerten (durch einen 1-basierten Index), die für die angegebene Spalten-ID aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="46c56-113">Optionally identifies an array of column values (by one-based index) to enumerate for the specified column ID.</span></span>

<span data-ttu-id="46c56-114">Wenn **ctagsequence** gleich 0 (null) ist, wird **rgtagsequence** ignoriert, und alle Spaltenwerte für die angegebene Spalten-ID werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="46c56-114">If **ctagSequence** is 0 (zero) then **rgtagSequence** is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="46c56-115">Wenn ein Element von **rgtagsequence** gleich 0 (null) ist, wird die Enumeration dieses Spaltenwerts (durch einen einbasierten Index) übersprungen.</span><span class="sxs-lookup"><span data-stu-id="46c56-115">If an element of **rgtagSequence** is 0 (zero), then the enumeration of that column value (by one-based index) will be skipped.</span></span> <span data-ttu-id="46c56-116">Ein entsprechender Slot im Ausgabe Array der **JET_ENUMCOLUMNID** Struktur wird mit einem Spalten Statuswert JET_wrnColumnSkipped generiert.</span><span class="sxs-lookup"><span data-stu-id="46c56-116">A corresponding slot in the output array of the **JET_ENUMCOLUMNID** structure will be generated with a column status value of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="46c56-117">**rgtagsequence**</span><span class="sxs-lookup"><span data-stu-id="46c56-117">**rgtagSequence**</span></span>

<span data-ttu-id="46c56-118">Ein Array von einbasierten Indizes in das Array von Spaltenwerten für eine angegebene Spalte.</span><span class="sxs-lookup"><span data-stu-id="46c56-118">An array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="46c56-119">Bei einem einzelnen Element handelt es sich um eine in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)definierte **itagsequence** .</span><span class="sxs-lookup"><span data-stu-id="46c56-119">A single element is an **itagSequence** which is defined in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="46c56-120">Eine **itagsequence** -Wert von 0 (null) bedeutet "Skip".</span><span class="sxs-lookup"><span data-stu-id="46c56-120">An **itagSequence** of 0 (zero) means "skip".</span></span> <span data-ttu-id="46c56-121">Eine **itagsequence** von 1 bedeutet, dass der erste Spaltenwert der Spalte zurückgegeben wird, der Wert 2 für den zweiten Wert usw.</span><span class="sxs-lookup"><span data-stu-id="46c56-121">An **itagSequence** of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

### <a name="requirements"></a><span data-ttu-id="46c56-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46c56-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46c56-123"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="46c56-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="46c56-124">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="46c56-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46c56-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="46c56-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="46c56-126">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="46c56-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46c56-127"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="46c56-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="46c56-128">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="46c56-128">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="46c56-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="46c56-129">See Also</span></span>

[<span data-ttu-id="46c56-130">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="46c56-130">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="46c56-131">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="46c56-131">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="46c56-132">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="46c56-132">JET_ENUMCOLUMNID</span></span>]()  
[<span data-ttu-id="46c56-133">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="46c56-133">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="46c56-134">Jetenreeratecolumschlag</span><span class="sxs-lookup"><span data-stu-id="46c56-134">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
