---
description: 'Weitere Informationen finden Sie hier: JET_SETINFO Struktur'
title: JET_SETINFO Struktur
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531118"
---
# <a name="jet_setinfo-structure"></a><span data-ttu-id="ffcec-103">JET_SETINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="ffcec-103">JET_SETINFO Structure</span></span>


<span data-ttu-id="ffcec-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ffcec-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setinfo-structure"></a><span data-ttu-id="ffcec-105">JET_SETINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="ffcec-105">JET_SETINFO Structure</span></span>

<span data-ttu-id="ffcec-106">Die **JET_SETINFO** Struktur enthält optionale Eingabeparameter für [jetsetcolumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="ffcec-106">The **JET_SETINFO** structure contains optional input parameters for [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="ffcec-107">Ein **null** -Zeiger kann an die Stelle geleitet werden, an der ein Zeiger auf diese-Struktur andernfalls passieren würde.</span><span class="sxs-lookup"><span data-stu-id="ffcec-107">A **NULL** pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="ffcec-108">Die Übergabe eines **null** -Werts ist identisch mit dem übergeben von **JET_SETINFO** , wobei **cbStruct** auf sizeof (JET_SETINFO) festgelegt ist, **iblongvalue** auf 0 (null) und **itagsequence** auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ffcec-108">The meaning of passing a **NULL** is the same as passing **JET_SETINFO** with **cbStruct** set to sizeof(JET_SETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a><span data-ttu-id="ffcec-109">Member</span><span class="sxs-lookup"><span data-stu-id="ffcec-109">Members</span></span>

<span data-ttu-id="ffcec-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="ffcec-110">**cbStruct**</span></span>

<span data-ttu-id="ffcec-111">Die Größe (in Bytes) der **JET_SETINFO**.</span><span class="sxs-lookup"><span data-stu-id="ffcec-111">The size, in bytes, of the **JET_SETINFO**.</span></span> <span data-ttu-id="ffcec-112">Dieser Wert bestätigt, dass die folgenden Felder vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ffcec-112">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="ffcec-113">**iblongvalue**</span><span class="sxs-lookup"><span data-stu-id="ffcec-113">**ibLongValue**</span></span>

<span data-ttu-id="ffcec-114">Der Offset zum ersten Byte, der in einer Spalte vom Typ [JET_coltypLongBinary](./jet-coltyp.md) oder [JET_coltypLongText](./jet-coltyp.md)festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffcec-114">The offset to the first byte to be set in a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="ffcec-115">**itagsequence**</span><span class="sxs-lookup"><span data-stu-id="ffcec-115">**itagSequence**</span></span>

<span data-ttu-id="ffcec-116">Beschreibt die Sequenznummer des Werts in einer mehrwertigen Spalte, die festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffcec-116">Describes the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="ffcec-117">Das Array von Werten ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="ffcec-117">The array of values is one-based.</span></span> <span data-ttu-id="ffcec-118">Der erste Wert ist Sequenz 1, nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ffcec-118">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="ffcec-119">Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als **itagsequence** übergeben werden, wenn dieser Wert ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="ffcec-119">If the record column has only one value then 1 should be passed as the **itagSequence** if that value is being replaced.</span></span> <span data-ttu-id="ffcec-120">Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ffcec-120">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="ffcec-121">Bei einer Spalte, die mehrere Werte enthalten kann, ist es nur möglich, eine Sequenznummer größer als 1 in [jetsetcolumn](./jetsetcolumn-function.md) und [jetretrievecolumschlag](./jetretrievecolumn-function.md) oder 0 in [jetsetcolumn](./jetsetcolumn-function.md)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ffcec-121">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="ffcec-122">In der aktuellen Implementierung der Engine kann jede Spalte, die mit JET_bitColumnTagged erstellt wurde, mehrere Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="ffcec-122">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="ffcec-123">Spalten, die mit JET_bitColumnMultiValued erstellt werden, unterscheiden sich nur in der Art und Weise, in der Sie indiziert werden</span><span class="sxs-lookup"><span data-stu-id="ffcec-123">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="ffcec-124">Weitere Informationen finden Sie unter [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="ffcec-124">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

### <a name="requirements"></a><span data-ttu-id="ffcec-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffcec-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffcec-126"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ffcec-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ffcec-127">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ffcec-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffcec-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ffcec-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ffcec-129">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ffcec-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffcec-130"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ffcec-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ffcec-131">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ffcec-131">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ffcec-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ffcec-132">See Also</span></span>

[<span data-ttu-id="ffcec-133">Jetsetcolumn</span><span class="sxs-lookup"><span data-stu-id="ffcec-133">JetSetColumn</span></span>](./jetsetcolumn-function.md)
