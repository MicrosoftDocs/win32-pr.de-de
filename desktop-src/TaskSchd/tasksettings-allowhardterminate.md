---
title: Tasksettings. zugewhardend-Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task vom Taskplaner Dienst mithilfe von TerminateProcess beendet werden kann, oder legt ihn fest.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Eigenschaft ' zugeTaskplaner Zuweisung '
- Eigenschaft "zugeTaskplaner Zuweisung", Task Settings-Objekt
- Tasksettings-Objekt Taskplaner, Eigenschaft "Zuweisung beenden"
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742416"
---
# <a name="tasksettingsallowhardterminate-property"></a><span data-ttu-id="8f008-106">Tasksettings. zugewhardend-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8f008-106">TaskSettings.AllowHardTerminate property</span></span>

<span data-ttu-id="8f008-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task vom Taskplaner Dienst mithilfe von [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet werden kann, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="8f008-107">For scripting, gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="8f008-108">Der Dienst versucht, die ausgelaufende Aufgabe zu schließen, indem er die Benachrichtigung zum [**\_ Schließen der WM**](../winmsg/wm-close.md) sendet. wenn die Aufgabe nicht antwortet, wird die Aufgabe nur beendet, wenn diese Eigenschaft auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8f008-108">The service will try to close the running task by sending the [**WM\_CLOSE**](../winmsg/wm-close.md) notification, and if the task does not respond, the task will be terminated only if this property is set to true.</span></span>

<span data-ttu-id="8f008-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8f008-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f008-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f008-110">Syntax</span></span>


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8f008-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8f008-111">Property value</span></span>

<span data-ttu-id="8f008-112">True gibt an, dass die Aufgabe mithilfe von [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8f008-112">If True, the task can be terminated by using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="8f008-113">Wenn der Wert false ist, kann die Aufgabe nicht mithilfe von **TerminateProcess** beendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f008-113">If False, the task cannot be terminated by using **TerminateProcess**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f008-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f008-114">Remarks</span></span>

<span data-ttu-id="8f008-115">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im Element "- [Zuweisung](taskschedulerschema-allowhardterminate-settingstype-element.md) " des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="8f008-115">When reading or writing XML for a task, this setting is specified in the [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f008-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f008-116">Requirements</span></span>



| <span data-ttu-id="8f008-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f008-117">Requirement</span></span> | <span data-ttu-id="8f008-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8f008-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f008-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f008-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8f008-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f008-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8f008-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f008-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8f008-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f008-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8f008-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8f008-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="8f008-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8f008-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8f008-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8f008-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f008-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f008-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f008-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f008-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f008-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="8f008-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

