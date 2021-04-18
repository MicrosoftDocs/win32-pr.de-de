---
title: Abrufen von Aufgaben Eigenschafts Beispielen
description: Um die Eigenschaften einer Aufgabe abzurufen, rufen Sie itaskscheduler aktivieren auf, um die Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende ITask-Methode auf, um die gewünschte Aufgaben Eigenschaft abzurufen.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- Abrufen von Task Eigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316047"
---
# <a name="retrieving-task-property-examples"></a><span data-ttu-id="0b648-104">Abrufen von Aufgaben Eigenschafts Beispielen</span><span class="sxs-lookup"><span data-stu-id="0b648-104">Retrieving Task Property Examples</span></span>

<span data-ttu-id="0b648-105">Rufen Sie zum Abrufen der Eigenschaften einer Aufgabe [**itaskscheduler:: Aktivierungs**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode auf, um die gewünschte Aufgaben Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b648-105">To retrieve the properties of a task, call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get retrieve the interface of the task object, then call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the task property that you are interested in.</span></span> <span data-ttu-id="0b648-106">Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die verschiedenen Task Eigenschaften abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0b648-106">The code examples listed at the bottom of the page show how to retrieve the different task properties.</span></span>

<span data-ttu-id="0b648-107">Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften abgerufen werden, die für Aufgaben Objekte eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="0b648-107">The code examples listed at the bottom of the page show how to retrieve the properties that are unique to task objects.</span></span> <span data-ttu-id="0b648-108">Weitere Informationen zu anderen [*Arbeits Element*](w.md) Eigenschaften, die auch für Aufgaben gelten, finden Sie unter [Abrufen von Beispielen für Arbeitselemente](retrieving-work-item-property-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0b648-108">For other [*work item*](w.md) properties that also apply to tasks, see [Retrieving Work Item Examples](retrieving-work-item-property-examples.md).</span></span>

> [!Note]  
> <span data-ttu-id="0b648-109">Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b648-109">In the following code example, all interfaces are released after they are no longer needed.</span></span>

 

<span data-ttu-id="0b648-110">Beachten Sie Folgendes: Wenn Sie eine Zeichen folgen Eigenschaft (z. b. den Anwendungsnamen, Parameter oder das Arbeitsverzeichnis) abrufen, müssen Sie " [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, um den für die zurückgegebenen Zeichenfolge zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0b648-110">Note that if you are retrieving a string property (such as the application name, parameters, or working directory), you must call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>

<span data-ttu-id="0b648-111">Im folgenden Verfahren wird beschrieben, wie eine Task Eigenschaft abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0b648-111">The following procedure describes how to retrieve a task property.</span></span>

<span data-ttu-id="0b648-112">**So rufen Sie eine Task Eigenschaft ab**</span><span class="sxs-lookup"><span data-stu-id="0b648-112">**To retrieve a task property**</span></span>

1.  <span data-ttu-id="0b648-113">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="0b648-113">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="0b648-114">(In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="0b648-114">(These examples assume that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="0b648-115">Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b648-115">Call [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) to get the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface of the task object.</span></span> <span data-ttu-id="0b648-116">(Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)</span><span class="sxs-lookup"><span data-stu-id="0b648-116">(Note that this example gets the "Test Task" task.)</span></span>
3.  <span data-ttu-id="0b648-117">Rufen Sie die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode auf, um die gewünschte Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0b648-117">Call the appropriate [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) method to retrieve the property you are interested in.</span></span>
4.  <span data-ttu-id="0b648-118">Verarbeiten Sie die Eigenschaft nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="0b648-118">Process the property as needed.</span></span> <span data-ttu-id="0b648-119">(In diesen Beispielen wird die-Eigenschaft auf dem Bildschirm gedruckt.)</span><span class="sxs-lookup"><span data-stu-id="0b648-119">(These examples print the property to the screen.)</span></span>
5.  <span data-ttu-id="0b648-120">Wenn die zurückgegebene Eigenschaft eine Zeichenfolge ist, können Sie [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) aufrufen, um den für die zurückgegebenen Zeichenfolge belegten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0b648-120">If the returned property is a string, call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory allocated for the returned string.</span></span>



| <span data-ttu-id="0b648-121">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="0b648-121">For a code example of</span></span>                                                                                                                           | <span data-ttu-id="0b648-122">Siehe</span><span class="sxs-lookup"><span data-stu-id="0b648-122">See</span></span>                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b648-123">Abrufen des Namens der Anwendung, die einer bestimmten Aufgabe zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="0b648-123">Retrieving the name of the application associated with a given task</span></span>                                                                             | [<span data-ttu-id="0b648-124">C/C++-Code Beispiel: Abrufen des Aufgaben Anwendungs namens</span><span class="sxs-lookup"><span data-stu-id="0b648-124">C/C++ Code Example: Retrieving the Task Application Name</span></span>](c-c-code-example-retrieving-the-task-application-name.md)   |
| <span data-ttu-id="0b648-125">Abrufen der maximalen Zeitspanne, die der Task ausgeführt werden kann, und Anzeigen dieser Zahl auf dem Bildschirm</span><span class="sxs-lookup"><span data-stu-id="0b648-125">Retrieving the maximum amount of time the task can run and displaying that number on the screen</span></span>                                                 | [<span data-ttu-id="0b648-126">C/C++-Code Beispiel: Abrufen der Aufgabe maxruntime</span><span class="sxs-lookup"><span data-stu-id="0b648-126">C/C++ Code Example: Retrieving the Task MaxRunTime</span></span>](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| <span data-ttu-id="0b648-127">Abrufen der Parameter Zeichenfolge, die ausgeführt wird, wenn die Aufgabe ausgeführt wird und diese Zeichenfolge auf dem Bildschirm anzeigt</span><span class="sxs-lookup"><span data-stu-id="0b648-127">Retrieving the parameter string that is executed when the task is run and displaying that string on the screen</span></span>                                  | [<span data-ttu-id="0b648-128">C/C++-Code Beispiel: Abrufen von Aufgaben Parametern</span><span class="sxs-lookup"><span data-stu-id="0b648-128">C/C++ Code Example: Retrieving Task Parameters</span></span>](c-c-code-example-retrieving-task-parameters.md)                       |
| <span data-ttu-id="0b648-129">Abrufen der [*Prioritätsstufe*](p.md) der Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0b648-129">Retrieving the [*priority level*](p.md) of the task</span></span>                                                                    | [<span data-ttu-id="0b648-130">C/C++-Code Beispiel: Abrufen der Aufgaben Priorität</span><span class="sxs-lookup"><span data-stu-id="0b648-130">C/C++ Code Example: Retrieving Task Priority</span></span>](c-c-code-example-retrieving-task-priority.md)                           |
| <span data-ttu-id="0b648-131">Abrufen des [*Arbeitsverzeichnisses*](w.md) einer Aufgabe und Anzeigen des Pfads zum Arbeitsverzeichnis auf dem Bildschirm</span><span class="sxs-lookup"><span data-stu-id="0b648-131">Retrieving the [*working directory*](w.md) of a task and displaying the path to the working directory on the screen</span></span> | [<span data-ttu-id="0b648-132">C/C++-Code Beispiel: Abrufen des Aufgaben Arbeitsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="0b648-132">C/C++ Code Example: Retrieving the Task Working Directory</span></span>](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0b648-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b648-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b648-134">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b648-134">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 