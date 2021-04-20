---
title: RepetitionPattern.Interval-Eigenschaft
description: Bei der Skripterstellung ruft die Zeit zwischen jedem Neustart der Aufgabe ab oder legt diese fest.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Interval-Taskplaner
- Interval-Taskplaner , RepetitionPattern-Objekt
- RepetitionPattern-Objekt Taskplaner , Interval-Eigenschaft
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
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734175"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="39f9a-106">RepetitionPattern.Interval-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39f9a-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="39f9a-107">Bei der Skripterstellung ruft die Zeit zwischen jedem Neustart der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="39f9a-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f9a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39f9a-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="39f9a-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="39f9a-109">Property value</span></span>

<span data-ttu-id="39f9a-110">Die Zeit zwischen jedem Neustart der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="39f9a-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="39f9a-111">Das Format für diese Zeichenfolge ist (z. B. `P<days>DT<hours>H<minutes>M<seconds>S` ist "PT5M" 5 Minuten, "PT1H" ist 1 Stunde und "PT20M" beträgt 20 Minuten).</span><span class="sxs-lookup"><span data-stu-id="39f9a-111">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="39f9a-112">Die maximal zulässige Zeit beträgt 31 Tage, und die zulässige Mindestzeit beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="39f9a-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="39f9a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39f9a-113">Remarks</span></span>

<span data-ttu-id="39f9a-114">Wenn Sie eine Wiederholungsdauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.</span><span class="sxs-lookup"><span data-stu-id="39f9a-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="39f9a-115">Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsintervall im [**Interval-Element**](taskschedulerschema-interval-repetitiontype-element.md) des Taskplaner angegeben.</span><span class="sxs-lookup"><span data-stu-id="39f9a-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f9a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39f9a-116">Requirements</span></span>



| <span data-ttu-id="39f9a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39f9a-117">Requirement</span></span> | <span data-ttu-id="39f9a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="39f9a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39f9a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39f9a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39f9a-120">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39f9a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="39f9a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39f9a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39f9a-122">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39f9a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39f9a-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="39f9a-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="39f9a-124"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="39f9a-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="39f9a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="39f9a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39f9a-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39f9a-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f9a-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="39f9a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f9a-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="39f9a-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





