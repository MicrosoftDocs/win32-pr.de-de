---
title: Taskfolder-Objekt
description: Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um Aufgaben im Ordner zu registrieren (zu erstellen), Tasks aus dem Ordner zu entfernen und Unterordner aus dem Ordner zu erstellen oder zu entfernen.
ms.assetid: f6fd09ec-2777-4903-83b5-e3ac1aa472a0
keywords:
- Task Folder-Objekt Taskplaner
- Task Folder-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ccad9331cf3df12ea5752fdd7e5ac94bfbeba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518599"
---
# <a name="taskfolder-object"></a><span data-ttu-id="206f6-105">Taskfolder-Objekt</span><span class="sxs-lookup"><span data-stu-id="206f6-105">TaskFolder object</span></span>

<span data-ttu-id="206f6-106">Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um Aufgaben im Ordner zu registrieren (zu erstellen), Tasks aus dem Ordner zu entfernen und Unterordner aus dem Ordner zu erstellen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="206f6-106">Scripting object that provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.</span></span>

## <a name="members"></a><span data-ttu-id="206f6-107">Member</span><span class="sxs-lookup"><span data-stu-id="206f6-107">Members</span></span>

<span data-ttu-id="206f6-108">Das **taskfolder** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="206f6-108">The **TaskFolder** object has these types of members:</span></span>

-   [<span data-ttu-id="206f6-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="206f6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="206f6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="206f6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="206f6-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="206f6-111">Methods</span></span>

<span data-ttu-id="206f6-112">Das **taskfolder** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="206f6-112">The **TaskFolder** object has these methods.</span></span>



| <span data-ttu-id="206f6-113">Methode</span><span class="sxs-lookup"><span data-stu-id="206f6-113">Method</span></span>                                                              | <span data-ttu-id="206f6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="206f6-114">Description</span></span>                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="206f6-115">**CreateFolder**</span><span class="sxs-lookup"><span data-stu-id="206f6-115">**CreateFolder**</span></span>](taskfolder-createfolder.md)                     | <span data-ttu-id="206f6-116">Erstellt einen Ordner für Verwandte Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="206f6-116">Creates a folder for related tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="206f6-117">**DeleteFolder**</span><span class="sxs-lookup"><span data-stu-id="206f6-117">**DeleteFolder**</span></span>](taskfolder-deletefolder.md)                     | <span data-ttu-id="206f6-118">Löscht einen Unterordner aus dem übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="206f6-118">Deletes a subfolder from the parent folder.</span></span><br/>                                                                                         |
| [<span data-ttu-id="206f6-119">**DeleteTask**</span><span class="sxs-lookup"><span data-stu-id="206f6-119">**DeleteTask**</span></span>](taskfolder-deletetask.md)                         | <span data-ttu-id="206f6-120">Löscht eine Aufgabe aus dem Ordner.</span><span class="sxs-lookup"><span data-stu-id="206f6-120">Deletes a task from the folder.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="206f6-121">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="206f6-121">**GetFolder**</span></span>](taskfolder-getfolder.md)                           | <span data-ttu-id="206f6-122">Ruft einen Ordner ab, der Tasks an einem angegebenen Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="206f6-122">Gets a folder that contains tasks at a specified location.</span></span><br/>                                                                          |
| [<span data-ttu-id="206f6-123">**GetFolders**</span><span class="sxs-lookup"><span data-stu-id="206f6-123">**GetFolders**</span></span>](taskfolder-getfolders.md)                         | <span data-ttu-id="206f6-124">Ruft alle Unterordner im Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="206f6-124">Gets all the subfolders in the folder.</span></span><br/>                                                                                              |
| [<span data-ttu-id="206f6-125">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="206f6-125">**GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)   | <span data-ttu-id="206f6-126">Ruft die Sicherheits Beschreibung für den Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="206f6-126">Gets the security descriptor for the folder.</span></span><br/>                                                                                        |
| [<span data-ttu-id="206f6-127">**GetTask**</span><span class="sxs-lookup"><span data-stu-id="206f6-127">**GetTask**</span></span>](taskfolder-gettask.md)                               | <span data-ttu-id="206f6-128">Ruft eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="206f6-128">Gets a task at a specified location in a folder.</span></span><br/>                                                                                    |
| [<span data-ttu-id="206f6-129">**GetTasks**</span><span class="sxs-lookup"><span data-stu-id="206f6-129">**GetTasks**</span></span>](taskfolder-gettasks.md)                             | <span data-ttu-id="206f6-130">Ruft alle Tasks im Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="206f6-130">Gets all the tasks in the folder.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="206f6-131">**Register Task**</span><span class="sxs-lookup"><span data-stu-id="206f6-131">**RegisterTask**</span></span>](taskfolder-registertask.md)                     | <span data-ttu-id="206f6-132">Registriert (erstellt) eine neue Aufgabe im Ordner mithilfe von XML, um den Task zu definieren.</span><span class="sxs-lookup"><span data-stu-id="206f6-132">Registers (creates) a new task in the folder using XML to define the task.</span></span><br/>                                                          |
| [<span data-ttu-id="206f6-133">**Methode**</span><span class="sxs-lookup"><span data-stu-id="206f6-133">**RegisterTaskDefinition**</span></span>](taskfolder-registertaskdefinition.md) | <span data-ttu-id="206f6-134">Registriert (erstellt) einen Task an einem angegebenen Speicherort mithilfe der [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle zum Definieren einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="206f6-134">Registers (creates) a task in a specified location using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define a task.</span></span><br/> |
| [<span data-ttu-id="206f6-135">**SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="206f6-135">**SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)   | <span data-ttu-id="206f6-136">Legt die Sicherheits Beschreibung für den Ordner fest.</span><span class="sxs-lookup"><span data-stu-id="206f6-136">Sets the security descriptor for the folder.</span></span><br/>                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="206f6-137">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="206f6-137">Properties</span></span>

<span data-ttu-id="206f6-138">Das **taskfolder** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="206f6-138">The **TaskFolder** object has these properties.</span></span>



| <span data-ttu-id="206f6-139">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="206f6-139">Property</span></span>                                   | <span data-ttu-id="206f6-140">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="206f6-140">Access type</span></span>          | <span data-ttu-id="206f6-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="206f6-141">Description</span></span>                                                                        |
|:-------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="206f6-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="206f6-142">**Name**</span></span>](taskfolder-name.md)<br/> | <span data-ttu-id="206f6-143">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="206f6-143">Read-only</span></span><br/> | <span data-ttu-id="206f6-144">Ruft den Namen ab, der verwendet wird, um den Ordner zu identifizieren, der einen Task enthält.</span><span class="sxs-lookup"><span data-stu-id="206f6-144">Gets the name that is used to identify the folder that contains a task.</span></span><br/> |
| [<span data-ttu-id="206f6-145">**ADS**</span><span class="sxs-lookup"><span data-stu-id="206f6-145">**Path**</span></span>](taskfolder-path.md)<br/> | <span data-ttu-id="206f6-146">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="206f6-146">Read-only</span></span><br/> | <span data-ttu-id="206f6-147">Ruft den Pfad zum Speicherort des Ordners ab.</span><span class="sxs-lookup"><span data-stu-id="206f6-147">Gets the path to where the folder is stored.</span></span><br/>                            |



 

## <a name="examples"></a><span data-ttu-id="206f6-148">Beispiele</span><span class="sxs-lookup"><span data-stu-id="206f6-148">Examples</span></span>

<span data-ttu-id="206f6-149">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md), [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den [täglichen Aufruf (Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen [wöchentlichen](weekly-trigger-example--scripting-.md)Vorgang (Skripterstellung), Beispiel für den Logon-Vorgang [(Skripterstellung)](logon-trigger-example--scripting-.md), Beispiel für den [Start](boot-trigger-example--scripting-.md) [-](displaying-task-names-and-state--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="206f6-149">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md), or [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="206f6-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="206f6-150">Requirements</span></span>



| <span data-ttu-id="206f6-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="206f6-151">Requirement</span></span> | <span data-ttu-id="206f6-152">Wert</span><span class="sxs-lookup"><span data-stu-id="206f6-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="206f6-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="206f6-153">Minimum supported client</span></span><br/> | <span data-ttu-id="206f6-154">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="206f6-154">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="206f6-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="206f6-155">Minimum supported server</span></span><br/> | <span data-ttu-id="206f6-156">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="206f6-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="206f6-157">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="206f6-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="206f6-158"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="206f6-158"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="206f6-159">DLL</span><span class="sxs-lookup"><span data-stu-id="206f6-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="206f6-160"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="206f6-160"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206f6-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="206f6-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206f6-162">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="206f6-162">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="206f6-163">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="206f6-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





