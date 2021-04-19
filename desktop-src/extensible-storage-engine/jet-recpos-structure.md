---
description: 'Weitere Informationen finden Sie hier: JET_RECPOS Struktur'
title: JET_RECPOS Struktur
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364081"
---
# <a name="jet_recpos-structure"></a><span data-ttu-id="d0d37-103">JET_RECPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="d0d37-103">JET_RECPOS Structure</span></span>


<span data-ttu-id="d0d37-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d0d37-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recpos-structure"></a><span data-ttu-id="d0d37-105">JET_RECPOS Struktur</span><span class="sxs-lookup"><span data-stu-id="d0d37-105">JET_RECPOS Structure</span></span>

<span data-ttu-id="d0d37-106">Die **JET_RECPOS** -Struktur enthält eine Auflistung von ganzen Zahlen, die eine Bruch Position innerhalb eines Indexes darstellen.</span><span class="sxs-lookup"><span data-stu-id="d0d37-106">The **JET_RECPOS** structure contains a collection of integers that represent a fractional position within an index.</span></span> <span data-ttu-id="d0d37-107">**centrieslt** ist die Anzahl der Indexeinträge, die kleiner sind als der aktuelle Index Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d0d37-107">**centriesLT** is the number of index entries less than the current index key.</span></span> <span data-ttu-id="d0d37-108">**centriesinrange** ist die Anzahl der Indexeinträge, die dem aktuellen Schlüssel entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d0d37-108">**centriesInRange** is the number of index entries equal to the current key.</span></span> <span data-ttu-id="d0d37-109">**centriesinrange** wird nicht unterstützt und wird immer als 1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d0d37-109">**centriesInRange** is not supported and is always returned as 1.</span></span> <span data-ttu-id="d0d37-110">" **zentriestotal** " ist die Anzahl der Indexeinträge im Index.</span><span class="sxs-lookup"><span data-stu-id="d0d37-110">**centriesTotal** is the number of index entries in the index.</span></span> <span data-ttu-id="d0d37-111">Alle Werte sind Näherungen, ohne die Genauigkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="d0d37-111">All values are approximations with no guarantee of accuracy.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a><span data-ttu-id="d0d37-112">Member</span><span class="sxs-lookup"><span data-stu-id="d0d37-112">Members</span></span>

<span data-ttu-id="d0d37-113">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d0d37-113">**cbStruct**</span></span>

<span data-ttu-id="d0d37-114">Die Größe der [JET_RETINFO](./jet-retinfo-structure.md) Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d0d37-114">The size of the [JET_RETINFO](./jet-retinfo-structure.md) structure, in bytes.</span></span> <span data-ttu-id="d0d37-115">Dieser Wert bestätigt, dass die folgenden Felder vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d0d37-115">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="d0d37-116">**centrieslt**</span><span class="sxs-lookup"><span data-stu-id="d0d37-116">**centriesLT**</span></span>

<span data-ttu-id="d0d37-117">Die ungefähre Anzahl der Indexeinträge, die kleiner als der aktuelle Schlüssel sind.</span><span class="sxs-lookup"><span data-stu-id="d0d37-117">The approximate number of index entries less than the current key.</span></span>

<span data-ttu-id="d0d37-118">**centriesinrange**</span><span class="sxs-lookup"><span data-stu-id="d0d37-118">**centriesInRange**</span></span>

<span data-ttu-id="d0d37-119">Die ungefähre Anzahl der Indexeinträge, die dem aktuellen Schlüssel entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d0d37-119">The approximate number of index entries equal to the current key.</span></span> <span data-ttu-id="d0d37-120">Dieses Feld wird immer auf 1 festgelegt, unabhängig von der Anzahl der Indexeinträge, die tatsächlich dem aktuellen Schlüssel entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d0d37-120">This field is always set to 1, regardless of the number of index entries that are actually equal to the current key.</span></span>

<span data-ttu-id="d0d37-121">**zentriestotal**</span><span class="sxs-lookup"><span data-stu-id="d0d37-121">**centriesTotal**</span></span>

<span data-ttu-id="d0d37-122">Die ungefähre Anzahl von Einträgen im Index.</span><span class="sxs-lookup"><span data-stu-id="d0d37-122">The approximate number of entries in the index.</span></span>

### <a name="requirements"></a><span data-ttu-id="d0d37-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0d37-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0d37-124"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d0d37-124"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d37-125">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d0d37-125">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0d37-126"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d0d37-126"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d37-127">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d0d37-127">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0d37-128"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d0d37-128"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d0d37-129">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="d0d37-129">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d0d37-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0d37-130">See Also</span></span>

[<span data-ttu-id="d0d37-131">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="d0d37-131">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="d0d37-132">Jetgetrecordposition</span><span class="sxs-lookup"><span data-stu-id="d0d37-132">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)
