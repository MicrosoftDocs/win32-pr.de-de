---
title: Verwenden des Taskplaner
description: Dieser Abschnitt enthält Codebeispiele, die veranschaulichen, wie die Taskplaner-API verwendet wird, und XML-Beispiele, die zeigen, wie Aufgaben im Taskplaner Schema definiert werden.
ms.assetid: 6346cbd3-b584-47b4-8313-7830f7fd77b3
keywords:
- Trigger Taskplaner, Beispiele
- Starten einer Aufgabe Taskplaner
- Erstellen von Aufgaben Taskplaner
- Taskplaner Taskplaner mit
- Taskplaner Beispiele Taskplaner
- Taskplaner Taskplaner finden Sie in den Beispielen Taskplaner Beispiele Taskplaner
- Beispiele Taskplaner finden Sie Taskplaner Beispiele Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81dda9551917b8f6345248a316bd5941de53f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342026"
---
# <a name="using-the-task-scheduler"></a><span data-ttu-id="11683-110">Verwenden des Taskplaner</span><span class="sxs-lookup"><span data-stu-id="11683-110">Using the Task Scheduler</span></span>

<span data-ttu-id="11683-111">Dieser Abschnitt enthält Codebeispiele, die veranschaulichen, wie die Taskplaner-API verwendet wird, und XML-Beispiele, die zeigen, wie Aufgaben im Taskplaner Schema definiert werden.</span><span class="sxs-lookup"><span data-stu-id="11683-111">This section contains code examples that illustrate how the Task Scheduler API is used and XML examples that show how tasks are defined in the Task Scheduler schema.</span></span> <span data-ttu-id="11683-112">Die meisten dieser Beispiele sind eigenständige Codes, die unabhängig ausgeführt werden können oder in eine größere Anwendung eingefügt und an die Anforderungen der Anwendung angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="11683-112">Most of these examples are stand-alone code that can be run independently, or pasted into a larger application and modified to the requirements of the application.</span></span>

<span data-ttu-id="11683-113">In der folgenden Tabelle sind die Taskplaner 2,0-Beispiele in diesem Abschnitt aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="11683-113">The following table lists Task Scheduler 2.0 examples included in this section.</span></span>



| <span data-ttu-id="11683-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="11683-114">Example</span></span>                                                                                                    | <span data-ttu-id="11683-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11683-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="11683-116">Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="11683-116">Starting an Executable at a Specific Time</span></span>](starting-an-executable-at-a-spcific-time.md)                  | <span data-ttu-id="11683-117">Definiert einen Task, der den Editor zu einem angegebenen Zeitpunkt startet.</span><span class="sxs-lookup"><span data-stu-id="11683-117">Defines a task that starts Notepad at a specified time.</span></span>                                |
| [<span data-ttu-id="11683-118">Täglich eine ausführbare Datei starten</span><span class="sxs-lookup"><span data-stu-id="11683-118">Starting an Executable Daily</span></span>](starting-an-executable-daily.md)                                           | <span data-ttu-id="11683-119">Definiert eine Aufgabe, die täglich mit Notepad startet.</span><span class="sxs-lookup"><span data-stu-id="11683-119">Defines a task that starts Notepad daily.</span></span>                                              |
| [<span data-ttu-id="11683-120">Starten einer ausführbaren Datei beim System Start</span><span class="sxs-lookup"><span data-stu-id="11683-120">Starting an Executable on System Boot</span></span>](starting-an-executable-on-system-boot.md)                         | <span data-ttu-id="11683-121">Definiert einen Task, der den Editor startet, wenn das System gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="11683-121">Defines a task that starts Notepad when the system is booted.</span></span>                          |
| [<span data-ttu-id="11683-122">Wöchentliches Starten einer ausführbaren Datei</span><span class="sxs-lookup"><span data-stu-id="11683-122">Starting an Executable Weekly</span></span>](starting-an-executable-weekly.md)                                         | <span data-ttu-id="11683-123">Definiert einen Task, der den Notepad wöchentlich startet.</span><span class="sxs-lookup"><span data-stu-id="11683-123">Defines a task that starts Notepad on a weekly basis.</span></span>                                  |
| [<span data-ttu-id="11683-124">Starten einer ausführbaren Datei, wenn eine Aufgabe registriert ist</span><span class="sxs-lookup"><span data-stu-id="11683-124">Starting an Executable When a Task is Registered</span></span>](starting-an-executable-when-a-task-is-registered.md)   | <span data-ttu-id="11683-125">Definiert einen Task, der den Editor startet, wenn der Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="11683-125">Defines a task that starts Notepad when the task is registered.</span></span>                        |
| [<span data-ttu-id="11683-126">Starten einer ausführbaren Datei, wenn sich ein Benutzer anmeldet</span><span class="sxs-lookup"><span data-stu-id="11683-126">Starting an Executable When a User Logs On</span></span>](starting-an-executable-when-a-user-logs-on.md)               | <span data-ttu-id="11683-127">Definiert einen Task, der den Editor startet, wenn sich ein Benutzer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="11683-127">Defines a task that starts Notepad when a user logs on.</span></span>                                |
| [<span data-ttu-id="11683-128">Auflisten von Aufgaben und Anzeigen von Aufgabeninformationen</span><span class="sxs-lookup"><span data-stu-id="11683-128">Enumerating Tasks and Displaying Task Information</span></span>](enumerating-tasks-and-displaying-task-information.md) | <span data-ttu-id="11683-129">Listet alle Tasks auf dem lokalen Computer auf und zeigt den Zustand jeder Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="11683-129">Enumerates through all the tasks on the local computer and displays each task's state.</span></span> |



 

<span data-ttu-id="11683-130">In der folgenden Tabelle sind die Taskplaner 1,0-Beispiele in diesem Abschnitt aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="11683-130">The following table lists Task Scheduler 1.0 examples included in this section.</span></span> 

| <span data-ttu-id="11683-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="11683-131">Example</span></span>                                                                                    | <span data-ttu-id="11683-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11683-132">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11683-133">Erstellen einer Aufgabe mit NewWorkItem-Beispiel</span><span class="sxs-lookup"><span data-stu-id="11683-133">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) | <span data-ttu-id="11683-134">Erstellt eine neue Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="11683-134">Creates a new task.</span></span>                                                                           |
| [<span data-ttu-id="11683-135">Beispiel für Aufzählung von Aufgaben</span><span class="sxs-lookup"><span data-stu-id="11683-135">Enumerating Tasks Example</span></span>](enumerating-tasks-example.md)                                 | <span data-ttu-id="11683-136">Listet alle Tasks auf dem lokalen Computer auf.</span><span class="sxs-lookup"><span data-stu-id="11683-136">Enumerates all the tasks on the local computer.</span></span>                                               |
| [<span data-ttu-id="11683-137">Beispiel für das Starten einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="11683-137">Starting a Task Example</span></span>](starting-a-task-example.md)                                     | <span data-ttu-id="11683-138">Startet eine bekannte Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="11683-138">Starts a known task.</span></span>                                                                          |
| [<span data-ttu-id="11683-139">Bearbeiten eines Arbeits Elements mithilfe von Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="11683-139">Editing a Work Item using Property Pages</span></span>](editing-a-work-item-using-property-pages.md)   | <span data-ttu-id="11683-140">Zeigt die Eigenschaften Seiten einer Aufgabe zum Bearbeiten an.</span><span class="sxs-lookup"><span data-stu-id="11683-140">Displays the property pages of a task for editing.</span></span>                                            |
| [<span data-ttu-id="11683-141">Abrufen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11683-141">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       | <span data-ttu-id="11683-142">Eine Reihe von Beispielen, die zeigen, wie Eigenschaften abgerufen werden, die für alle Typen von Arbeitsaufgaben gelten.</span><span class="sxs-lookup"><span data-stu-id="11683-142">A set of examples that show how to retrieve properties that apply to all types of work items.</span></span> |
| [<span data-ttu-id="11683-143">Festlegen von Beispielen für Arbeits Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11683-143">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             | <span data-ttu-id="11683-144">Eine Reihe von Beispielen, die zeigen, wie Eigenschaften festgelegt werden, die für alle Typen von Arbeitsaufgaben gelten.</span><span class="sxs-lookup"><span data-stu-id="11683-144">A set of examples that show how to set properties that apply to all types of work items.</span></span>      |
| [<span data-ttu-id="11683-145">Abrufen von Aufgaben Eigenschafts Beispielen</span><span class="sxs-lookup"><span data-stu-id="11683-145">Retrieving Task Property Examples</span></span>](retrieving-task-property-examples.md)                 | <span data-ttu-id="11683-146">Eine Reihe von Beispielen, die zeigen, wie Eigenschaften abgerufen werden, die für Aufgaben eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="11683-146">A set of examples that show how to retrieve properties unique to tasks.</span></span>                       |
| [<span data-ttu-id="11683-147">Festlegen von Aufgaben Eigenschafts Beispielen</span><span class="sxs-lookup"><span data-stu-id="11683-147">Setting Task Property Examples</span></span>](setting-task-property-examples.md)                       | <span data-ttu-id="11683-148">Eine Reihe von Beispielen, die zeigen, wie Eigenschaften festgelegt werden, die für Aufgaben eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="11683-148">A set of examples that show how to set properties unique to tasks.</span></span>                            |
| [<span data-ttu-id="11683-149">Abrufen einer Aufgabenseite (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="11683-149">Retrieving a Task Page Example</span></span>](retrieving-a-task-page-example.md)                       | <span data-ttu-id="11683-150">Ruft die Seite "allgemeine Aufgabe" einer bekannten Aufgabe ab und zeigt diese an.</span><span class="sxs-lookup"><span data-stu-id="11683-150">Retrieves and displays the general task page of a known task.</span></span>                                 |
| [<span data-ttu-id="11683-151">Erstellen eines neuen-Auslösers</span><span class="sxs-lookup"><span data-stu-id="11683-151">Creating a New Trigger</span></span>](creating-a-new-trigger.md)                                       | <span data-ttu-id="11683-152">Erstellt einen neuen-Auslösers für eine bekannte Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="11683-152">Creates a new trigger for a known task.</span></span>                                                       |
| [<span data-ttu-id="11683-153">Erstellen eines Beispiels für einen Leerlauf-Timeout</span><span class="sxs-lookup"><span data-stu-id="11683-153">Creating an Idle Trigger Example</span></span>](creating-an-idle-trigger-example.md)                   | <span data-ttu-id="11683-154">Erstellt einen ereignisbasierten Leerlauf--Auslösers für eine bekannte Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="11683-154">Creates an event-based idle trigger for a known task.</span></span>                                         |
| [<span data-ttu-id="11683-155">Beispiel für das Beenden einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="11683-155">Terminating a Task Example</span></span>](terminating-a-task-example.md)                               | <span data-ttu-id="11683-156">Beendet eine Aufgabe, während Sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11683-156">Terminates a task while it is running.</span></span>                                                        |
| [<span data-ttu-id="11683-157">Beispiel für das Abrufen von Beispiel Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="11683-157">Retrieving Trigger Strings Example</span></span>](retrieving-trigger-strings-example.md)               | <span data-ttu-id="11683-158">Ruft die triggerzeichenfolge aller mit einer bekannten Aufgabe verknüpften Trigger ab.</span><span class="sxs-lookup"><span data-stu-id="11683-158">Retrieves the trigger string of all triggers associated with a known task.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="11683-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11683-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11683-160">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="11683-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="11683-161">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="11683-161">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




