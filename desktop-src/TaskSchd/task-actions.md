---
title: Task Aktionen
description: Die Arbeitselemente, die von einer Aufgabe ausgeführt werden, werden als Aktionen bezeichnet. Eine Aufgabe kann eine einzelne Aktion oder maximal 32 Aktionen aufweisen. Beachten Sie, dass beim Angeben mehrerer Aktionen sequenziell ausgeführt wird.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- Aktionen Taskplaner
- Aktionen Taskplaner, beschrieben
- Aktionen Taskplaner, Aktion ausführen
- Aktionen Taskplaner, com-handleraktion
- Aktion Taskplaner ausführen
- Aktionen des com-Handlers Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "103722058"
---
# <a name="task-actions"></a><span data-ttu-id="fff6d-111">Task Aktionen</span><span class="sxs-lookup"><span data-stu-id="fff6d-111">Task Actions</span></span>

<span data-ttu-id="fff6d-112">Die Arbeitselemente, die von einer Aufgabe ausgeführt werden, werden als Aktionen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fff6d-112">The work items performed by a task are called actions.</span></span> <span data-ttu-id="fff6d-113">Eine Aufgabe kann eine einzelne Aktion oder maximal 32 Aktionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fff6d-113">A task can have a single action or a maximum of 32 actions.</span></span> <span data-ttu-id="fff6d-114">Beachten Sie, dass beim Angeben mehrerer Aktionen sequenziell ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fff6d-114">Be aware that when multiple actions are specified, they are executed sequentially.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="fff6d-115">Aktionstypen</span><span class="sxs-lookup"><span data-stu-id="fff6d-115">Types of Actions</span></span>

<span data-ttu-id="fff6d-116">In der folgenden Tabelle von Aktionen werden der Typ der Arbeit oder Aktionen beschrieben, die von einer Aufgabe ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="fff6d-116">The following table of actions describes the type of work or actions that can be accomplished by a task.</span></span>

| <span data-ttu-id="fff6d-117">Aktionstyp</span><span class="sxs-lookup"><span data-stu-id="fff6d-117">Type of Action</span></span>      | <span data-ttu-id="fff6d-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fff6d-118">Description</span></span>                                                             |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fff6d-119">Comhandleraktion</span><span class="sxs-lookup"><span data-stu-id="fff6d-119">ComHandler Action</span></span>   | <span data-ttu-id="fff6d-120">Diese Aktion löst einen com-Handler aus.</span><span class="sxs-lookup"><span data-stu-id="fff6d-120">This action fires a COM handler.</span></span>                                        |
| <span data-ttu-id="fff6d-121">Exec-Aktion</span><span class="sxs-lookup"><span data-stu-id="fff6d-121">Exec Action</span></span>         | <span data-ttu-id="fff6d-122">Diese Aktion führt einen Befehlszeilen Vorgang aus, z. b. das Starten von Notepad.</span><span class="sxs-lookup"><span data-stu-id="fff6d-122">This action executes a command-line operation such as starting Notepad.</span></span> |
| <span data-ttu-id="fff6d-123">E-Mail-Aktion</span><span class="sxs-lookup"><span data-stu-id="fff6d-123">E-mail Action</span></span>       | <span data-ttu-id="fff6d-124">Diese Aktion sendet eine e-Mail, wenn ein Task ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="fff6d-124">This action sends an email when a task is triggered.</span></span>                    |
| <span data-ttu-id="fff6d-125">Nachricht anzeigen (Aktion)</span><span class="sxs-lookup"><span data-stu-id="fff6d-125">Show Message Action</span></span> | <span data-ttu-id="fff6d-126">Diese Aktion zeigt ein Meldungs Feld mit einer angegebenen Meldung und einem angegebenen Titel an.</span><span class="sxs-lookup"><span data-stu-id="fff6d-126">This action shows a message box with a specified message and title.</span></span>     |



 

## <a name="specifying-actions"></a><span data-ttu-id="fff6d-127">Festlegen von Aktionen</span><span class="sxs-lookup"><span data-stu-id="fff6d-127">Specifying Actions</span></span>

<span data-ttu-id="fff6d-128">Die Aktionen einer Aufgabe werden angegeben, wenn der Task definiert und in einer Auflistung von Aktionen gespeichert wird, die vom Taskplaner Dienst verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fff6d-128">The actions of a task are specified when the task is defined and stored in a collection of actions used by the Task Scheduler service.</span></span> <span data-ttu-id="fff6d-129">In der folgenden Tabelle sind Links zu Referenz Themen für die APIs und XML-Elemente aufgelistet, die Aktionen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fff6d-129">The following table lists links to reference topics for the APIs and XML elements that are associated with actions.</span></span>

<span data-ttu-id="fff6d-130">Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skript Objekte und XML finden [Sie unter Verwenden der Taskplaner](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="fff6d-130">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="interface-apis-for-c-development"></a><span data-ttu-id="fff6d-131">Interface-APIs für die C++-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="fff6d-131">Interface APIs for C++ Development</span></span>



| <span data-ttu-id="fff6d-132">API</span><span class="sxs-lookup"><span data-stu-id="fff6d-132">API</span></span>                                                                    | <span data-ttu-id="fff6d-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fff6d-133">Description</span></span>                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fff6d-134">**Actions-Eigenschaft von itaskdefinition**</span><span class="sxs-lookup"><span data-stu-id="fff6d-134">**Actions Property of ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | <span data-ttu-id="fff6d-135">Ruft die von der Aufgabe ausgeführten Aktionen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fff6d-135">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="fff6d-136">**IActionCollection**</span><span class="sxs-lookup"><span data-stu-id="fff6d-136">**IActionCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | <span data-ttu-id="fff6d-137">Enthält die Aktionen, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff6d-137">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="fff6d-138">**Icomhandleraction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-138">**IComHandlerAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | <span data-ttu-id="fff6d-139">Stellt eine Aktion dar, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="fff6d-139">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="fff6d-140">**IExecAction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-140">**IExecAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | <span data-ttu-id="fff6d-141">Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="fff6d-141">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="fff6d-142">**Iemailaction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-142">**IEmailAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | <span data-ttu-id="fff6d-143">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="fff6d-143">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="fff6d-144">**Ishowmessageaction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-144">**IShowMessageAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | <span data-ttu-id="fff6d-145">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fff6d-145">Represents an action that shows a message box.</span></span>               |



 

### <a name="scripting-object-apis-for-scripting-development"></a><span data-ttu-id="fff6d-146">Skript Objekt-APIs für die Skript Entwicklung</span><span class="sxs-lookup"><span data-stu-id="fff6d-146">Scripting Object APIs for Scripting Development</span></span>



| <span data-ttu-id="fff6d-147">API</span><span class="sxs-lookup"><span data-stu-id="fff6d-147">API</span></span>                                                      | <span data-ttu-id="fff6d-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fff6d-148">Description</span></span>                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fff6d-149">**Task Definition. Actions**</span><span class="sxs-lookup"><span data-stu-id="fff6d-149">**TaskDefinition.Actions**</span></span>](taskdefinition-actions.md) | <span data-ttu-id="fff6d-150">Ruft die von der Aufgabe ausgeführten Aktionen ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fff6d-150">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="fff6d-151">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="fff6d-151">**ActionCollection**</span></span>](actioncollection.md)             | <span data-ttu-id="fff6d-152">Enthält die Aktionen, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff6d-152">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="fff6d-153">**Comhandleraction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-153">**ComHandlerAction**</span></span>](comhandleraction.md)             | <span data-ttu-id="fff6d-154">Stellt eine Aktion dar, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="fff6d-154">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="fff6d-155">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-155">**ExecAction**</span></span>](execaction.md)                         | <span data-ttu-id="fff6d-156">Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="fff6d-156">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="fff6d-157">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-157">**EmailAction**</span></span>](emailaction.md)                       | <span data-ttu-id="fff6d-158">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="fff6d-158">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="fff6d-159">**Showmessageaction**</span><span class="sxs-lookup"><span data-stu-id="fff6d-159">**ShowMessageAction**</span></span>](showmessageaction.md)           | <span data-ttu-id="fff6d-160">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fff6d-160">Represents an action that shows a message box.</span></span>               |



 

### <a name="xml-elements"></a><span data-ttu-id="fff6d-161">XML-Elemente</span><span class="sxs-lookup"><span data-stu-id="fff6d-161">XML Elements</span></span>



| <span data-ttu-id="fff6d-162">Element</span><span class="sxs-lookup"><span data-stu-id="fff6d-162">Element</span></span>                                                                    | <span data-ttu-id="fff6d-163">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fff6d-163">Description</span></span>                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fff6d-164">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="fff6d-164">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)            | <span data-ttu-id="fff6d-165">Definiert die Aktionen, die von der Aufgabe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fff6d-165">Defines the actions performed by the task.</span></span>                   |
| [<span data-ttu-id="fff6d-166">**Comhandler**</span><span class="sxs-lookup"><span data-stu-id="fff6d-166">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | <span data-ttu-id="fff6d-167">Stellt eine Aktion dar, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="fff6d-167">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="fff6d-168">**Exec**</span><span class="sxs-lookup"><span data-stu-id="fff6d-168">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | <span data-ttu-id="fff6d-169">Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="fff6d-169">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="fff6d-170">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="fff6d-170">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | <span data-ttu-id="fff6d-171">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="fff6d-171">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="fff6d-172">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="fff6d-172">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | <span data-ttu-id="fff6d-173">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fff6d-173">Represents an action that shows a message box.</span></span>               |



 

## <a name="using-variables-in-action-properties"></a><span data-ttu-id="fff6d-174">Verwenden von Variablen in Aktions Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fff6d-174">Using Variables in Action Properties</span></span>

<span data-ttu-id="fff6d-175">Einige Aktions Eigenschaften vom Typ **BSTR** können die Variablen $ (Arg0), $ (arg1),..., $ (Arg32) in ihren Zeichen folgen Werten enthalten.</span><span class="sxs-lookup"><span data-stu-id="fff6d-175">Some action properties that are of type **BSTR** can contain $(Arg0), $(Arg1), ..., $(Arg32) variables in their string values.</span></span> <span data-ttu-id="fff6d-176">Diese Variablen werden durch die Werte ersetzt, die im Parameter *para* meters der [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) -Methode und der [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) -Methode angegeben sind oder im Ereignis--Fehler für die Aufgabe enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fff6d-176">These variables are replaced with the values that are specified in the *params* parameter of the [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) and [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) methods or are contained within the event trigger for the task.</span></span> <span data-ttu-id="fff6d-177">In der folgenden Tabelle sind die Aktions Eigenschaften aufgeführt, die Variablen in ihren Zeichen folgen Werten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="fff6d-177">The following table lists the action properties that can use variables in their string values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fff6d-178">Aktion</span><span class="sxs-lookup"><span data-stu-id="fff6d-178">Action</span></span></th>
<th><span data-ttu-id="fff6d-179">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fff6d-179">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fff6d-180">COM-handleraktion</span><span class="sxs-lookup"><span data-stu-id="fff6d-180">COM Handler Action</span></span></td>
<td><span data-ttu-id="fff6d-181">C++:</span><span class="sxs-lookup"><span data-stu-id="fff6d-181">C++:</span></span>
<ul>
<li><span data-ttu-id="fff6d-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassID-Eigenschaft von icomhandleraction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId Property of IComHandlerAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Dateneigenschaft von icomhandleraction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data Property of IComHandlerAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fff6d-184">Skripterstellung:</span><span class="sxs-lookup"><span data-stu-id="fff6d-184">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fff6d-185"><a href="comhandleraction-classid.md"><strong>Comhandleraction. ClassID</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-186"><a href="comhandleraction-data.md"><strong>Comhandleraction. Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fff6d-187">E-Mail-Aktion</span><span class="sxs-lookup"><span data-stu-id="fff6d-187">Email Action</span></span></td>
<td><span data-ttu-id="fff6d-188">C++:</span><span class="sxs-lookup"><span data-stu-id="fff6d-188">C++:</span></span>
<ul>
<li><span data-ttu-id="fff6d-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>CC-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>BCC-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From-Eigenschaft von iemailaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From Property of IEmailAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fff6d-197">Skripterstellung:</span><span class="sxs-lookup"><span data-stu-id="fff6d-197">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fff6d-198"><a href="emailaction-body.md"><strong>Emailaction. Body</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-198"><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-199"><a href="emailaction-server.md"><strong>Emailaction. Server</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-199"><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-200"><a href="emailaction-subject.md"><strong>Emailaction. Subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-200"><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-203"><a href="emailaction-bcc.md"><strong>Emailaction. BCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-203"><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-204"><a href="emailaction-replyto.md"><strong>Emailaction. ReplyTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-204"><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-205"><a href="emailaction-from.md"><strong>Emailaction. from</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-205"><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fff6d-206">Exec-Aktion</span><span class="sxs-lookup"><span data-stu-id="fff6d-206">Exec Action</span></span></td>
<td><span data-ttu-id="fff6d-207">C++:</span><span class="sxs-lookup"><span data-stu-id="fff6d-207">C++:</span></span>
<ul>
<li><span data-ttu-id="fff6d-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments-Eigenschaft von IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments Property of IExecAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory-Eigenschaft von IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory Property of IExecAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fff6d-210">Skripterstellung:</span><span class="sxs-lookup"><span data-stu-id="fff6d-210">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fff6d-211"><a href="execaction-arguments.md"><strong>Execaction. Arguments</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-211"><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-212"><a href="execaction-workingdirectory.md"><strong>Execaction. WorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-212"><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fff6d-213">Nachricht anzeigen (Aktion)</span><span class="sxs-lookup"><span data-stu-id="fff6d-213">Show Message Action</span></span></td>
<td><span data-ttu-id="fff6d-214">C++:</span><span class="sxs-lookup"><span data-stu-id="fff6d-214">C++:</span></span>
<ul>
<li><span data-ttu-id="fff6d-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title-Eigenschaft von ishowmessageaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title Property of IShowMessageAction</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody-Eigenschaft von ishowmessageaction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody Property of IShowMessageAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fff6d-217">Skripterstellung:</span><span class="sxs-lookup"><span data-stu-id="fff6d-217">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fff6d-218"><a href="showmessageaction-title.md"><strong>Showmessageaction. Title</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></span></span></li>
<li><span data-ttu-id="fff6d-219"><a href="showmessageaction-messagebody.md"><strong>Showmessageaction. MessageBody</strong></a></span><span class="sxs-lookup"><span data-stu-id="fff6d-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fff6d-220">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fff6d-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fff6d-221">Informationen zum Taskplaner</span><span class="sxs-lookup"><span data-stu-id="fff6d-221">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 





