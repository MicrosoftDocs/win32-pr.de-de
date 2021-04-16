---
title: Tasksettings. multipleinhaltungen (Eigenschaft)
description: Ruft bei der Skripterstellung die Richtlinie ab oder legt Sie fest, die definiert, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Multipleinhaltungen-Eigenschaft Taskplaner
- Multipleinhaltungen-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, multipleinhaltungen (Eigenschaft)
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517468"
---
# <a name="tasksettingsmultipleinstances-property"></a><span data-ttu-id="ebdc6-106">Tasksettings. multipleinhaltungen (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ebdc6-106">TaskSettings.MultipleInstances property</span></span>

<span data-ttu-id="ebdc6-107">Ruft bei der Skripterstellung die Richtlinie ab oder legt Sie fest, die definiert, wie die Taskplaner mehrere Instanzen der Aufgabe behandelt.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-107">For scripting, gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

<span data-ttu-id="ebdc6-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebdc6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebdc6-109">Syntax</span></span>


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a><span data-ttu-id="ebdc6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ebdc6-110">Property value</span></span>

<span data-ttu-id="ebdc6-111">[**Aufgabe \_ Instanzen \_ Richtlinien**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) Konstanten.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-111">[**TASK\_INSTANCES\_POLICY**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) constants.</span></span>



| <span data-ttu-id="ebdc6-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ebdc6-112">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="ebdc6-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ebdc6-113">Meaning</span></span>                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <span data-ttu-id="ebdc6-114"><dt>**Aufgabe \_ Instanzen \_ parallel**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc6-114"><dt>**TASK\_INSTANCES\_PARALLEL**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="ebdc6-115">Startet eine neue-Instanz, während eine vorhandene Instanz der Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-115">Starts a new instance while an existing instance of the task is running.</span></span><br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <span data-ttu-id="ebdc6-116"><dt>**Aufgabe \_ Instanzen \_ Warteschlange**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc6-116"><dt>**TASK\_INSTANCES\_QUEUE**</dt> <dt>1</dt></span></span> </dl>                          | <span data-ttu-id="ebdc6-117">Startet eine neue Instanz der Aufgabe, nachdem alle anderen Instanzen der Aufgabe vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-117">Starts a new instance of the task after all other instances of the task are complete.</span></span><br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <span data-ttu-id="ebdc6-118"><dt>**Aufgabe \_ Instanzen \_ ignorieren \_ neu**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc6-118"><dt>**TASK\_INSTANCES\_IGNORE\_NEW**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="ebdc6-119">Startet keine neue Instanz, wenn eine vorhandene Instanz der Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-119">Does not start a new instance if an existing instance of the task is running.</span></span><br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <span data-ttu-id="ebdc6-120"><dt>**Aufgabe \_ Instanzen, die \_ \_ vorhandene**</dt> <dt>3</dt> Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ebdc6-120"><dt>**TASK\_INSTANCES\_STOP\_EXISTING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="ebdc6-121">Beendet eine vorhandene Instanz der Aufgabe vor dem Starten der neuen Instanz.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-121">Stops an existing instance of the task before it starts new instance.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="ebdc6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebdc6-122">Remarks</span></span>

<span data-ttu-id="ebdc6-123">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**multipleinstancespolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="ebdc6-123">When reading or writing XML for a task, this setting is specified in the [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebdc6-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebdc6-124">Requirements</span></span>



| <span data-ttu-id="ebdc6-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebdc6-125">Requirement</span></span> | <span data-ttu-id="ebdc6-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ebdc6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebdc6-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebdc6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ebdc6-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebdc6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ebdc6-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebdc6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ebdc6-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebdc6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebdc6-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ebdc6-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebdc6-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc6-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ebdc6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ebdc6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebdc6-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebdc6-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebdc6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebdc6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebdc6-136">**Task \_ Instanzen \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="ebdc6-136">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[<span data-ttu-id="ebdc6-137">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ebdc6-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





