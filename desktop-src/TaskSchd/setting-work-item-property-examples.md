---
title: Festlegen von Beispielen für Arbeits Element Eigenschaften
description: Um die Eigenschaften eines Arbeits Elements festzulegen, rufen Sie itaskscheduler aktivieren auf, um die Schnittstelle des Arbeits Element Objekts abzurufen, und rufen Sie dann die entsprechende Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen. Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- Festlegen von Arbeits Element Eigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948956"
---
# <a name="setting-work-item-property-examples"></a><span data-ttu-id="aa398-105">Festlegen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa398-105">Setting Work Item Property Examples</span></span>

<span data-ttu-id="aa398-106">Um die Eigenschaften eines Arbeits Elements festzulegen, rufen Sie [**itaskscheduler:: Aktivierungs**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die-Schnittstelle des Arbeits Element Objekts abzurufen, und rufen Sie dann die entsprechende-Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aa398-106">To set the properties of a work item, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the work item object, then call the appropriate method to set the task property you are interested in.</span></span> <span data-ttu-id="aa398-107">Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="aa398-107">Currently, the only valid work items are tasks.</span></span>

<span data-ttu-id="aa398-108">Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften festgelegt werden, die für alle Arbeitsaufgaben gelten.</span><span class="sxs-lookup"><span data-stu-id="aa398-108">The code examples listed at the bottom of the page show how to set the properties that apply to all work items.</span></span> <span data-ttu-id="aa398-109">Informationen zu anderen Eigenschaften, die für aufgabenspezifisch sind, finden Sie unter [Setting Task Property examples](setting-task-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="aa398-109">For other properties that are unique to tasks, see [Setting Task Property Examples](setting-task-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="aa398-110">Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="aa398-110">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="aa398-111">In den folgenden Beispielen wird das geänderte Objekt immer durch einen [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)-Befehl auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aa398-111">In the following examples, the modified object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="aa398-112">(Die Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine Standard-COM-Schnittstelle, die vom Task-Objekt geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="aa398-112">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="aa398-113">Im folgenden Verfahren wird beschrieben, wie eine Task Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="aa398-113">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="aa398-114">**So legen Sie eine Task Eigenschaft fest**</span><span class="sxs-lookup"><span data-stu-id="aa398-114">**To set a task property**</span></span>

1.  <span data-ttu-id="aa398-115">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa398-115">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="aa398-116">(In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="aa398-116">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="aa398-117">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aa398-117">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="aa398-118">(Beachten Sie, dass Aufgaben derzeit der einzige gültige Typ von Arbeits Element sind.)</span><span class="sxs-lookup"><span data-stu-id="aa398-118">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="aa398-119">Wenden Sie die entsprechende [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode an, um die Eigenschaft festzulegen, an der Sie interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="aa398-119">Call the appropriate [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) method to set the property you are interested in.</span></span> <span data-ttu-id="aa398-120">Beachten Sie, dass die **ischeduledworkitem** -Methoden von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="aa398-120">Note that **IScheduledWorkItem** methods are inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>
4.  <span data-ttu-id="aa398-121">Nennen Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , um das geänderte Task Objekt auf dem Datenträger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="aa398-121">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="aa398-122">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="aa398-122">For a code example of</span></span>                            | <span data-ttu-id="aa398-123">Siehe</span><span class="sxs-lookup"><span data-stu-id="aa398-123">See</span></span>                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa398-124">Festlegen der Kontoinformationen für eine bekannte Aufgabe</span><span class="sxs-lookup"><span data-stu-id="aa398-124">Setting the account information for a known task</span></span> | [<span data-ttu-id="aa398-125">C/C++-Code Beispiel: Festlegen von Informationen zum Task Konto</span><span class="sxs-lookup"><span data-stu-id="aa398-125">C/C++ Code Example: Setting Task Account Information</span></span>](c-c-code-example-setting-task-account-information.md) |
| <span data-ttu-id="aa398-126">Festlegen eines Kommentars für eine bekannte Aufgabe</span><span class="sxs-lookup"><span data-stu-id="aa398-126">Setting the comment of a known task</span></span>              | [<span data-ttu-id="aa398-127">C/C++-Code Beispiel: Festlegen des Aufgaben Kommentars</span><span class="sxs-lookup"><span data-stu-id="aa398-127">C/C++ Code Example: Setting Task Comment</span></span>](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a><span data-ttu-id="aa398-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa398-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa398-129">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa398-129">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 