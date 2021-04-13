---
title: Erstellen eines neuen-Auslösers
description: Zum Erstellen eines-Auslösers müssen Sie drei Schnittstellen verwenden.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390679"
---
# <a name="creating-a-new-trigger"></a><span data-ttu-id="f1197-103">Erstellen eines neuen-Auslösers</span><span class="sxs-lookup"><span data-stu-id="f1197-103">Creating a New Trigger</span></span>

<span data-ttu-id="f1197-104">Zum Erstellen eines-Auslösers müssen Sie drei Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f1197-104">To create a trigger you must use three interfaces.</span></span> <span data-ttu-id="f1197-105">[**Ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) stellt die [**ischeduledworkitem:: up-auslösermethode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) zum Erstellen des-auslöserobjekts bereit. [**itaskausgelöst**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) stellt die [**itaskausgelöst:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) -Methode zum Festlegen der Kriterien für den-Befehl bereit, und die COM-Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) bietet eine **Save** -Methode zum Speichern des neuen-Auslösers</span><span class="sxs-lookup"><span data-stu-id="f1197-105">[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) provides the [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) method for creating the trigger object, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) provides the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method for setting the criteria for the trigger, and the COM interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) provides a **Save** method for saving the new trigger to disk.</span></span>

<span data-ttu-id="f1197-106">Im folgenden Verfahren wird das Erstellen eines neuen-Auslösers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1197-106">The following procedure describes how to create a new trigger.</span></span>

<span data-ttu-id="f1197-107">**So erstellen Sie einen neuen-Auslösung**</span><span class="sxs-lookup"><span data-stu-id="f1197-107">**To create a new trigger**</span></span>

1.  <span data-ttu-id="f1197-108">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1197-108">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="f1197-109">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="f1197-109">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="f1197-110">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f1197-110">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="f1197-111">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="f1197-111">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="f1197-112">Rufen [**Sie**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) zum Erstellen eines-auslöserobjekts "up" auf.</span><span class="sxs-lookup"><span data-stu-id="f1197-112">Call [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) to create a trigger object.</span></span> <span data-ttu-id="f1197-113">(Beachten Sie, dass " [**kreatetransform**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) " von " [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)" geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="f1197-113">(Note that [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) is inherited from [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)</span></span>
4.  <span data-ttu-id="f1197-114">Definieren Sie eine [**Aufgaben \_ auslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="f1197-114">Define a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="f1197-115">Beachten Sie, dass die Member "wbeginday", "wbeginmonth" und "wbeginyear" des **Task- \_ Auslösers** auf einen gültigen Tag, Monat und Jahr festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f1197-115">Note that wBeginDay, wBeginMonth, and wBeginYear members of **TASK\_TRIGGER** must be set to a valid day, month, and year respectively.</span></span>
5.  <span data-ttu-id="f1197-116">Wenden Sie [**itaskausgelöst:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) an, um die Auslöserkriterien festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f1197-116">Call [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) to set the trigger criteria.</span></span>
6.  <span data-ttu-id="f1197-117">Speichern Sie die Aufgabe mit dem neuen-Vorgang auf dem Datenträger mithilfe von [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span><span class="sxs-lookup"><span data-stu-id="f1197-117">Save the task with the new trigger to disk using [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="f1197-118">(Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist eine von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützte Standard-COM-Schnittstelle.)</span><span class="sxs-lookup"><span data-stu-id="f1197-118">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
7.  <span data-ttu-id="f1197-119">Ruft die [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf, um alle Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f1197-119">Call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release all resources.</span></span> <span data-ttu-id="f1197-120">(Beachten Sie, dass **Release** eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="f1197-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="f1197-121">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="f1197-121">For a code example of</span></span>                       | <span data-ttu-id="f1197-122">Siehe</span><span class="sxs-lookup"><span data-stu-id="f1197-122">See</span></span>                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1197-123">Erstellen eines neuen-Auslösers für eine vorhandene Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f1197-123">Creating a new trigger for an existing task</span></span> | [<span data-ttu-id="f1197-124">C/C++-Code Beispiel: Erstellen eines Aufgaben Auslösers</span><span class="sxs-lookup"><span data-stu-id="f1197-124">C/C++ Code Example: Creating a Task Trigger</span></span>](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a><span data-ttu-id="f1197-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1197-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1197-126">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1197-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 