---
title: Task Service-Objekt
description: Bietet für die Skripterstellung Zugriff auf den Taskplaner-Dienst zum Verwalten registrierter Tasks.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Task Service-Objekt Taskplaner
- Task Service-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478372"
---
# <a name="taskservice-object"></a><span data-ttu-id="0bf62-105">Task Service-Objekt</span><span class="sxs-lookup"><span data-stu-id="0bf62-105">TaskService object</span></span>

<span data-ttu-id="0bf62-106">Bietet für die Skripterstellung Zugriff auf den Taskplaner-Dienst zum Verwalten registrierter Tasks.</span><span class="sxs-lookup"><span data-stu-id="0bf62-106">For scripting, provides access to the Task Scheduler service for managing registered tasks.</span></span>

<span data-ttu-id="0bf62-107">Die [**TaskService. Connect**](taskservice-connect.md) -Methode sollte aufgerufen werden, bevor eine der anderen **Task Service** -Methoden aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0bf62-107">The [**TaskService.Connect**](taskservice-connect.md) method should be called before calling any of the other **TaskService** methods.</span></span>

## <a name="members"></a><span data-ttu-id="0bf62-108">Member</span><span class="sxs-lookup"><span data-stu-id="0bf62-108">Members</span></span>

<span data-ttu-id="0bf62-109">Das **TaskService** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0bf62-109">The **TaskService** object has these types of members:</span></span>

-   [<span data-ttu-id="0bf62-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0bf62-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0bf62-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bf62-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0bf62-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0bf62-112">Methods</span></span>

<span data-ttu-id="0bf62-113">Das **Task Service** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0bf62-113">The **TaskService** object has these methods.</span></span>



| <span data-ttu-id="0bf62-114">Methode</span><span class="sxs-lookup"><span data-stu-id="0bf62-114">Method</span></span>                                                 | <span data-ttu-id="0bf62-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bf62-115">Description</span></span>                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bf62-116">**Verbinden**</span><span class="sxs-lookup"><span data-stu-id="0bf62-116">**Connect**</span></span>](taskservice-connect.md)                 | <span data-ttu-id="0bf62-117">Stellt eine Verbindung mit einem Remote Computer her und ordnet alle nachfolgenden Aufrufe für diese Schnittstelle einer Remote Sitzung zu.</span><span class="sxs-lookup"><span data-stu-id="0bf62-117">Connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="0bf62-118">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="0bf62-118">**GetFolder**</span></span>](taskservice-getfolder.md)             | <span data-ttu-id="0bf62-119">Ruft den Pfad zu einem Ordner registrierter Tasks ab.</span><span class="sxs-lookup"><span data-stu-id="0bf62-119">Gets the path to a folder of registered tasks.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="0bf62-120">**Getrunningtasks**</span><span class="sxs-lookup"><span data-stu-id="0bf62-120">**GetRunningTasks**</span></span>](taskservice-getrunningtasks.md) | <span data-ttu-id="0bf62-121">Ruft eine Auflistung von Tasks ab, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0bf62-121">Gets a collection of running tasks.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="0bf62-122">**NewTask**</span><span class="sxs-lookup"><span data-stu-id="0bf62-122">**NewTask**</span></span>](taskservice-newtask.md)                 | <span data-ttu-id="0bf62-123">Gibt ein leeres Aufgaben Definitions Objekt zurück, das mit Einstellungen und Eigenschaften ausgefüllt und dann mithilfe der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bf62-123">Returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0bf62-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0bf62-124">Properties</span></span>

<span data-ttu-id="0bf62-125">Das **Task Service** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0bf62-125">The **TaskService** object has these properties.</span></span>



| <span data-ttu-id="0bf62-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0bf62-126">Property</span></span>                                                          | <span data-ttu-id="0bf62-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bf62-127">Description</span></span>                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bf62-128">**Verbunden**</span><span class="sxs-lookup"><span data-stu-id="0bf62-128">**Connected**</span></span>](taskservice-connected.md)<br/>             | <span data-ttu-id="0bf62-129">Ruft einen booleschen Wert ab, der angibt, ob eine Verbindung mit dem Taskplaner-Dienst besteht.</span><span class="sxs-lookup"><span data-stu-id="0bf62-129">Gets a Boolean value that indicates if you are connected to the Task Scheduler service.</span></span><br/>                          |
| [<span data-ttu-id="0bf62-130">**Connecteddomain**</span><span class="sxs-lookup"><span data-stu-id="0bf62-130">**ConnectedDomain**</span></span>](taskservice-connecteddomain.md)<br/> | <span data-ttu-id="0bf62-131">Ruft den Namen der Domäne ab, mit der der [**TargetServer**](taskservice-targetserver.md) -Computer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0bf62-131">Gets the name of the domain to which the [**TargetServer**](taskservice-targetserver.md) computer is connected.</span></span><br/> |
| [<span data-ttu-id="0bf62-132">**ConnectedUser**</span><span class="sxs-lookup"><span data-stu-id="0bf62-132">**ConnectedUser**</span></span>](taskservice-connecteduser.md)<br/>     | <span data-ttu-id="0bf62-133">Ruft den Namen des Benutzers ab, der mit dem Taskplaner-Dienst verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0bf62-133">Gets the name of the user that is connected to the Task Scheduler service.</span></span><br/>                                       |
| <span data-ttu-id="0bf62-134">Highestversion</span><span class="sxs-lookup"><span data-stu-id="0bf62-134">HighestVersion</span></span><br/>                                         | <span data-ttu-id="0bf62-135">Ruft die höchste Version von Taskplaner ab, die von einem Computer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0bf62-135">Gets the highest version of Task Scheduler that a computer supports.</span></span><br/>                                             |
| [<span data-ttu-id="0bf62-136">**TargetServer**</span><span class="sxs-lookup"><span data-stu-id="0bf62-136">**TargetServer**</span></span>](taskservice-targetserver.md)<br/>       | <span data-ttu-id="0bf62-137">Ruft den Namen des Computers ab, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0bf62-137">Gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span><br/>          |



 

## <a name="examples"></a><span data-ttu-id="0bf62-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0bf62-138">Examples</span></span>

<span data-ttu-id="0bf62-139">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md), [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den [täglichen Aufruf (Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen [wöchentlichen](weekly-trigger-example--scripting-.md)Vorgang (Skripterstellung), Beispiel für den Logon-Vorgang [(Skripterstellung)](logon-trigger-example--scripting-.md), Beispiel für den [Start](boot-trigger-example--scripting-.md) [-](displaying-task-names-and-state--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="0bf62-139">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf62-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bf62-140">Requirements</span></span>



| <span data-ttu-id="0bf62-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bf62-141">Requirement</span></span> | <span data-ttu-id="0bf62-142">Wert</span><span class="sxs-lookup"><span data-stu-id="0bf62-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf62-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bf62-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf62-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bf62-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0bf62-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bf62-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf62-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bf62-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0bf62-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0bf62-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="0bf62-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0bf62-148"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0bf62-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0bf62-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bf62-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bf62-150"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf62-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bf62-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf62-152">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="0bf62-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





