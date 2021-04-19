---
title: TaskSettings.Executiontimelimit-Eigenschaft
description: Ruft bei der Skripterstellung die Zeitspanne ab, die zum Ausführen der Aufgabe zulässig ist, oder legt diese fest.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Executiontimelimit-Eigenschaft Taskplaner
- Executiontimelimit-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, executiontimelimit-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339359"
---
# <a name="tasksettingsexecutiontimelimit-property"></a><span data-ttu-id="f7570-106">TaskSettings.Executiontimelimit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f7570-106">TaskSettings.ExecutionTimeLimit property</span></span>

<span data-ttu-id="f7570-107">Ruft bei der Skripterstellung die Zeitspanne ab, die zum Ausführen der Aufgabe zulässig ist, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f7570-107">For scripting, gets or sets the amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="f7570-108">Standardmäßig wird eine Aufgabe 72 Stunden nach dem Start angehalten.</span><span class="sxs-lookup"><span data-stu-id="f7570-108">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="f7570-109">Sie können dies ändern, indem Sie diese Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="f7570-109">You can change this by changing this setting.</span></span>

<span data-ttu-id="f7570-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f7570-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7570-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7570-111">Syntax</span></span>


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="f7570-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f7570-112">Property value</span></span>

<span data-ttu-id="f7570-113">Die Zeitspanne, die zum Ausführen der Aufgabe zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f7570-113">The amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="f7570-114">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="f7570-114">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="f7570-115">Mit dem Wert PT0S kann der Task unbegrenzt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f7570-115">A value of PT0S will enable the task to run indefinitely.</span></span> <span data-ttu-id="f7570-116">Wenn dieser Parameter auf "Nothing" festgelegt ist, ist das Ausführungszeit Limit unendlich.</span><span class="sxs-lookup"><span data-stu-id="f7570-116">When this parameter is set to Nothing, the execution time limit is infinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7570-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7570-117">Remarks</span></span>

<span data-ttu-id="f7570-118">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**executiontimelimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="f7570-118">When reading or writing XML for a task, this setting is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7570-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7570-119">Requirements</span></span>



| <span data-ttu-id="f7570-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7570-120">Requirement</span></span> | <span data-ttu-id="f7570-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f7570-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7570-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7570-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7570-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7570-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f7570-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7570-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7570-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f7570-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7570-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f7570-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7570-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7570-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7570-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f7570-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7570-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7570-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7570-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7570-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7570-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f7570-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





