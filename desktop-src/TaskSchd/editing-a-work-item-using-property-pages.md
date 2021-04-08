---
title: Bearbeiten eines Arbeits Elements mithilfe von Eigenschaften Seiten
description: Sie können die Eigenschaften eines Arbeits Elements bearbeiten, indem Sie die grafische Benutzeroberfläche verwenden, die vom Taskplaner-Dienst bereitgestellt wird.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- Bearbeiten von Arbeits Elementen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727985"
---
# <a name="editing-a-work-item-using-property-pages"></a><span data-ttu-id="64d0d-104">Bearbeiten eines Arbeits Elements mithilfe von Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="64d0d-104">Editing a Work Item using Property Pages</span></span>

<span data-ttu-id="64d0d-105">Sie können die Eigenschaften eines Arbeits Elements bearbeiten, indem Sie die grafische Benutzeroberfläche verwenden, die vom Taskplaner-Dienst bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64d0d-105">You can edit the properties of a work item by using the graphic user interface provided by the Task Scheduler Service.</span></span> <span data-ttu-id="64d0d-106">(Zurzeit sind die einzigen gültigen Arbeitselemente Tasks.)</span><span class="sxs-lookup"><span data-stu-id="64d0d-106">(Currently, the only valid work items are tasks.)</span></span>

<span data-ttu-id="64d0d-107">Im folgenden Verfahren wird beschrieben, wie eine Aufgabe mithilfe ihrer Eigenschaften Seiten bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="64d0d-107">The following procedure describes how to edit a task using its property pages.</span></span>

<span data-ttu-id="64d0d-108">**So bearbeiten Sie eine Aufgabe mithilfe der zugehörigen Eigenschaften Seiten**</span><span class="sxs-lookup"><span data-stu-id="64d0d-108">**To edit a task using its property pages**</span></span>

1.  <span data-ttu-id="64d0d-109">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="64d0d-109">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="64d0d-110">(In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="64d0d-110">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="64d0d-111">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="64d0d-111">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="64d0d-112">(Beachten Sie, dass Aufgaben derzeit der einzige gültige Typ von Arbeits Element sind.)</span><span class="sxs-lookup"><span data-stu-id="64d0d-112">(Note that tasks are currently the only valid type of work item.)</span></span>
3.  <span data-ttu-id="64d0d-113">Aufrufen von [**ischeduledworkitem:: editworkitem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) , um die Eigenschaften Seiten für den Task anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64d0d-113">Call [**IScheduledWorkItem::EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) to display the property pages for the task.</span></span>
4.  <span data-ttu-id="64d0d-114">Bearbeiten Sie die Eigenschaften der Aufgabe nach Bedarf, und klicken Sie dann auf OK, um die neuen Werte zu übernehmen und die angezeigten Eigenschaften Seiten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="64d0d-114">Edit the properties of the task as needed, then click OK to accept the new values and remove the displayed property pages.</span></span>



| <span data-ttu-id="64d0d-115">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="64d0d-115">For a code example of</span></span>                                                                                      | <span data-ttu-id="64d0d-116">Siehe</span><span class="sxs-lookup"><span data-stu-id="64d0d-116">See</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="64d0d-117">Anzeigen der Eigenschaften Seiten für eine bekannte Aufgabe und ermöglichen der Bearbeitung der Eigenschaften der Arbeitsaufgabe durch einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="64d0d-117">Displaying the property pages for a known task and allowing a user to edit the properties of the work item</span></span> | [<span data-ttu-id="64d0d-118">C/C++-Code Beispiel: Bearbeiten eines Arbeits Elements</span><span class="sxs-lookup"><span data-stu-id="64d0d-118">C/C++ Code Example: Editing a Work Item</span></span>](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a><span data-ttu-id="64d0d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64d0d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d0d-120">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="64d0d-120">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 