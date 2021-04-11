---
description: 'Weitere Informationen finden Sie hier: JET_BKINFO Struktur'
title: JET_BKINFO Struktur
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217870"
---
# <a name="jet_bkinfo-structure"></a><span data-ttu-id="3860d-103">JET_BKINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="3860d-103">JET_BKINFO Structure</span></span>


<span data-ttu-id="3860d-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="3860d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bkinfo-structure"></a><span data-ttu-id="3860d-105">JET_BKINFO Struktur</span><span class="sxs-lookup"><span data-stu-id="3860d-105">JET_BKINFO Structure</span></span>

<span data-ttu-id="3860d-106">Die **JET_BKINFO** -Struktur enthält eine Sammlung von Daten zu einem bestimmten Sicherungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="3860d-106">The **JET_BKINFO** structure holds a collection of data about a specific backup event.</span></span>

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a><span data-ttu-id="3860d-107">Member</span><span class="sxs-lookup"><span data-stu-id="3860d-107">Members</span></span>

<span data-ttu-id="3860d-108">**lgposmark**</span><span class="sxs-lookup"><span data-stu-id="3860d-108">**lgposMark**</span></span>

<span data-ttu-id="3860d-109">Die ID dieser Sicherung.</span><span class="sxs-lookup"><span data-stu-id="3860d-109">The ID of this backup.</span></span>

<span data-ttu-id="3860d-110">**logtimemark**</span><span class="sxs-lookup"><span data-stu-id="3860d-110">**logtimeMark**</span></span>

<span data-ttu-id="3860d-111">Der Zeitpunkt dieses Sicherungs Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="3860d-111">The time of this backup event.</span></span>

<span data-ttu-id="3860d-112">**bklogtimemark**</span><span class="sxs-lookup"><span data-stu-id="3860d-112">**bklogtimeMark**</span></span>

<span data-ttu-id="3860d-113">Die Zeit dieses Sicherungs Ereignisses mit zusätzlichen Bits, die auf eine Momentaufnahme Sicherung hindeuten.</span><span class="sxs-lookup"><span data-stu-id="3860d-113">The time of this backup event, with additional bits to indicate a snapshot backup.</span></span>

<span data-ttu-id="3860d-114">**Windows Vista: bklogtimemark** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3860d-114">**Windows Vista:  bklogtimeMark** is introduced in Windows Vista.</span></span>

<span data-ttu-id="3860d-115">**genlow**</span><span class="sxs-lookup"><span data-stu-id="3860d-115">**genLow**</span></span>

<span data-ttu-id="3860d-116">Die niedrige Protokoll Generierungs Nummer, die diesem Sicherungs Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3860d-116">The low log generation number associated with this backup event.</span></span>

<span data-ttu-id="3860d-117">**genhoch**</span><span class="sxs-lookup"><span data-stu-id="3860d-117">**genHigh**</span></span>

<span data-ttu-id="3860d-118">Die hohe Protokoll Generierungs Nummer, die diesem Sicherungs Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3860d-118">The high log generation number associated with this backup event.</span></span>

### <a name="remarks"></a><span data-ttu-id="3860d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3860d-119">Remarks</span></span>

<span data-ttu-id="3860d-120">Diese Struktur wird in der [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) -Struktur verwendet, um Daten zum Daten Bank Sicherungs Ereignis darzustellen.</span><span class="sxs-lookup"><span data-stu-id="3860d-120">This structure is used inside the [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) structure to represent data about the database backup event.</span></span>

### <a name="requirements"></a><span data-ttu-id="3860d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3860d-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3860d-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3860d-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3860d-123">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="3860d-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3860d-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="3860d-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3860d-125">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3860d-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3860d-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="3860d-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3860d-127">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="3860d-127">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3860d-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3860d-128">See Also</span></span>

[<span data-ttu-id="3860d-129">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="3860d-129">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="3860d-130">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="3860d-130">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="3860d-131">JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="3860d-131">JET_BKLOGTIME</span></span>](./jet-bklogtime-structure.md)  
[<span data-ttu-id="3860d-132">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="3860d-132">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
