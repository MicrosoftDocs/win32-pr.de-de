---
title: Beispiel für das Starten einer Aufgabe
description: Um eine Aufgabe zu starten, können Sie die Run-Methode der ITask-Schnittstelle aufzurufen. Run ist eine asynchrone Methode, die versucht, die Aufgabe auszuführen, und gibt zurück, sobald die Aufgabe gestartet wurde. Der Taskplaner-Dienst muss ausgeführt werden, damit diese Methode erfolgreich ausgeführt wird.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341953"
---
# <a name="starting-a-task-example"></a><span data-ttu-id="dd4ce-105">Beispiel für das Starten einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="dd4ce-105">Starting a Task Example</span></span>

<span data-ttu-id="dd4ce-106">Um eine Aufgabe zu starten, können Sie die [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) -Methode der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-106">To start a task, call the [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) method of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="dd4ce-107">**Run** ist eine asynchrone Methode, die versucht, die Aufgabe auszuführen, und gibt zurück, sobald die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-107">**Run** is an asynchronous method that attempts to execute the task and returns as soon as the task has started.</span></span> <span data-ttu-id="dd4ce-108">Der Taskplaner-Dienst muss ausgeführt werden, damit diese Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-108">The Task Scheduler service must be running for this method to succeed.</span></span>

<span data-ttu-id="dd4ce-109">Im folgenden Verfahren wird beschrieben, wie eine Aufgabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-109">The following procedure describes how to start a task.</span></span>

<span data-ttu-id="dd4ce-110">**So starten Sie eine Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="dd4ce-110">**To start a task**</span></span>

1.  <span data-ttu-id="dd4ce-111">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="dd4ce-112">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="dd4ce-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="dd4ce-113">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="dd4ce-114">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="dd4ce-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="dd4ce-115">[**Führen**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) Sie aus, um die Aufgabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-115">Call [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) to start the task.</span></span> <span data-ttu-id="dd4ce-116">Beachten Sie, dass diese Methode von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-116">Note that this method is inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="dd4ce-117">Fortsetzen der Verarbeitung nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-117">Continue processing as needed.</span></span>
5.  <span data-ttu-id="dd4ce-118">Wenden Sie **ITask:: Release** an, um Ressourcen frei [**zugeben und die Initialisierung von**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) com aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="dd4ce-118">Call **ITask::Release** to free resources and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to uninitialize COM.</span></span> <span data-ttu-id="dd4ce-119">In diesem Beispiel wird Release aufgerufen, um den Zeiger auf die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle frei [**zugeben**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="dd4ce-119">This example calls [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to free the pointer to the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="dd4ce-120">(Beachten Sie, dass **Release** eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von **ITask** geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="dd4ce-120">(Note that **Release** is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="dd4ce-121">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="dd4ce-121">For a code example of</span></span>    | <span data-ttu-id="dd4ce-122">Siehe</span><span class="sxs-lookup"><span data-stu-id="dd4ce-122">See</span></span>                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="dd4ce-123">Ausführen einer vorhandenen Aufgabe</span><span class="sxs-lookup"><span data-stu-id="dd4ce-123">Running an existing task</span></span> | [<span data-ttu-id="dd4ce-124">C/C++-Code Beispiel: Starten einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="dd4ce-124">C/C++ Code Example: Starting a Task</span></span>](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="dd4ce-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd4ce-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd4ce-126">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd4ce-126">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 