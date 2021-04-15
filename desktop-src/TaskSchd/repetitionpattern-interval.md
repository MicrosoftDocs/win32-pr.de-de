---
title: Repetitionpattern. Interval (Eigenschaft)
description: Ruft bei der Skripterstellung die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe ab oder legt diese fest.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Intervall Eigenschaft Taskplaner
- Interval-Eigenschaft Taskplaner, repetitionpattern-Objekt
- Repetitionpattern-Objekt Taskplaner, Intervall Eigenschaft
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d62bb821f4c5e61d344e21fafa4ba1265c73470
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518215"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="544b1-106">Repetitionpattern. Interval (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="544b1-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="544b1-107">Ruft bei der Skripterstellung die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="544b1-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="544b1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="544b1-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="544b1-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="544b1-109">Property value</span></span>

<span data-ttu-id="544b1-110">Die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="544b1-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="544b1-111">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S ("PT5M" ist beispielsweise 5 Minuten, "PT1H" ist 1 Stunde, und "PT20M" beträgt 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="544b1-111">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="544b1-112">Die maximal zulässige Dauer beträgt 31 Tage, und die zulässige Mindestanzahl beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="544b1-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="544b1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="544b1-113">Remarks</span></span>

<span data-ttu-id="544b1-114">Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.</span><span class="sxs-lookup"><span data-stu-id="544b1-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="544b1-115">Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsintervall im [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="544b1-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="544b1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="544b1-116">Requirements</span></span>



| <span data-ttu-id="544b1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="544b1-117">Requirement</span></span> | <span data-ttu-id="544b1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="544b1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="544b1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="544b1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="544b1-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="544b1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="544b1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="544b1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="544b1-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="544b1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="544b1-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="544b1-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="544b1-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="544b1-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="544b1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="544b1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="544b1-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="544b1-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="544b1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="544b1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544b1-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="544b1-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





