---
title: Repetitionpattern. Duration (Eigenschaft)
description: Ruft bei der Skripterstellung ab oder legt fest, wie lange das Muster wiederholt wird.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Duration-Eigenschaft Taskplaner
- Duration-Eigenschaft Taskplaner, repetitionpattern-Objekt
- Repetitionpattern-Objekt Taskplaner, Duration-Eigenschaft
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345310"
---
# <a name="repetitionpatternduration-property"></a><span data-ttu-id="74242-106">Repetitionpattern. Duration (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="74242-106">RepetitionPattern.Duration property</span></span>

<span data-ttu-id="74242-107">Ruft bei der Skripterstellung ab oder legt fest, wie lange das Muster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="74242-107">For scripting, gets or sets how long the pattern is repeated.</span></span>

## <a name="syntax"></a><span data-ttu-id="74242-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="74242-108">Syntax</span></span>


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a><span data-ttu-id="74242-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="74242-109">Property value</span></span>

<span data-ttu-id="74242-110">Gibt an, wie lange das Muster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="74242-110">How long the pattern is repeated.</span></span> <span data-ttu-id="74242-111">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="74242-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="74242-112">Die zulässige minimal Dauer beträgt eine Minute.</span><span class="sxs-lookup"><span data-stu-id="74242-112">The minimum time allowed is one minute.</span></span>

<span data-ttu-id="74242-113">Wenn für die Dauer kein Wert angegeben wird, wird das Muster unbegrenzt wiederholt.</span><span class="sxs-lookup"><span data-stu-id="74242-113">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span>

## <a name="remarks"></a><span data-ttu-id="74242-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74242-114">Remarks</span></span>

<span data-ttu-id="74242-115">Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.</span><span class="sxs-lookup"><span data-stu-id="74242-115">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="74242-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Wiederholungs Dauer im [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="74242-116">When reading or writing XML for a task, the repetition duration is specified in the [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="74242-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74242-117">Requirements</span></span>



| <span data-ttu-id="74242-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74242-118">Requirement</span></span> | <span data-ttu-id="74242-119">Wert</span><span class="sxs-lookup"><span data-stu-id="74242-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74242-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74242-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74242-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74242-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="74242-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74242-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74242-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74242-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74242-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="74242-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="74242-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74242-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74242-126">DLL</span><span class="sxs-lookup"><span data-stu-id="74242-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74242-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74242-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74242-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74242-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74242-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="74242-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





