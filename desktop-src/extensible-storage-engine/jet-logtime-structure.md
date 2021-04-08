---
description: 'Weitere Informationen finden Sie hier: JET_LOGTIME Struktur'
title: JET_LOGTIME Struktur
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762426"
---
# <a name="jet_logtime-structure"></a><span data-ttu-id="65341-103">JET_LOGTIME Struktur</span><span class="sxs-lookup"><span data-stu-id="65341-103">JET_LOGTIME Structure</span></span>


<span data-ttu-id="65341-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="65341-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_logtime-structure"></a><span data-ttu-id="65341-105">JET_LOGTIME Struktur</span><span class="sxs-lookup"><span data-stu-id="65341-105">JET_LOGTIME Structure</span></span>

<span data-ttu-id="65341-106">Die **JET_LOGTIME** -Struktur enthält Elemente des Datums und der Uhrzeit eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="65341-106">The **JET_LOGTIME** structure holds elements of the date and time of an event.</span></span>

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a><span data-ttu-id="65341-107">Member</span><span class="sxs-lookup"><span data-stu-id="65341-107">Members</span></span>

<span data-ttu-id="65341-108">**bseconds**</span><span class="sxs-lookup"><span data-stu-id="65341-108">**bSeconds**</span></span>

<span data-ttu-id="65341-109">Die Uhrzeit des Ereignisses in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="65341-109">The time of the event in seconds.</span></span> <span data-ttu-id="65341-110">Dieser Wert kann zwischen 0 und 59 liegen.</span><span class="sxs-lookup"><span data-stu-id="65341-110">This value can be 0 to 59.</span></span> <span data-ttu-id="65341-111">0 wird verwendet, wenn die-Struktur NULL ist.</span><span class="sxs-lookup"><span data-stu-id="65341-111">0 is used when the structure is null.</span></span>

<span data-ttu-id="65341-112">**bminuten**</span><span class="sxs-lookup"><span data-stu-id="65341-112">**bMinutes**</span></span>

<span data-ttu-id="65341-113">Die Uhrzeit des Ereignisses (in Minuten).</span><span class="sxs-lookup"><span data-stu-id="65341-113">The time of the event in minutes.</span></span> <span data-ttu-id="65341-114">Dieser Wert kann zwischen 0 und 59 liegen.</span><span class="sxs-lookup"><span data-stu-id="65341-114">This value can be 0 to 59.</span></span> <span data-ttu-id="65341-115">0 wird verwendet, wenn die-Struktur NULL ist.</span><span class="sxs-lookup"><span data-stu-id="65341-115">0 is used when the structure is null.</span></span>

<span data-ttu-id="65341-116">**bhours**</span><span class="sxs-lookup"><span data-stu-id="65341-116">**bHours**</span></span>

<span data-ttu-id="65341-117">Die Uhrzeit des Ereignisses (in Stunden).</span><span class="sxs-lookup"><span data-stu-id="65341-117">The time of the event in hours.</span></span> <span data-ttu-id="65341-118">Dieser Wert kann zwischen 0 und 23 liegen.</span><span class="sxs-lookup"><span data-stu-id="65341-118">This value can be 0 to 23.</span></span> <span data-ttu-id="65341-119">0 wird verwendet, wenn die-Struktur NULL ist.</span><span class="sxs-lookup"><span data-stu-id="65341-119">0 is used when the structure is null.</span></span>

<span data-ttu-id="65341-120">**bday**</span><span class="sxs-lookup"><span data-stu-id="65341-120">**bDay**</span></span>

<span data-ttu-id="65341-121">Der Tag des Monats des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="65341-121">The day of the month of the event.</span></span> <span data-ttu-id="65341-122">Dieser Wert kann zwischen 0 und 31 liegen.</span><span class="sxs-lookup"><span data-stu-id="65341-122">This value can be 0 to 31.</span></span> <span data-ttu-id="65341-123">0 wird verwendet, wenn die-Struktur NULL ist.</span><span class="sxs-lookup"><span data-stu-id="65341-123">0 is used when the structure is null.</span></span>

<span data-ttu-id="65341-124">**bmonth**</span><span class="sxs-lookup"><span data-stu-id="65341-124">**bMonth**</span></span>

<span data-ttu-id="65341-125">Der Monat des Jahres des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="65341-125">The month of the year of the event.</span></span> <span data-ttu-id="65341-126">Dieser Wert kann zwischen 0 und 12 liegen.</span><span class="sxs-lookup"><span data-stu-id="65341-126">This value can be 0 to 12.</span></span> <span data-ttu-id="65341-127">0 wird verwendet, wenn die-Struktur NULL ist.</span><span class="sxs-lookup"><span data-stu-id="65341-127">0 is used when the structure is null.</span></span>

<span data-ttu-id="65341-128">**byear**</span><span class="sxs-lookup"><span data-stu-id="65341-128">**bYear**</span></span>

<span data-ttu-id="65341-129">Das Jahr des Ereignisses (Offset um 1900).</span><span class="sxs-lookup"><span data-stu-id="65341-129">The year of the event (offset by 1900).</span></span> <span data-ttu-id="65341-130">Um das tatsächliche Jahr zu erreichen, fügen Sie diesem Wert 1900 hinzu.</span><span class="sxs-lookup"><span data-stu-id="65341-130">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="65341-131">0 wird verwendet, wenn die-Struktur NULL ist.</span><span class="sxs-lookup"><span data-stu-id="65341-131">0 is used when the structure is null.</span></span>

<span data-ttu-id="65341-132">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="65341-132">**bFiller1**</span></span>

<span data-ttu-id="65341-133">Dieses Feld sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="65341-133">This field should be ignored.</span></span>

<span data-ttu-id="65341-134">**"f"**</span><span class="sxs-lookup"><span data-stu-id="65341-134">**fTimeIsUTC**</span></span>

<span data-ttu-id="65341-135">Die Uhrzeit liegt im UTC-Format vor.</span><span class="sxs-lookup"><span data-stu-id="65341-135">The time is in UTC format.</span></span>

<span data-ttu-id="65341-136">**funused**</span><span class="sxs-lookup"><span data-stu-id="65341-136">**fUnused**</span></span>

<span data-ttu-id="65341-137">Dieses Feld sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="65341-137">This field should be ignored.</span></span>

<span data-ttu-id="65341-138">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="65341-138">**bFiller2**</span></span>

<span data-ttu-id="65341-139">Dieses Feld sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="65341-139">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="65341-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65341-140">Remarks</span></span>

<span data-ttu-id="65341-141">Diese Struktur ist hauptsächlich für die Verwendung beim Debuggen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="65341-141">This structure is meant primarily for usage in debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="65341-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65341-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65341-143"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="65341-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="65341-144">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="65341-144">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65341-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="65341-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="65341-146">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="65341-146">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65341-147"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="65341-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="65341-148">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="65341-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="65341-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="65341-149">See Also</span></span>

[<span data-ttu-id="65341-150">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="65341-150">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
