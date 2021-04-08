---
title: Trigger.Executiontimelimit-Eigenschaft
description: Ruft bei der Skripterstellung die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Executiontimelimit-Eigenschaft Taskplaner
- Executiontimelimit-Eigenschaft Taskplaner, Auslöserobjekt
- Auslöse Objekt Taskplaner, executiontimelimit-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949637"
---
# <a name="triggerexecutiontimelimit-property"></a><span data-ttu-id="d69f3-106">Trigger.Executiontimelimit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d69f3-106">Trigger.ExecutionTimeLimit property</span></span>

<span data-ttu-id="d69f3-107">Ruft bei der Skripterstellung die maximale Zeitspanne ab, die der vom-Aufruf gestartete Task ausgeführt werden darf, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d69f3-107">For scripting, gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69f3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d69f3-108">Syntax</span></span>


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="d69f3-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d69f3-109">Property value</span></span>

<span data-ttu-id="d69f3-110">Die maximale Zeitspanne, die der vom-Aufruf gestartete Task ausgeführt werden darf.</span><span class="sxs-lookup"><span data-stu-id="d69f3-110">The maximum amount of time that the task launched by the trigger is allowed to run.</span></span> <span data-ttu-id="d69f3-111">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="d69f3-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="d69f3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d69f3-112">Remarks</span></span>

<span data-ttu-id="d69f3-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Ausführungszeit Limit im [**executiontimelimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="d69f3-113">When reading or writing XML for a task, the execution time limit is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69f3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d69f3-114">Requirements</span></span>



| <span data-ttu-id="d69f3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d69f3-115">Requirement</span></span> | <span data-ttu-id="d69f3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d69f3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d69f3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d69f3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d69f3-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d69f3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d69f3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d69f3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d69f3-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d69f3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d69f3-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d69f3-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d69f3-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d69f3-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d69f3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d69f3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d69f3-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d69f3-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d69f3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d69f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69f3-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d69f3-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





