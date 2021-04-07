---
title: Bearbeiten von Arbeits Elementen
description: Die ischeduledworkitem-Schnittstelle stellt Methoden zum Abrufen und Festlegen von Arbeits Element Eigenschaften bereit. Erstellen, abrufen und Löschen von Triggern für Arbeitselemente (das Festlegen des Triggers muss mit der itasktrigger-settrigger-Methode erfolgen); und zum Ausführen, beenden und Löschen des Arbeits Elements. Beachten Sie für die Eigenschaften eines bestimmten Arbeits Elementtyps die-Schnittstelle für diesen Objekttyp. Beispielsweise können Sie die Prioritätsstufe eines Arbeits Elements nicht festlegen. Sie können jedoch die Methoden der ITask-Schnittstelle verwenden, um die Priorität einer Aufgabe abzurufen und festzulegen.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- Arbeitselemente Taskplaner, verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728545"
---
# <a name="manipulating-work-items"></a><span data-ttu-id="a8a59-105">Bearbeiten von Arbeits Elementen</span><span class="sxs-lookup"><span data-stu-id="a8a59-105">Manipulating Work Items</span></span>

<span data-ttu-id="a8a59-106">Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle stellt Methoden zum Abrufen und Festlegen von Arbeits Element Eigenschaften bereit. Erstellen, abrufen und Löschen von Triggern für Arbeitselemente (das Festlegen des Triggers muss mit der [**itasktrigger:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) -Methode erfolgen); und zum Ausführen, beenden und Löschen des Arbeits Elements.</span><span class="sxs-lookup"><span data-stu-id="a8a59-106">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for retrieving and setting work item properties; creating, retrieving, and deleting triggers for work items (setting the trigger must be done with the [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) method); and for running, terminating, and deleting the work item.</span></span>

> [!Note]  
> <span data-ttu-id="a8a59-107">Informationen zu den Eigenschaften eines bestimmten Arbeits Elementtyps finden Sie in der-Schnittstelle für diesen Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="a8a59-107">For the properties of a specific type of work item, refer to the interface for that type of object.</span></span> <span data-ttu-id="a8a59-108">Beispielsweise können Sie die Prioritätsstufe eines Arbeits Elements nicht festlegen. Sie können jedoch die Methoden der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle verwenden, um die Priorität einer Aufgabe abzurufen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a8a59-108">For example, you cannot set the priority level of a work item; however, you can use the methods of the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface to retrieve and set the priority of a task.</span></span>

 

<span data-ttu-id="a8a59-109">Wenn Sie ein Arbeits Element ändern, müssen Sie das Objekt [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) abrufen, um das geänderte Arbeits Element auf dem Datenträger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a8a59-109">Whenever you modify a work item, you must call the [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) object to save the modified work item to disk.</span></span> <span data-ttu-id="a8a59-110">Die Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine Standard-COM-Schnittstelle, die von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a8a59-110">The [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface is a standard COM interface that is supported by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface.</span></span>

| <span data-ttu-id="a8a59-111">Beispiele für</span><span class="sxs-lookup"><span data-stu-id="a8a59-111">For examples of</span></span>                                                            | <span data-ttu-id="a8a59-112">Siehe</span><span class="sxs-lookup"><span data-stu-id="a8a59-112">See</span></span>                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a59-113">Abrufen von Eigenschaften, die für alle Typen von Arbeits Elementen gelten</span><span class="sxs-lookup"><span data-stu-id="a8a59-113">Retrieving properties that apply to all types of work items</span></span>                | [<span data-ttu-id="a8a59-114">Abrufen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8a59-114">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md) |
| <span data-ttu-id="a8a59-115">Festlegen von Eigenschaften, die für alle Typen von Arbeits Elementen gelten</span><span class="sxs-lookup"><span data-stu-id="a8a59-115">Setting properties that apply to all types of work items</span></span>                   | [<span data-ttu-id="a8a59-116">Festlegen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a8a59-116">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)       |
| <span data-ttu-id="a8a59-117">Ausführen einer bekannten Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a8a59-117">Running a known task</span></span>                                                       | [<span data-ttu-id="a8a59-118">Beispiel für das Starten einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a8a59-118">Starting a Task Example</span></span>](starting-a-task-example.md)                               |
| <span data-ttu-id="a8a59-119">Beenden einer laufenden Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a8a59-119">Terminating a running task</span></span>                                                 | [<span data-ttu-id="a8a59-120">Beispiel für das Beenden einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a8a59-120">Terminating a Task Example</span></span>](terminating-a-task-example.md)                         |
| <span data-ttu-id="a8a59-121">Erstellen eines neuen-Auslösers für eine bekannte Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a8a59-121">Creating a new trigger for a known task</span></span>                                    | [<span data-ttu-id="a8a59-122">Erstellen eines neuen-Auslösers</span><span class="sxs-lookup"><span data-stu-id="a8a59-122">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                 |
| <span data-ttu-id="a8a59-123">Erstellen eines ereignisbasierten Leerlauf-Auslösers für eine bekannte Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a8a59-123">Creating an event-based idle trigger for a known task</span></span>                      | [<span data-ttu-id="a8a59-124">Erstellen eines Beispiels für einen Leerlauf-Timeout</span><span class="sxs-lookup"><span data-stu-id="a8a59-124">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)             |
| <span data-ttu-id="a8a59-125">Abrufen der triggerzeichenfolge aller Trigger, die einer bekannten Aufgabe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="a8a59-125">Retrieving the trigger string of all triggers associated with a known task</span></span> | [<span data-ttu-id="a8a59-126">Beispiel für das Abrufen von Beispiel Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="a8a59-126">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)         |



 

 

 