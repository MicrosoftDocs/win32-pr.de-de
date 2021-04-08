---
title: Tasksettings. Compatibility (Eigenschaft)
description: Ruft bei der Skripterstellung einen ganzzahligen Wert ab, der angibt, mit welcher Version von Taskplaner eine Aufgabe kompatibel ist, oder legt ihn fest
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Kompatibilitäts Eigenschaft Taskplaner
- Kompatibilitäts Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, Compatibility-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740816"
---
# <a name="tasksettingscompatibility-property"></a><span data-ttu-id="3d0e4-106">Tasksettings. Compatibility (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3d0e4-106">TaskSettings.Compatibility property</span></span>

<span data-ttu-id="3d0e4-107">Ruft bei der Skripterstellung einen ganzzahligen Wert ab, der angibt, mit welcher Version von Taskplaner eine Aufgabe kompatibel ist, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="3d0e4-107">For scripting, gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.</span></span>

<span data-ttu-id="3d0e4-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3d0e4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d0e4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d0e4-109">Syntax</span></span>


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a><span data-ttu-id="3d0e4-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3d0e4-110">Property value</span></span>



| <span data-ttu-id="3d0e4-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3d0e4-111">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="3d0e4-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d0e4-112">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <span data-ttu-id="3d0e4-113"><dt>**Aufgabe \_ Kompatibilität \_ bei**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3d0e4-113"><dt>**TASK\_COMPATIBILITY\_AT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="3d0e4-114">Der Task ist mit dem AT-Befehl kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3d0e4-114">The task is compatible with the AT command.</span></span><br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <span data-ttu-id="3d0e4-115"><dt>**Aufgabe \_ Kompatibilität \_ v1**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3d0e4-115"><dt>**TASK\_COMPATIBILITY\_V1**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="3d0e4-116">Der Task ist mit Taskplaner 1,0 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3d0e4-116">The task is compatible with Task Scheduler 1.0.</span></span><br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <span data-ttu-id="3d0e4-117"><dt>**Aufgabe \_ Kompatibilität \_ v2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3d0e4-117"><dt>**TASK\_COMPATIBILITY\_V2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3d0e4-118">Der Task ist mit Taskplaner 2,0 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3d0e4-118">The task is compatible with Task Scheduler 2.0.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d0e4-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d0e4-119">Remarks</span></span>

<span data-ttu-id="3d0e4-120">Die mit der [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) -Eigenschaft festgelegte Task Kompatibilität sollte nur auf Task Compatibility v1 festgelegt werden, \_ \_ Wenn ein Task auf einen Computer mit Windows XP, Windows Server 2003 oder Windows 2000 zugreifen oder diese ändern muss.</span><span class="sxs-lookup"><span data-stu-id="3d0e4-120">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task needs to be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="3d0e4-121">Andernfalls wird empfohlen, dass die Kompatibilität mit Taskplaner 2,0 verwendet wird, da die Aufgabe mehr Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="3d0e4-121">Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.</span></span>

<span data-ttu-id="3d0e4-122">Aufgaben, die mit dem AT-Befehl kompatibel sind, können nur einen Zeit-und Zeit-</span><span class="sxs-lookup"><span data-stu-id="3d0e4-122">Tasks compatible with the AT command can only have one time trigger.</span></span>

<span data-ttu-id="3d0e4-123">Aufgaben, die mit Taskplaner 1,0 kompatibel sind, können nur einen Zeit-oder einen Logon-Triggern oder einen Start-Triggervorgang aufweisen, und der Task kann nur eine ausführbare Aktion aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3d0e4-123">Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.</span></span>

<span data-ttu-id="3d0e4-124">Weitere Informationen zur Aufgaben Kompatibilität finden Sie unter [Neues in Taskplaner](what-s-new-in-task-scheduler.md) und [Aufgaben](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="3d0e4-124">For more information about task compatibility, see [What's New in Task Scheduler](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d0e4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d0e4-125">Requirements</span></span>



| <span data-ttu-id="3d0e4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d0e4-126">Requirement</span></span> | <span data-ttu-id="3d0e4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3d0e4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d0e4-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d0e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3d0e4-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d0e4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3d0e4-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d0e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3d0e4-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d0e4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d0e4-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3d0e4-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d0e4-133"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3d0e4-133"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3d0e4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3d0e4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d0e4-135"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d0e4-135"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d0e4-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d0e4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d0e4-137">**Aufgaben \_ Kompatibilität**</span><span class="sxs-lookup"><span data-stu-id="3d0e4-137">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[<span data-ttu-id="3d0e4-138">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="3d0e4-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





