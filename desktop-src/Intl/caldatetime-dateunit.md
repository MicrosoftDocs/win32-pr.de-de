---
description: Veraltet. Gibt die Datums Einheiten für die Anpassung der caldatetime-Struktur an.
ms.assetid: 20d0cd7a-6e6b-4c82-9cfa-e4f4315d6362
title: CALDATETIME_DATEUNIT-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME_DATEUNIT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6ce1f8929dd6e2f7de59d32d66229f73c062505c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345703"
---
# <a name="caldatetime_dateunit-enumeration"></a><span data-ttu-id="267fe-104">Caldatetime \_ dateunit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="267fe-104">CALDATETIME\_DATEUNIT enumeration</span></span>

<span data-ttu-id="267fe-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="267fe-105">Deprecated.</span></span> <span data-ttu-id="267fe-106">Gibt die Datums Einheiten für die Anpassung der [**caldatetime**](caldatetime.md) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="267fe-106">Specifies the date units for adjusting the [**CALDATETIME**](caldatetime.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="267fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="267fe-107">Syntax</span></span>


```C++
enum CALDATETIME_DATEUNIT {
  EraUnit, 
  YearUnit, 
  MonthUnit, 
  WeekUnit, 
  DayUnit, 
  HourUnit, 
  MinuteUnit, 
  SecondUnit, 
  TickUnit 

};
```



## <a name="constants"></a><span data-ttu-id="267fe-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="267fe-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="267fe-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**Eraunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-109"><span id="EraUnit"></span><span id="eraunit"></span><span id="ERAUNIT"></span>**EraUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-110">Die Zeiteinheit für das ERA-Datum.</span><span class="sxs-lookup"><span data-stu-id="267fe-110">The era date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**Yearunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-111"><span id="YearUnit"></span><span id="yearunit"></span><span id="YEARUNIT"></span>**YearUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-112">Die Zeiteinheit für das Jahr.</span><span class="sxs-lookup"><span data-stu-id="267fe-112">The year date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**Monthunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-113"><span id="MonthUnit"></span><span id="monthunit"></span><span id="MONTHUNIT"></span>**MonthUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-114">Die Zeiteinheit für das Datum des Monats.</span><span class="sxs-lookup"><span data-stu-id="267fe-114">The month date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**Weekunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-115"><span id="WeekUnit"></span><span id="weekunit"></span><span id="WEEKUNIT"></span>**WeekUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-116">Die Zeiteinheit für die Woche.</span><span class="sxs-lookup"><span data-stu-id="267fe-116">The week date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**Dayunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-117"><span id="DayUnit"></span><span id="dayunit"></span><span id="DAYUNIT"></span>**DayUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-118">Die Zeiteinheit für das Datum des Tages.</span><span class="sxs-lookup"><span data-stu-id="267fe-118">The day date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**Sanunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-119"><span id="HourUnit"></span><span id="hourunit"></span><span id="HOURUNIT"></span>**HourUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-120">Die Zeiteinheit für das Stunden Datum.</span><span class="sxs-lookup"><span data-stu-id="267fe-120">The hour date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**Minuteunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-121"><span id="MinuteUnit"></span><span id="minuteunit"></span><span id="MINUTEUNIT"></span>**MinuteUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-122">Die Zeiteinheit für das Minuten Datum.</span><span class="sxs-lookup"><span data-stu-id="267fe-122">The minute date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**Secondunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-123"><span id="SecondUnit"></span><span id="secondunit"></span><span id="SECONDUNIT"></span>**SecondUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-124">Die zweite Datums-/uhrzeiteinheit.</span><span class="sxs-lookup"><span data-stu-id="267fe-124">The second date time unit.</span></span>

</dd> <dt>

<span data-ttu-id="267fe-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**Tickunit**</span><span class="sxs-lookup"><span data-stu-id="267fe-125"><span id="TickUnit"></span><span id="tickunit"></span><span id="TICKUNIT"></span>**TickUnit**</span></span>
</dt> <dd>

<span data-ttu-id="267fe-126">Die Zeiteinheit für den Teil Strich.</span><span class="sxs-lookup"><span data-stu-id="267fe-126">The tick date time unit.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="267fe-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="267fe-127">Requirements</span></span>



| <span data-ttu-id="267fe-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="267fe-128">Requirement</span></span> | <span data-ttu-id="267fe-129">Wert</span><span class="sxs-lookup"><span data-stu-id="267fe-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="267fe-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="267fe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="267fe-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="267fe-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="267fe-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="267fe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="267fe-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="267fe-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="267fe-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="267fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267fe-135">Enumerationstypen für die Unterstützung der</span><span class="sxs-lookup"><span data-stu-id="267fe-135">National Language Support Enumeration Types</span></span>](national-language-support-enumeration-types.md)
</dt> </dl>

 

 




