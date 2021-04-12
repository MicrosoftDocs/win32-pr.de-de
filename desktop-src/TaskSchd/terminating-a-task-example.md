---
title: Beispiel für das Beenden einer Aufgabe
description: Sie können eine Aufgabe beenden, während Sie ausgeführt wird, indem Sie ischeduledworkitem beenden aufrufen.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209300"
---
# <a name="terminating-a-task-example"></a><span data-ttu-id="866b8-103">Beispiel für das Beenden einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="866b8-103">Terminating a Task Example</span></span>

<span data-ttu-id="866b8-104">Sie können eine Aufgabe beenden, während Sie ausgeführt wird, indem Sie [**ischeduledworkitem:: beenden**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="866b8-104">You can terminate a task while it is running by calling [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).</span></span>

<span data-ttu-id="866b8-105">Im folgenden Verfahren wird beschrieben, wie eine Aufgabe beendet wird, wenn Sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="866b8-105">The following procedure describes how to terminate a task if it is running.</span></span>

<span data-ttu-id="866b8-106">**So beenden Sie einen Task, wenn er ausgeführt wird**</span><span class="sxs-lookup"><span data-stu-id="866b8-106">**To terminate a task if it is running**</span></span>

1.  <span data-ttu-id="866b8-107">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="866b8-107">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="866b8-108">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="866b8-108">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="866b8-109">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="866b8-109">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="866b8-110">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="866b8-110">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="866b8-111">Aufrufen von **ITask:: GetStatus** , um herauszufinden, ob die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="866b8-111">Call **ITask::GetStatus** to find out if the task is running.</span></span> <span data-ttu-id="866b8-112">(Beachten Sie, dass [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="866b8-112">(Note that [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="866b8-113">Überprüfen Sie den Status des Tasks, und nennen Sie dann **ITask:: beenden** , wenn die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="866b8-113">Check the status of the task and then call **ITask::Terminate** if the task is running.</span></span> <span data-ttu-id="866b8-114">(Beachten Sie, dass " [**Beenden**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) " eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="866b8-114">(Note that [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="866b8-115">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="866b8-115">For a code example of</span></span>                | <span data-ttu-id="866b8-116">Siehe</span><span class="sxs-lookup"><span data-stu-id="866b8-116">See</span></span>                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="866b8-117">Überprüfen des Status einer bekannten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="866b8-117">Verifying the status of a known task</span></span> | [<span data-ttu-id="866b8-118">C/C++-Code Beispiel: Beenden einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="866b8-118">C/C++ Code Example: Terminating a Task</span></span>](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a><span data-ttu-id="866b8-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="866b8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="866b8-120">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="866b8-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 