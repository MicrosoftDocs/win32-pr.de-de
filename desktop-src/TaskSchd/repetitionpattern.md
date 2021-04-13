---
title: Repetitionpattern-Objekt
description: Skript Objekt, das definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- Trigger Taskplaner, Wiederholungsmuster Objekt
- Wiederholungsmuster Taskplaner, Objekt
- Repetitionpattern-Objekt Taskplaner
- Wiederholungpattern-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475975"
---
# <a name="repetitionpattern-object"></a><span data-ttu-id="fb335-107">Repetitionpattern-Objekt</span><span class="sxs-lookup"><span data-stu-id="fb335-107">RepetitionPattern object</span></span>

<span data-ttu-id="fb335-108">Skript Objekt, das definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="fb335-108">Scripting object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="members"></a><span data-ttu-id="fb335-109">Member</span><span class="sxs-lookup"><span data-stu-id="fb335-109">Members</span></span>

<span data-ttu-id="fb335-110">Das **wiederholungpattern** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fb335-110">The **RepetitionPattern** object has these types of members:</span></span>

-   [<span data-ttu-id="fb335-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb335-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb335-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fb335-112">Properties</span></span>

<span data-ttu-id="fb335-113">Das **repetitionpattern** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb335-113">The **RepetitionPattern** object has these properties.</span></span>



| <span data-ttu-id="fb335-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fb335-114">Property</span></span>                                                                    | <span data-ttu-id="fb335-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="fb335-115">Access type</span></span>           | <span data-ttu-id="fb335-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb335-116">Description</span></span>                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb335-117">**Duration**</span><span class="sxs-lookup"><span data-stu-id="fb335-117">**Duration**</span></span>](repetitionpattern-duration.md)<br/>                   | <span data-ttu-id="fb335-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fb335-118">Read/write</span></span><br/> | <span data-ttu-id="fb335-119">Ruft ab oder legt fest, wie lange das Muster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="fb335-119">Gets or sets how long the pattern is repeated.</span></span><br/>                                                                                          |
| [<span data-ttu-id="fb335-120">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="fb335-120">**Interval**</span></span>](repetitionpattern-interval.md)<br/>                   | <span data-ttu-id="fb335-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fb335-121">Read/write</span></span><br/> | <span data-ttu-id="fb335-122">Ruft die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="fb335-122">Gets or sets the amount of time between each restart of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="fb335-123">**Stopatdurationend**</span><span class="sxs-lookup"><span data-stu-id="fb335-123">**StopAtDurationEnd**</span></span>](repetitionpattern-stopatdurationend.md)<br/> | <span data-ttu-id="fb335-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fb335-124">Read/write</span></span><br/> | <span data-ttu-id="fb335-125">Ruft einen booleschen Wert ab, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fb335-125">Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb335-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb335-126">Remarks</span></span>

<span data-ttu-id="fb335-127">Wenn Sie eine Wiederholungs Dauer für eine Aufgabe angeben, müssen Sie auch das Wiederholungsintervall angeben.</span><span class="sxs-lookup"><span data-stu-id="fb335-127">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="fb335-128">Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet.</span><span class="sxs-lookup"><span data-stu-id="fb335-128">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="fb335-129">Die fünf Wiederholungen können mithilfe des folgenden Musters definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb335-129">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="fb335-130">Eine Aufgabe beginnt am Anfang der ersten Minute.</span><span class="sxs-lookup"><span data-stu-id="fb335-130">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="fb335-131">Die nächste Aufgabe beginnt am Ende der ersten Minute.</span><span class="sxs-lookup"><span data-stu-id="fb335-131">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="fb335-132">Die nächste Aufgabe beginnt am Ende der zweiten Minute.</span><span class="sxs-lookup"><span data-stu-id="fb335-132">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="fb335-133">Die nächste Aufgabe beginnt am Ende der dritten Minute.</span><span class="sxs-lookup"><span data-stu-id="fb335-133">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="fb335-134">Die nächste Aufgabe beginnt am Ende der vierten Minute.</span><span class="sxs-lookup"><span data-stu-id="fb335-134">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="fb335-135">**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.</span><span class="sxs-lookup"><span data-stu-id="fb335-135">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="fb335-136">Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsmuster mithilfe des [**Wiederholungs**](taskschedulerschema-repetition-triggerbasetype-element.md) Elements des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="fb335-136">When reading or writing XML for a task, the repetition pattern is specified using the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="fb335-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb335-137">Examples</span></span>

<span data-ttu-id="fb335-138">Weitere Informationen und Beispielcode für diese Eigenschaft finden Sie unter [Beispiel für den täglichen Beispiel (Skripterstellung)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="fb335-138">For more information and example code for this property, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb335-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb335-139">Requirements</span></span>



| <span data-ttu-id="fb335-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb335-140">Requirement</span></span> | <span data-ttu-id="fb335-141">Wert</span><span class="sxs-lookup"><span data-stu-id="fb335-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb335-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb335-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fb335-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb335-143">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fb335-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb335-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fb335-145">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb335-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb335-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fb335-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb335-147"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb335-147"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb335-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fb335-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb335-149"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb335-149"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb335-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb335-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb335-151">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="fb335-151">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="fb335-152">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="fb335-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





