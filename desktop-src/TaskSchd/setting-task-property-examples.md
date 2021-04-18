---
title: Festlegen von Aufgaben Eigenschafts Beispielen
description: Um die Eigenschaften einer Aufgabe festzulegen, rufen Sie itaskscheduler aktivieren auf, um die Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende ITask-Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- Festlegen von Task Eigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340278"
---
# <a name="setting-task-property-examples"></a><span data-ttu-id="45242-104">Festlegen von Aufgaben Eigenschafts Beispielen</span><span class="sxs-lookup"><span data-stu-id="45242-104">Setting Task Property Examples</span></span>

<span data-ttu-id="45242-105">Um die Eigenschaften einer Aufgabe festzulegen, rufen Sie [**itaskscheduler:: Aktivierungs**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die-Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="45242-105">To set the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the task property you are interested in.</span></span>

<span data-ttu-id="45242-106">Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften festgelegt werden, die für Aufgaben Objekte eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="45242-106">The code examples listed at the bottom of the page show how to set the properties that are unique to task objects.</span></span> <span data-ttu-id="45242-107">Informationen zu anderen [*Arbeits Element*](w.md) Eigenschaften, die auch für Aufgaben gelten, finden Sie unter [Festlegen von Beispielen für Arbeits Element](setting-work-item-property-examples.md)Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45242-107">For other [*work item*](w.md) properties that also apply to tasks, see [Setting Work Item Property Examples](setting-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="45242-108">Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="45242-108">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="45242-109">In den folgenden Beispielen wird das geänderte Task Objekt immer durch einen [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)-Befehl auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="45242-109">In the following examples, the modified task object is always saved to disk by a call to [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="45242-110">(Die Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine Standard-COM-Schnittstelle, die vom Task-Objekt geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="45242-110">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface inherited by the task object.)</span></span>

<span data-ttu-id="45242-111">Im folgenden Verfahren wird beschrieben, wie eine Task Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="45242-111">The following procedure describes how to set a task property.</span></span>

<span data-ttu-id="45242-112">**So legen Sie eine Task Eigenschaft fest**</span><span class="sxs-lookup"><span data-stu-id="45242-112">**To set a task property**</span></span>

1.  <span data-ttu-id="45242-113">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="45242-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="45242-114">(In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="45242-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="45242-115">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="45242-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="45242-116">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="45242-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="45242-117">Wenden Sie die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode an, um die gewünschte Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="45242-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to set the property you are interested in.</span></span>
4.  <span data-ttu-id="45242-118">Nennen Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , um das geänderte Task Objekt auf dem Datenträger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="45242-118">Call [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) to store the modified task object to disk.</span></span>



| <span data-ttu-id="45242-119">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="45242-119">For a code example of</span></span>                                                                                                                                | <span data-ttu-id="45242-120">Siehe</span><span class="sxs-lookup"><span data-stu-id="45242-120">See</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45242-121">Festlegen des Namens der Anwendung, die einer bekannten Aufgabe zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="45242-121">Setting the name of the application associated with a known task</span></span>                                                                                     | [<span data-ttu-id="45242-122">C/C++-Code Beispiel: Festlegen des Anwendungs namens</span><span class="sxs-lookup"><span data-stu-id="45242-122">C/C++ Code Example: Setting Application Name</span></span>](c-c-code-example-setting-application-name.md)   |
| <span data-ttu-id="45242-123">Festlegen der maximalen Laufzeit einer bekannten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="45242-123">Setting the maximum run time of a known task</span></span>                                                                                                         | [<span data-ttu-id="45242-124">C/C++-Code Beispiel: Festlegen von maxruntime</span><span class="sxs-lookup"><span data-stu-id="45242-124">C/C++ Code Example: Setting MaxRunTime</span></span>](c-c-code-example-setting-maxruntime.md)               |
| <span data-ttu-id="45242-125">Löschen aller Befehlszeilenparameter, die einer bekannten Aufgabe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="45242-125">Clearing all command-line parameters associated with a known task</span></span>                                                                                    | [<span data-ttu-id="45242-126">C/C++-Code Beispiel: Festlegen von Aufgaben Parametern</span><span class="sxs-lookup"><span data-stu-id="45242-126">C/C++ Code Example: Setting Task Parameters</span></span>](c-c-code-example-setting-task-parameters.md)     |
| <span data-ttu-id="45242-127">In diesem Beispiel wird die Priorität einer Testaufgabe festgelegt, und anschließend wird die Aufgabe gespeichert.</span><span class="sxs-lookup"><span data-stu-id="45242-127">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="45242-128">In diesem Beispiel wird davon ausgegangen, dass die Testaufgabe bereits auf dem lokalen Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="45242-128">This example assumes that the test task already exists on the local computer.</span></span> | [<span data-ttu-id="45242-129">C/C++-Code Beispiel: Festlegen der Aufgaben Priorität</span><span class="sxs-lookup"><span data-stu-id="45242-129">C/C++ Code Example: Setting Task Priority</span></span>](c-c-code-example-setting-task-priority.md)         |
| <span data-ttu-id="45242-130">Festlegen des [*Arbeitsverzeichnisses*](w.md) einer bekannten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="45242-130">Setting the [*working directory*](w.md) of a known task</span></span>                                                                  | [<span data-ttu-id="45242-131">C/C++-Code Beispiel: Festlegen des Arbeitsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="45242-131">C/C++ Code Example: Setting Working Directory</span></span>](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="45242-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45242-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45242-133">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="45242-133">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 