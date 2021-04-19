---
description: Veraltet. Stellt einen Zeitpunkt dar, der normalerweise als Datum und Uhrzeit und als entsprechender Kalender ausgedrückt wird.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Caldatetime-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363860"
---
# <a name="caldatetime-structure"></a><span data-ttu-id="03222-104">Caldatetime-Struktur</span><span class="sxs-lookup"><span data-stu-id="03222-104">CALDATETIME structure</span></span>

<span data-ttu-id="03222-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="03222-105">Deprecated.</span></span> <span data-ttu-id="03222-106">Stellt einen Zeitpunkt dar, der normalerweise als Datum und Uhrzeit und als entsprechender Kalender ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="03222-106">Represents an instant in time, typically expressed as a date and time of day and a corresponding calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="03222-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03222-107">Syntax</span></span>


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a><span data-ttu-id="03222-108">Member</span><span class="sxs-lookup"><span data-stu-id="03222-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="03222-109">**Calid**</span><span class="sxs-lookup"><span data-stu-id="03222-109">**CalId**</span></span>
</dt> <dd>

<span data-ttu-id="03222-110">Der [Kalender Bezeichner](calendar-identifiers.md) für den Zeitpunkt des Zeitpunkts.</span><span class="sxs-lookup"><span data-stu-id="03222-110">The [calendar identifier](calendar-identifiers.md) for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-111">**Thi**</span><span class="sxs-lookup"><span data-stu-id="03222-111">**Era**</span></span>
</dt> <dd>

<span data-ttu-id="03222-112">Die ERA-Informationen für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-112">The era information for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-113">**Jährigen**</span><span class="sxs-lookup"><span data-stu-id="03222-113">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="03222-114">Das Jahr für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-114">The year for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-115">**Ges**</span><span class="sxs-lookup"><span data-stu-id="03222-115">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="03222-116">Der Monat für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-116">The month for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-117">**Day**</span><span class="sxs-lookup"><span data-stu-id="03222-117">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="03222-118">Der Tag für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-118">The day for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-119">**DayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="03222-119">**DayOfWeek**</span></span>
</dt> <dd>

<span data-ttu-id="03222-120">Der Wochentag für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-120">The day of the week for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-121">**Geöffneten**</span><span class="sxs-lookup"><span data-stu-id="03222-121">**Hour**</span></span>
</dt> <dd>

<span data-ttu-id="03222-122">Die Stunde für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-122">The hour for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-123">**Tiges**</span><span class="sxs-lookup"><span data-stu-id="03222-123">**Minute**</span></span>
</dt> <dd>

<span data-ttu-id="03222-124">Die Minute für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-124">The minute for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-125">**Klässler**</span><span class="sxs-lookup"><span data-stu-id="03222-125">**Second**</span></span>
</dt> <dd>

<span data-ttu-id="03222-126">Die zweite für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-126">The second for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="03222-127">**Bewegt**</span><span class="sxs-lookup"><span data-stu-id="03222-127">**Tick**</span></span>
</dt> <dd>

<span data-ttu-id="03222-128">Der Takt für den Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="03222-128">The tick for the instant in time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03222-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03222-129">Requirements</span></span>



| <span data-ttu-id="03222-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03222-130">Requirement</span></span> | <span data-ttu-id="03222-131">Wert</span><span class="sxs-lookup"><span data-stu-id="03222-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="03222-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03222-132">Minimum supported client</span></span><br/> | <span data-ttu-id="03222-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03222-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="03222-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03222-134">Minimum supported server</span></span><br/> | <span data-ttu-id="03222-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03222-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03222-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03222-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03222-137">Unterstützung für nationale Sprachunterstützung</span><span class="sxs-lookup"><span data-stu-id="03222-137">National Language Support Structures</span></span>](national-language-support-structures.md)
</dt> </dl>

 

 




