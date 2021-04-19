---
title: Beispiel für das Abrufen von Beispiel Zeichen folgen
description: Abhängig vom Typ des Objekts, mit dem Sie arbeiten, können Sie die auslöserzeichenfolgen eines bekannten Auslösers mithilfe der ischeduledworkitem-Schnittstelle oder der itaskauslöst-Schnittstelle abrufen.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- Abrufen von Auslöse Zeichen folgen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341736"
---
# <a name="retrieving-trigger-strings-example"></a><span data-ttu-id="d4c1c-104">Beispiel für das Abrufen von Beispiel Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="d4c1c-104">Retrieving Trigger Strings Example</span></span>

<span data-ttu-id="d4c1c-105">Abhängig vom Typ des Objekts, mit dem Sie arbeiten, können Sie die auslöserzeichenfolgen eines bekannten Auslösers mithilfe der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle oder der [**itaskauslöst**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-105">You can retrieve the trigger strings of a known trigger using the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) or [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface, depending on the type of object you are working with.</span></span>

<span data-ttu-id="d4c1c-106">Verwenden Sie beim Arbeiten mit einem [*Task Objekt*](t.md)die Methoden der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle, um die auslöserzeichenfolgen einer Arbeitsaufgabe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-106">When working with a [*task object*](t.md), use the methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface to retrieve the trigger strings of a work item.</span></span>

<span data-ttu-id="d4c1c-107">Wenn Sie mit einem [*taskauslöserobjekt*](t.md)arbeiten, verwenden Sie die-Methoden der [**itaskauslöserschnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , um die auslösende Zeichenfolge des Auslösers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-107">When you are working with a [*task trigger object*](t.md), use the methods of the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger string of the trigger.</span></span>

<span data-ttu-id="d4c1c-108">Im folgenden Beispiel wird gezeigt, wie [**ischeduledworkitem:: gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) verwendet wird, um die Zeichen folgen aller mit einer bekannten Aufgabe verknüpften Trigger anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-108">The following example shows how to use [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) to display the strings of all triggers associated with a known task.</span></span>

<span data-ttu-id="d4c1c-109">Im folgenden Verfahren wird beschrieben, wie die auslöserzeichenfolgen einer Aufgabe abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-109">The following procedure describes how to retrieve the trigger strings of a task.</span></span>

<span data-ttu-id="d4c1c-110">**So rufen Sie die Auslöse Zeichenfolgen einer Aufgabe ab**</span><span class="sxs-lookup"><span data-stu-id="d4c1c-110">**To retrieve the trigger strings of a task**</span></span>

1.  <span data-ttu-id="d4c1c-111">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-111">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="d4c1c-112">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="d4c1c-112">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="d4c1c-113">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-113">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="d4c1c-114">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="d4c1c-114">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="d4c1c-115">Aufrufen von **ITask:: gettriggercount** , um herauszufinden, wie viele Trigger einer Aufgabe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-115">Call **ITask::GetTriggerCount** to find out how many triggers are associated with a task.</span></span> <span data-ttu-id="d4c1c-116">(Beachten Sie, dass [**gettriggercount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="d4c1c-116">(Note that [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
4.  <span data-ttu-id="d4c1c-117">Zeigen Sie die auslöserzeichenfolgen an, und rufen Sie **ITask:: gettriggerstring** für jeden der Aufgabe zugeordneten Befehl auf.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-117">Display the trigger strings, calling **ITask::GetTriggerString** for each trigger associated with the task.</span></span> <span data-ttu-id="d4c1c-118">(Beachten Sie, dass [**gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="d4c1c-118">(Note that [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) is an [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>
5.  <span data-ttu-id="d4c1c-119">Alle Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-119">Release all resources.</span></span> <span data-ttu-id="d4c1c-120">Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) zum Freigeben der Trigger-Zeichen folgen und **ITask:: Release** zum Freigeben der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d4c1c-120">Call [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the trigger strings and **ITask::Release** to release the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span> <span data-ttu-id="d4c1c-121">(Beachten Sie, dass [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von **ITask** geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="d4c1c-121">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by **ITask**.)</span></span>



| <span data-ttu-id="d4c1c-122">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="d4c1c-122">For a code example of</span></span>                                                         | <span data-ttu-id="d4c1c-123">Siehe</span><span class="sxs-lookup"><span data-stu-id="d4c1c-123">See</span></span>                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c1c-124">Abrufen einer triggerzeichenfolge für alle Trigger, die einer bekannten Aufgabe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="d4c1c-124">Retrieving a trigger string for all the triggers associated with a known task</span></span> | [<span data-ttu-id="d4c1c-125">Code Beispiel: Abrufen von auslöserzeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="d4c1c-125">Code Example: Retrieving Trigger Strings</span></span>](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a><span data-ttu-id="d4c1c-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4c1c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4c1c-127">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4c1c-127">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 