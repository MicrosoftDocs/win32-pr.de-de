---
description: 'Weitere Informationen finden Sie hier: JET_RETINFO Struktur'
title: JET_RETINFO Struktur
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862967"
---
# <a name="jet_retinfo-structure"></a><span data-ttu-id="bedc6-103">JET_RETINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="bedc6-103">JET_RETINFO Structure</span></span>


<span data-ttu-id="bedc6-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bedc6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retinfo-structure"></a><span data-ttu-id="bedc6-105">JET_RETINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="bedc6-105">JET_RETINFO Structure</span></span>

<span data-ttu-id="bedc6-106">Die **JET_RETINFO** Struktur enthält optionale Eingabe-und Ausgabeparameter für [jetretrievecolumschlag](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="bedc6-106">The **JET_RETINFO** structure contains optional input and output parameters for [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span> <span data-ttu-id="bedc6-107">Ein NULL-Zeiger kann an die Stelle geleitet werden, an der ein Zeiger auf diese-Struktur andernfalls passieren würde.</span><span class="sxs-lookup"><span data-stu-id="bedc6-107">A null pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="bedc6-108">Das Übergeben eines NULL-Zeigers ist identisch mit dem übergeben von **JET_RETINFO** , wobei **cbStruct** auf sizeof (JET_RETINFO) festgelegt ist, **iblongvalue** auf 0 (null) und **itagsequence** auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bedc6-108">Passing a null pointer is the same as passing **JET_RETINFO** with **cbStruct** set to sizeof(JET_RETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a><span data-ttu-id="bedc6-109">Member</span><span class="sxs-lookup"><span data-stu-id="bedc6-109">Members</span></span>

<span data-ttu-id="bedc6-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="bedc6-110">**cbStruct**</span></span>

<span data-ttu-id="bedc6-111">Muss auf die Größe der **JET_RETINFO** Struktur in Bytes festgelegt werden und stellt sicher, dass die folgenden Felder vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bedc6-111">Must be set to the size of the **JET_RETINFO** structure, in bytes, and serves to confirm the presence of the following fields.</span></span>

<span data-ttu-id="bedc6-112">**iblongvalue**</span><span class="sxs-lookup"><span data-stu-id="bedc6-112">**ibLongValue**</span></span>

<span data-ttu-id="bedc6-113">Der Offset zum ersten Byte, der aus einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md)abgerufen werden soll, oder [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="bedc6-113">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span> <span data-ttu-id="bedc6-114">Beachten Sie, dass die Menge der Daten, die von diesem Offset abgerufen werden, die geringere Größe des Ausgabepuffers und die Größe der Daten im tatsächlichen Wert nach diesem Offset ist.</span><span class="sxs-lookup"><span data-stu-id="bedc6-114">Note that the amount of data retrieved from this offset is the lower of the size of the output buffer and the size of data in the actual value after this offset.</span></span>

<span data-ttu-id="bedc6-115">**itagsequence**</span><span class="sxs-lookup"><span data-stu-id="bedc6-115">**itagSequence**</span></span>

<span data-ttu-id="bedc6-116">Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="bedc6-116">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="bedc6-117">Beachten Sie, dass das Array von Werten einbasiert ist.</span><span class="sxs-lookup"><span data-stu-id="bedc6-117">Note that the array of values is one-based.</span></span> <span data-ttu-id="bedc6-118">Der erste Wert ist Sequenz 1, nicht 0.</span><span class="sxs-lookup"><span data-stu-id="bedc6-118">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="bedc6-119">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als **itagsequence** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="bedc6-119">If the record column has only one value then 1 should be passed as the **itagSequence**</span></span>

<span data-ttu-id="bedc6-120">Bei einer Spalte, die mehrere Werte enthalten kann, ist es nur möglich, eine Sequenznummer größer als 1 in [jetsetcolumn](./jetsetcolumn-function.md) und [jetretrievecolumschlag](./jetretrievecolumn-function.md) oder 0 in [jetsetcolumn](./jetsetcolumn-function.md)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bedc6-120">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="bedc6-121">In der aktuellen Implementierung der Engine kann jede Spalte, die mit JET_bitColumnTagged erstellt wurde, mehrere Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="bedc6-121">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="bedc6-122">Spalten, die mit JET_bitColumnMultiValued erstellt werden, unterscheiden sich nur in der Art und Weise, in der Sie indiziert werden</span><span class="sxs-lookup"><span data-stu-id="bedc6-122">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="bedc6-123">Weitere Informationen finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="bedc6-123">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

<span data-ttu-id="bedc6-124">**columnidnexttaging**</span><span class="sxs-lookup"><span data-stu-id="bedc6-124">**columnidNextTagged**</span></span>

<span data-ttu-id="bedc6-125">Gibt das ColumnID der abgerufenen Spalte mit mehreren Werten oder geringer Dichte zurück, wenn alle markierten Spalten abgerufen werden, indem 0 als ColumnID an [jetretrievecolbin](./jetretrievecolumn-function.md)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bedc6-125">Returns the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="bedc6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bedc6-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bedc6-127"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bedc6-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bedc6-128">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bedc6-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bedc6-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bedc6-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bedc6-130">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bedc6-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bedc6-131"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bedc6-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bedc6-132">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="bedc6-132">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bedc6-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bedc6-133">See Also</span></span>

[<span data-ttu-id="bedc6-134">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="bedc6-134">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="bedc6-135">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="bedc6-135">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="bedc6-136">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="bedc6-136">JET_RETINFO</span></span>]()  
[<span data-ttu-id="bedc6-137">Jetretrievecolumschlag</span><span class="sxs-lookup"><span data-stu-id="bedc6-137">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)
