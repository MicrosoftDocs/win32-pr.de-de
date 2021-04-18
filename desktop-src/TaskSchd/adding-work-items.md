---
title: Hinzufügen von Arbeits Elementen
description: Es gibt zwei Möglichkeiten, dem geplanten tasksordner Arbeitselemente hinzuzufügen. Sie können ein neues Arbeits Element innerhalb des Ordners erstellen, oder Sie können dem Ordner ein vorhandenes Arbeits Element hinzufügen.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- Arbeitselemente Taskplaner, hinzufügen
- Aufgaben Taskplaner, hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338598"
---
# <a name="adding-work-items"></a><span data-ttu-id="dfa18-106">Hinzufügen von Arbeits Elementen</span><span class="sxs-lookup"><span data-stu-id="dfa18-106">Adding Work Items</span></span>

<span data-ttu-id="dfa18-107">Es gibt zwei Möglichkeiten, dem [*geplanten tasksordner*](s.md) [*Arbeitselemente*](w.md) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dfa18-107">There are two ways to add [*work items*](w.md) to the [*Scheduled Tasksfolder*](s.md).</span></span> <span data-ttu-id="dfa18-108">Sie können ein neues Arbeits Element innerhalb des Ordners erstellen, oder Sie können dem Ordner ein vorhandenes Arbeits Element hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dfa18-108">You can create a new work item within the folder, or you can add an existing work item to the folder.</span></span>

> [!Note]  
> <span data-ttu-id="dfa18-109">Derzeit können dem Ordner "geplante Aufgaben" nur Aufgaben Objekte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="dfa18-109">Currently, only task objects can be added to the Scheduled Tasks folder.</span></span> <span data-ttu-id="dfa18-110">Wenn Sie eine Aufgabe hinzufügen, müssen Sie die Bezeichner für die Aufgaben Klasse und die Aufgaben Schnittstelle [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)kennen.</span><span class="sxs-lookup"><span data-stu-id="dfa18-110">When adding a task, you must know the identifiers for the task class and the task interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).</span></span>

 

<span data-ttu-id="dfa18-111">Sie erstellen neue Arbeitselemente, indem Sie die [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dfa18-111">You create new work items by calling the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method.</span></span> <span data-ttu-id="dfa18-112">Diese Methode erstellt ein neues Arbeits Element Objekt mit dem von Ihnen angegebenen Namen und fügt das Arbeits Element dem Ordner "geplante Aufgaben" hinzu.</span><span class="sxs-lookup"><span data-stu-id="dfa18-112">This method creates a new work item object using the name that you provide and adds the work item to the Scheduled Tasks folder.</span></span> <span data-ttu-id="dfa18-113">Wenn Sie ein neues Arbeits Element erstellen, ordnet der Taskplaner den für das neue-Objekt erforderlichen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="dfa18-113">When you create a new work item, the Task Scheduler allocates the memory that is required for the new object.</span></span>

<span data-ttu-id="dfa18-114">Um dem Ordner "geplante Aufgaben" vorhandene Arbeitselemente hinzuzufügen, müssen Sie die [**itaskscheduler:: addworkitem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dfa18-114">To add existing work items to the Scheduled Tasks folder, call the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method.</span></span> <span data-ttu-id="dfa18-115">Wenn Sie diese Methode aufgerufen haben, müssen Sie das-Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="dfa18-115">When you call this method, you must create the object.</span></span>

<span data-ttu-id="dfa18-116">Die Namen, die Sie für Arbeitselemente angeben, müssen innerhalb des Ordners für geplante Aufgaben eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="dfa18-116">The names you supply for work items must be unique within the Scheduled Tasks folder.</span></span> <span data-ttu-id="dfa18-117">Wenn eine Arbeitsaufgabe mit dem gleichen Namen bereits vorhanden ist, wenn Sie entweder die [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) -Methode oder die [**itaskscheduler:: addworkitem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) -Methode aufruft, gibt die Methode eine **Fehler Datei "ist \_ \_ vorhanden** " zurück.</span><span class="sxs-lookup"><span data-stu-id="dfa18-117">If a work item with the same name already exists when you call either the [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) method or the [**ITaskScheduler::AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) method, the method returns an **ERROR\_FILE\_EXISTS** error.</span></span> <span data-ttu-id="dfa18-118">Weitere Informationen finden Sie unter [Erstellen einer Aufgabe mit NewWorkItem-Beispiel](creating-a-task-using-newworkitem-example.md).</span><span class="sxs-lookup"><span data-stu-id="dfa18-118">For more information, see [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).</span></span>

 

 




