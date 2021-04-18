---
description: 'Weitere Informationen finden Sie hier: JET_BKLOGTIME Struktur'
title: JET_BKLOGTIME Struktur
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350834"
---
# <a name="jet_bklogtime-structure"></a><span data-ttu-id="80914-103">JET_BKLOGTIME Struktur</span><span class="sxs-lookup"><span data-stu-id="80914-103">JET_BKLOGTIME Structure</span></span>


<span data-ttu-id="80914-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="80914-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_bklogtime-structure"></a><span data-ttu-id="80914-105">JET_BKLOGTIME Struktur</span><span class="sxs-lookup"><span data-stu-id="80914-105">JET_BKLOGTIME Structure</span></span>

<span data-ttu-id="80914-106">Die **JET_BKLOGTIME** -Struktur enthält die Datums-und Uhrzeit Elemente eines Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="80914-106">The **JET_BKLOGTIME** structure holds the date and time elements of an event.</span></span> <span data-ttu-id="80914-107">Es handelt sich um eine Erweiterung von [JET_LOGTIME](./jet-logtime-structure.md).</span><span class="sxs-lookup"><span data-stu-id="80914-107">It is an extension of [JET_LOGTIME](./jet-logtime-structure.md).</span></span>

<span data-ttu-id="80914-108">**Windows Vista: JET_BKLOGTIME** wird in Windows Vista eingeführt.</span><span class="sxs-lookup"><span data-stu-id="80914-108">**Windows Vista:  JET_BKLOGTIME** is introduced in Windows Vista.</span></span>

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a><span data-ttu-id="80914-109">Member</span><span class="sxs-lookup"><span data-stu-id="80914-109">Members</span></span>

<span data-ttu-id="80914-110">**bseconds**</span><span class="sxs-lookup"><span data-stu-id="80914-110">**bSeconds**</span></span>

<span data-ttu-id="80914-111">Die Uhrzeit des Ereignisses in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="80914-111">The time of the event in seconds.</span></span> <span data-ttu-id="80914-112">Dies kann 0 (null) bis 60 sein.</span><span class="sxs-lookup"><span data-stu-id="80914-112">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="80914-113">0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.</span><span class="sxs-lookup"><span data-stu-id="80914-113">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="80914-114">**bminuten**</span><span class="sxs-lookup"><span data-stu-id="80914-114">**bMinutes**</span></span>

<span data-ttu-id="80914-115">Die Uhrzeit des Ereignisses (in Minuten).</span><span class="sxs-lookup"><span data-stu-id="80914-115">The time of the event in minutes.</span></span> <span data-ttu-id="80914-116">Dies kann 0 (null) bis 60 sein.</span><span class="sxs-lookup"><span data-stu-id="80914-116">This can be 0 (zero) to 60.</span></span> <span data-ttu-id="80914-117">0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.</span><span class="sxs-lookup"><span data-stu-id="80914-117">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="80914-118">**bhours**</span><span class="sxs-lookup"><span data-stu-id="80914-118">**bHours**</span></span>

<span data-ttu-id="80914-119">Die Uhrzeit des Ereignisses (in Stunden).</span><span class="sxs-lookup"><span data-stu-id="80914-119">The time of the event in hours.</span></span> <span data-ttu-id="80914-120">Dies kann 0 (null) bis 24 sein.</span><span class="sxs-lookup"><span data-stu-id="80914-120">This can be 0 (zero) to 24.</span></span> <span data-ttu-id="80914-121">0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.</span><span class="sxs-lookup"><span data-stu-id="80914-121">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="80914-122">**bday**</span><span class="sxs-lookup"><span data-stu-id="80914-122">**bDay**</span></span>

<span data-ttu-id="80914-123">Der Tag des Monats des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="80914-123">The day of the month of the event.</span></span> <span data-ttu-id="80914-124">Dies kann 0 (null) bis 31 sein.</span><span class="sxs-lookup"><span data-stu-id="80914-124">This can be 0 (zero) to 31.</span></span> <span data-ttu-id="80914-125">0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.</span><span class="sxs-lookup"><span data-stu-id="80914-125">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="80914-126">**bmonth**</span><span class="sxs-lookup"><span data-stu-id="80914-126">**bMonth**</span></span>

<span data-ttu-id="80914-127">Der Monat des Jahres des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="80914-127">The month of the year of the event.</span></span> <span data-ttu-id="80914-128">Der Wert kann zwischen 0 (null) und 12 liegen.</span><span class="sxs-lookup"><span data-stu-id="80914-128">This can be 0 (zero) to 12.</span></span> <span data-ttu-id="80914-129">0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.</span><span class="sxs-lookup"><span data-stu-id="80914-129">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="80914-130">**byear**</span><span class="sxs-lookup"><span data-stu-id="80914-130">**bYear**</span></span>

<span data-ttu-id="80914-131">Das Jahr (Offset um 1900) des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="80914-131">The year (offset by 1900) of the event.</span></span> <span data-ttu-id="80914-132">Um das tatsächliche Jahr zu erreichen, fügen Sie diesem Wert 1900 hinzu.</span><span class="sxs-lookup"><span data-stu-id="80914-132">To achieve the actual year, add 1900 to this value.</span></span> <span data-ttu-id="80914-133">0 (null) wird verwendet, wenn die **JET_BKLOGTIME** Struktur "Null" ist.</span><span class="sxs-lookup"><span data-stu-id="80914-133">0 (zero) is used when the **JET_BKLOGTIME** structure is "null".</span></span>

<span data-ttu-id="80914-134">**bFiller1**</span><span class="sxs-lookup"><span data-stu-id="80914-134">**bFiller1**</span></span>

<span data-ttu-id="80914-135">Dieses Feld sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="80914-135">This field should be ignored.</span></span>

<span data-ttu-id="80914-136">**"f"**</span><span class="sxs-lookup"><span data-stu-id="80914-136">**fTimeIsUTC**</span></span>

<span data-ttu-id="80914-137">Die Uhrzeit liegt im UTC-Format vor.</span><span class="sxs-lookup"><span data-stu-id="80914-137">The time is in UTC format.</span></span>

<span data-ttu-id="80914-138">**funused**</span><span class="sxs-lookup"><span data-stu-id="80914-138">**fUnused**</span></span>

<span data-ttu-id="80914-139">Dieses Feld sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="80914-139">This field should be ignored.</span></span>

<span data-ttu-id="80914-140">**bFiller2**</span><span class="sxs-lookup"><span data-stu-id="80914-140">**bFiller2**</span></span>

<span data-ttu-id="80914-141">Dieses Feld sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="80914-141">This field should be ignored.</span></span>

<span data-ttu-id="80914-142">**fossnapshot**</span><span class="sxs-lookup"><span data-stu-id="80914-142">**fOSSnapshot**</span></span>

<span data-ttu-id="80914-143">Wenn dieses Ereignis eine Sicherung ist, enthält dieses Flag einen der folgenden möglichen Werte:</span><span class="sxs-lookup"><span data-stu-id="80914-143">If this event is a backup, this flag contains one of the following possible values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80914-144">Name</span><span class="sxs-lookup"><span data-stu-id="80914-144">Name</span></span></p></th>
<th><p><span data-ttu-id="80914-145">Wert</span><span class="sxs-lookup"><span data-stu-id="80914-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80914-146">Streamingsicherung</span><span class="sxs-lookup"><span data-stu-id="80914-146">streaming backup</span></span></p></td>
<td><p><span data-ttu-id="80914-147">0 (null)</span><span class="sxs-lookup"><span data-stu-id="80914-147">0 (zero)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80914-148">Momentaufnahme Sicherung</span><span class="sxs-lookup"><span data-stu-id="80914-148">snapshot backup</span></span></p></td>
<td><p><span data-ttu-id="80914-149">1</span><span class="sxs-lookup"><span data-stu-id="80914-149">1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="80914-150">**frei bedient**</span><span class="sxs-lookup"><span data-stu-id="80914-150">**fReserved**</span></span>

<span data-ttu-id="80914-151">Dieses Feld sollte ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="80914-151">This field should be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="80914-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80914-152">Remarks</span></span>

<span data-ttu-id="80914-153">Diese Struktur wird beim Debuggen verwendet.</span><span class="sxs-lookup"><span data-stu-id="80914-153">This structure is used when debugging.</span></span>

### <a name="requirements"></a><span data-ttu-id="80914-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80914-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80914-155"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="80914-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="80914-156">Erfordert Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80914-156">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80914-157"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="80914-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="80914-158">Erfordert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="80914-158">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80914-159"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="80914-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="80914-160">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="80914-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="80914-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="80914-161">See Also</span></span>

[<span data-ttu-id="80914-162">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="80914-162">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="80914-163">JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="80914-163">JET_DBINFOMISC</span></span>](./jet-dbinfomisc-structure.md)
