---
title: Erstellen einer Aufgabe mit NewWorkItem-Beispiel
description: Wenn Sie einen Task erstellen, verwenden Sie die beiden Taskplaner-Schnittstellen itaskscheduler und ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- Erstellen von Arbeits Elementen Taskplaner
- Arbeitselemente Taskplaner, Erstellen von Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315819"
---
# <a name="creating-a-task-using-newworkitem-example"></a><span data-ttu-id="34c46-105">Erstellen einer Aufgabe mit NewWorkItem-Beispiel</span><span class="sxs-lookup"><span data-stu-id="34c46-105">Creating a Task Using NewWorkItem Example</span></span>

<span data-ttu-id="34c46-106">Beim Erstellen einer Aufgabe verwenden Sie zwei Taskplaner Schnittstellen: [**itaskscheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) und [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span><span class="sxs-lookup"><span data-stu-id="34c46-106">When creating a task, you will use two Task Scheduler interfaces: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) and [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span> <span data-ttu-id="34c46-107">Sie müssen einen eindeutigen Namen für den Task, den Klassen Bezeichner des Task-Objekts und den Schnittstellen Bezeichner " **ITask**" angeben.</span><span class="sxs-lookup"><span data-stu-id="34c46-107">You must provide a unique name for the task, the class identifier of the task object, and the interface identifier of **ITask**.</span></span> <span data-ttu-id="34c46-108">Der Klassen Bezeichner und der Schnittstellen Bezeichner werden im folgenden Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="34c46-108">The class identifier and interface identifier are shown in the code example following this topic.</span></span>

> [!Note]  
> <span data-ttu-id="34c46-109">Sie können auch einen Task erstellen, indem Sie [**itaskscheduler:: addworkitem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="34c46-109">You can also create a task by calling [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem).</span></span> <span data-ttu-id="34c46-110">Wenn Sie diese Route verwenden, liegt es in ihrer Verantwortung, eine Instanz des **Task** -Objekts (das die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützt) zu erstellen und dann die Aufgabe mit dem Namen hinzuzufügen, den Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="34c46-110">When you take this route, it is your responsibility to create an instance of the **Task** object (which supports the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface) and then add the task with the name you supply.</span></span>

 

> [!Note]  
> <span data-ttu-id="34c46-111">Standardmäßig können nur Mitglieder der Gruppe "Administratoren", "Sicherungs-Operatoren" oder "Server Operatoren" auf Windows Server 2003 Aufgaben erstellen.</span><span class="sxs-lookup"><span data-stu-id="34c46-111">By default, only a member of the Administrators, Backup Operators, or Server Operators group can create tasks on Windows Server 2003.</span></span> <span data-ttu-id="34c46-112">Ein Mitglied der Gruppe "Administratoren" kann die Sicherheits Beschreibung des Windows- \\ Task Ordners ändern, damit andere Aufgaben erstellen können.</span><span class="sxs-lookup"><span data-stu-id="34c46-112">A member of the Administrators group may change the security descriptor of the Windows\\Task folder to let others create tasks.</span></span>

 

<span data-ttu-id="34c46-113">Der Name, den Sie für die Aufgabe angeben, muss innerhalb des Ordners für geplante Aufgaben eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="34c46-113">The name you supply for the task must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="34c46-114">Wenn bereits eine Aufgabe mit dem gleichen Namen vorhanden ist, gibt [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) eine Fehler \_ Datei \_ vorhanden.</span><span class="sxs-lookup"><span data-stu-id="34c46-114">If a task with the same name already exists, [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) returns ERROR\_FILE\_EXISTS.</span></span> <span data-ttu-id="34c46-115">Wenn Sie diesen Rückgabewert erhalten, geben Sie einen anderen Namen an, und versuchen Sie erneut, die Aufgabe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34c46-115">If you get this return value, you should specify a different name and attempt to create the task again.</span></span>

<span data-ttu-id="34c46-116">Im folgenden Verfahren wird beschrieben, wie eine neue Arbeits Element Aufgabe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="34c46-116">The following procedure describes how to create a new work item task.</span></span>

<span data-ttu-id="34c46-117">**So erstellen Sie eine neue Arbeits Element Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="34c46-117">**To create a new work item task**</span></span>

1.  <span data-ttu-id="34c46-118">Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts.</span><span class="sxs-lookup"><span data-stu-id="34c46-118">Call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) to initialize the COM library and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get a Task Scheduler object.</span></span> <span data-ttu-id="34c46-119">(In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="34c46-119">(This example assumes that the Task Scheduler service is running.)</span></span>
2.  <span data-ttu-id="34c46-120">Rufen Sie [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) auf, um eine neue Aufgabe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34c46-120">Call [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) to create a new task.</span></span> <span data-ttu-id="34c46-121">(Diese Methode gibt einen Zeiger auf eine [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle zurück.)</span><span class="sxs-lookup"><span data-stu-id="34c46-121">(This method returns a pointer to an [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.)</span></span>
3.  <span data-ttu-id="34c46-122">Speichern Sie die neue Aufgabe auf einem Datenträger, indem Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="34c46-122">Save the new task to disk by calling [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save).</span></span> <span data-ttu-id="34c46-123">(Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist eine von der **ITask** -Schnittstelle unterstützte Standard-COM-Schnittstelle.)</span><span class="sxs-lookup"><span data-stu-id="34c46-123">(The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface supported by the **ITask** interface.)</span></span>
4.  <span data-ttu-id="34c46-124">Wenden Sie **ITask:: Release** an, um alle Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="34c46-124">Call **ITask::Release** to release all resources.</span></span> <span data-ttu-id="34c46-125">(Beachten Sie, dass [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)</span><span class="sxs-lookup"><span data-stu-id="34c46-125">(Note that [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) is an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method inherited by [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)</span></span>



| <span data-ttu-id="34c46-126">Ein Codebeispiel für</span><span class="sxs-lookup"><span data-stu-id="34c46-126">For a code example of</span></span>  | <span data-ttu-id="34c46-127">Siehe</span><span class="sxs-lookup"><span data-stu-id="34c46-127">See</span></span>                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c46-128">Erstellen einer einzelnen Aufgabe</span><span class="sxs-lookup"><span data-stu-id="34c46-128">Creating a single task</span></span> | [<span data-ttu-id="34c46-129">C/C++-Code Beispiel: Erstellen einer Aufgabe mit NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="34c46-129">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a><span data-ttu-id="34c46-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34c46-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34c46-131">Taskplaner 1,0-Beispiele</span><span class="sxs-lookup"><span data-stu-id="34c46-131">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 