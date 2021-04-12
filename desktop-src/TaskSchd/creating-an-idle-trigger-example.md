---
title: Erstellen eines Beispiels für einen Leerlauf-Timeout
description: Zum Erstellen eines Leerlauf-Auslösers müssen Sie beim Erstellen des Auslösers einen Leerlauf-Auslösers angeben und die Leerlaufzeit für den Task festlegen. Informationen zu Bedingungen im Leerlauf finden Sie Unteraufgaben im Leerlauf.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315926"
---
# <a name="creating-an-idle-trigger-example"></a><span data-ttu-id="468b2-104">Erstellen eines Beispiels für einen Leerlauf-Timeout</span><span class="sxs-lookup"><span data-stu-id="468b2-104">Creating an Idle Trigger Example</span></span>

<span data-ttu-id="468b2-105">Zum Erstellen eines Leerlauf-Auslösers müssen Sie beim Erstellen des Auslösers einen Leerlauf-Auslösers angeben und die Leerlaufzeit für den Task festlegen.</span><span class="sxs-lookup"><span data-stu-id="468b2-105">To create an idle trigger, you must specify an idle trigger when you create the trigger, and you must set the idle time for the task.</span></span> <span data-ttu-id="468b2-106">Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="468b2-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="468b2-107">Nachdem Sie den im Leerlauf befindlichen-Befehl erstellt haben, nennen Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , um den neuen-Befehl auf dem Datenträger</span><span class="sxs-lookup"><span data-stu-id="468b2-107">After creating the idle trigger, call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to save the new trigger to disk.</span></span>

<span data-ttu-id="468b2-108">Im folgenden Verfahren wird beschrieben, wie Sie einen Leerlauf-Auslösers für eine bekannte Aufgabe erstellen.</span><span class="sxs-lookup"><span data-stu-id="468b2-108">The following procedure describes how to create an idle trigger for a known task.</span></span>

<span data-ttu-id="468b2-109">**So erstellen Sie einen Leerlauf-Auslösers für eine bekannte Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="468b2-109">**To create an idle trigger for a known task**</span></span>

1.  <span data-ttu-id="468b2-110">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="468b2-110">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="468b2-111">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="468b2-111">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="468b2-112">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="468b2-112">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="468b2-113">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="468b2-113">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="468b2-114">Ruft [**setidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) auf, um festzulegen, wie lange das System im Leerlauf bleiben muss, bevor der Trigger ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="468b2-114">Call [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) to set how long the system must remain idle before the trigger will fire.</span></span> <span data-ttu-id="468b2-115">(Beachten Sie, dass "\* **tidlewait** " von " [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)" geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="468b2-115">(Note that **SetIdleWait** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="468b2-116">Definieren Sie die [**Task- \_ auslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) , und rufen Sie zum Erstellen des Leerlauf- [**Auslösers**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) den "</span><span class="sxs-lookup"><span data-stu-id="468b2-116">Define the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure and call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create the idle trigger.</span></span> <span data-ttu-id="468b2-117">(Beachten Sie, dass " **kreatetransform** " von " [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)" geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="468b2-117">(Note that **CreateTrigger** is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
5.  <span data-ttu-id="468b2-118">Speichern Sie die Aufgabe mit dem neuen Leerlauf-Auslösung auf dem Datenträger mithilfe von [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="468b2-118">Save the task with the new idle trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="468b2-119">(Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist eine von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützte Standard-COM-Schnittstelle.)</span><span class="sxs-lookup"><span data-stu-id="468b2-119">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
6.  <span data-ttu-id="468b2-120">Wenden Sie **ITask:: Release** an, um alle Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="468b2-120">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="468b2-121">(Beachten Sie, dass [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="468b2-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="468b2-122">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="468b2-122">For a code example of</span></span>                         | <span data-ttu-id="468b2-123">Siehe</span><span class="sxs-lookup"><span data-stu-id="468b2-123">See</span></span>                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="468b2-124">Erstellen eines Leerlauf-Auslösers für eine vorhandene Aufgabe</span><span class="sxs-lookup"><span data-stu-id="468b2-124">Creating an idle trigger for an existing task</span></span> | [<span data-ttu-id="468b2-125">C/C++-Code Beispiel: Erstellen eines Leerlauf-Auslösers</span><span class="sxs-lookup"><span data-stu-id="468b2-125">C/C++ Code Example: Creating an Idle Trigger</span></span>](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="468b2-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="468b2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="468b2-127">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="468b2-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 