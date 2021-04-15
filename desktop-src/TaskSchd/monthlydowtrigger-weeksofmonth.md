---
title: Monthlydowauslöst. weeksofmonth (Eigenschaft)
description: Ruft bei der Skripterstellung die Wochen des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Weeksofmonth-Eigenschaft Taskplaner
- Weeksofmonth-Eigenschaft Taskplaner, monthlydowauslöserobjekt
- Monthlydowauslöserobjekt Taskplaner, weeksofmonth (Eigenschaft)
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475807"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a><span data-ttu-id="f2bdb-106">Monthlydowauslöst. weeksofmonth (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f2bdb-106">MonthlyDOWTrigger.WeeksOfMonth property</span></span>

<span data-ttu-id="f2bdb-107">Ruft bei der Skripterstellung die Wochen des Monats ab, in denen die Aufgabe ausgeführt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f2bdb-107">For scripting, gets or sets the weeks of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bdb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2bdb-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a><span data-ttu-id="f2bdb-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f2bdb-109">Property value</span></span>

<span data-ttu-id="f2bdb-110">Eine bitweise Maske, die die Wochentage angibt, an denen die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2bdb-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2bdb-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2bdb-111">Remarks</span></span>

<span data-ttu-id="f2bdb-112">Die folgende Tabelle zeigt die Zuordnung der bitweisen Maske, die von dieser Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2bdb-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="f2bdb-113">Woche</span><span class="sxs-lookup"><span data-stu-id="f2bdb-113">Week</span></span>                     | <span data-ttu-id="f2bdb-114">Hexadezimalwert</span><span class="sxs-lookup"><span data-stu-id="f2bdb-114">Hex Value</span></span> | <span data-ttu-id="f2bdb-115">Dezimalwert</span><span class="sxs-lookup"><span data-stu-id="f2bdb-115">Decimal Value</span></span> |
|--------------------------|-----------|---------------|
| <span data-ttu-id="f2bdb-116">Erste Woche des Monats</span><span class="sxs-lookup"><span data-stu-id="f2bdb-116">First week of the month</span></span>  | <span data-ttu-id="f2bdb-117">0X01</span><span class="sxs-lookup"><span data-stu-id="f2bdb-117">0X01</span></span>      | <span data-ttu-id="f2bdb-118">1</span><span class="sxs-lookup"><span data-stu-id="f2bdb-118">1</span></span>             |
| <span data-ttu-id="f2bdb-119">Zweite Woche des Monats</span><span class="sxs-lookup"><span data-stu-id="f2bdb-119">Second week of the month</span></span> | <span data-ttu-id="f2bdb-120">0x02</span><span class="sxs-lookup"><span data-stu-id="f2bdb-120">0x02</span></span>      | <span data-ttu-id="f2bdb-121">2</span><span class="sxs-lookup"><span data-stu-id="f2bdb-121">2</span></span>             |
| <span data-ttu-id="f2bdb-122">Dritte Woche des Monats</span><span class="sxs-lookup"><span data-stu-id="f2bdb-122">Third week of the month</span></span>  | <span data-ttu-id="f2bdb-123">0X04</span><span class="sxs-lookup"><span data-stu-id="f2bdb-123">0X04</span></span>      | <span data-ttu-id="f2bdb-124">4</span><span class="sxs-lookup"><span data-stu-id="f2bdb-124">4</span></span>             |
| <span data-ttu-id="f2bdb-125">Vierte Woche des Monats</span><span class="sxs-lookup"><span data-stu-id="f2bdb-125">Fourth week of the month</span></span> | <span data-ttu-id="f2bdb-126">0X08</span><span class="sxs-lookup"><span data-stu-id="f2bdb-126">0X08</span></span>      | <span data-ttu-id="f2bdb-127">8</span><span class="sxs-lookup"><span data-stu-id="f2bdb-127">8</span></span>             |



 

<span data-ttu-id="f2bdb-128">Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Wochentage eines monatlichen [**Wochen**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) Tags durch das Week-Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2bdb-128">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bdb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2bdb-129">Requirements</span></span>



| <span data-ttu-id="f2bdb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2bdb-130">Requirement</span></span> | <span data-ttu-id="f2bdb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f2bdb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bdb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2bdb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bdb-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2bdb-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f2bdb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2bdb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bdb-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2bdb-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2bdb-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f2bdb-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2bdb-137"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2bdb-137"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2bdb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f2bdb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2bdb-139"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2bdb-139"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2bdb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2bdb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bdb-141">**Monthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="f2bdb-141">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="f2bdb-142">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f2bdb-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





