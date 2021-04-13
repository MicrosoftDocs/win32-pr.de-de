---
title: Runningtask-Objekt
description: Skript Objekt, das die Methoden bereitstellt, um Informationen aus einer laufenden Aufgabe zu erhalten und zu steuern.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Runningtask-Objekt Taskplaner
- Runningtask-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518209"
---
# <a name="runningtask-object"></a><span data-ttu-id="7cdaf-105">Runningtask-Objekt</span><span class="sxs-lookup"><span data-stu-id="7cdaf-105">RunningTask object</span></span>

<span data-ttu-id="7cdaf-106">Skript Objekt, das die Methoden bereitstellt, um Informationen aus einer laufenden Aufgabe zu erhalten und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-106">Scripting object that provides the methods to get information from and control a running task.</span></span>

## <a name="members"></a><span data-ttu-id="7cdaf-107">Member</span><span class="sxs-lookup"><span data-stu-id="7cdaf-107">Members</span></span>

<span data-ttu-id="7cdaf-108">Das **runningtask** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7cdaf-108">The **RunningTask** object has these types of members:</span></span>

-   [<span data-ttu-id="7cdaf-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="7cdaf-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7cdaf-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7cdaf-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7cdaf-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7cdaf-111">Methods</span></span>

<span data-ttu-id="7cdaf-112">Das **runningtask** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-112">The **RunningTask** object has these methods.</span></span>



| <span data-ttu-id="7cdaf-113">Methode</span><span class="sxs-lookup"><span data-stu-id="7cdaf-113">Method</span></span>                                 | <span data-ttu-id="7cdaf-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cdaf-114">Description</span></span>                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="7cdaf-115">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-115">**Refresh**</span></span>](runningtask-refresh.md) | <span data-ttu-id="7cdaf-116">Aktualisiert alle lokalen Instanzvariablen der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-116">Refreshes all of the local instance variables of the task.</span></span><br/> |
| [<span data-ttu-id="7cdaf-117">**Stop**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-117">**Stop**</span></span>](runningtask-stop.md)       | <span data-ttu-id="7cdaf-118">Beendet diese Instanz der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-118">Stops this instance of the task.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="7cdaf-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7cdaf-119">Properties</span></span>

<span data-ttu-id="7cdaf-120">Das **runningtask** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-120">The **RunningTask** object has these properties.</span></span>



| <span data-ttu-id="7cdaf-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7cdaf-121">Property</span></span>                                                      | <span data-ttu-id="7cdaf-122">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="7cdaf-122">Access type</span></span>          | <span data-ttu-id="7cdaf-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cdaf-123">Description</span></span>                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cdaf-124">**Currentaction**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-124">**CurrentAction**</span></span>](runningtask-currentaction.md)<br/> | <span data-ttu-id="7cdaf-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7cdaf-125">Read-only</span></span><br/> | <span data-ttu-id="7cdaf-126">Ruft den Namen der aktuellen Aktion ab, die der laufende Task ausführt.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-126">Gets the name of the current action that the running task is performing.</span></span><br/> |
| [<span data-ttu-id="7cdaf-127">**Enginepid**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-127">**EnginePID**</span></span>](runningtask-enginepid.md)<br/>         | <span data-ttu-id="7cdaf-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7cdaf-128">Read-only</span></span><br/> | <span data-ttu-id="7cdaf-129">Ruft die Prozess-ID für die Engine (Prozess) ab, in der die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-129">Gets the process ID for the engine (process) which is running the task.</span></span><br/>  |
| [<span data-ttu-id="7cdaf-130">**GUID**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-130">**InstanceGuid**</span></span>](runningtask-instanceguid.md)<br/>   | <span data-ttu-id="7cdaf-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7cdaf-131">Read-only</span></span><br/> | <span data-ttu-id="7cdaf-132">Ruft den GUID-Bezeichner für diese Instanz der Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-132">Gets the GUID identifier for this instance of the task.</span></span><br/>                  |
| [<span data-ttu-id="7cdaf-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-133">**Name**</span></span>](runningtask-name.md)<br/>                   | <span data-ttu-id="7cdaf-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7cdaf-134">Read-only</span></span><br/> | <span data-ttu-id="7cdaf-135">Ruft den Namen des Tasks ab.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-135">Gets the name of the task.</span></span><br/>                                               |
| [<span data-ttu-id="7cdaf-136">**ADS**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-136">**Path**</span></span>](runningtask-path.md)<br/>                   | <span data-ttu-id="7cdaf-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7cdaf-137">Read-only</span></span><br/> | <span data-ttu-id="7cdaf-138">Ruft den Pfad zum Speicherort der Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-138">Gets the path to where the task is stored.</span></span><br/>                               |
| [<span data-ttu-id="7cdaf-139">**State**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-139">**State**</span></span>](runningtask-state.md)<br/>                 | <span data-ttu-id="7cdaf-140">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7cdaf-140">Read-only</span></span><br/> | <span data-ttu-id="7cdaf-141">Ruft den Zustand der aktuell laufenden Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="7cdaf-141">Gets the state of the running task.</span></span> <br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="7cdaf-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cdaf-142">Requirements</span></span>



| <span data-ttu-id="7cdaf-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cdaf-143">Requirement</span></span> | <span data-ttu-id="7cdaf-144">Wert</span><span class="sxs-lookup"><span data-stu-id="7cdaf-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cdaf-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cdaf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7cdaf-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cdaf-146">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7cdaf-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cdaf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7cdaf-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cdaf-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cdaf-149">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7cdaf-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="7cdaf-150"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7cdaf-150"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7cdaf-151">DLL</span><span class="sxs-lookup"><span data-stu-id="7cdaf-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cdaf-152"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cdaf-152"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cdaf-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cdaf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cdaf-154">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="7cdaf-154">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="7cdaf-155">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="7cdaf-155">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="7cdaf-156">**Runningtaskcollection**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-156">**RunningTaskCollection**</span></span>](runningtaskcollection.md)
</dt> <dt>

[<span data-ttu-id="7cdaf-157">**Registeredtask. Run**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-157">**RegisteredTask.Run**</span></span>](registeredtask-run.md)
</dt> <dt>

[<span data-ttu-id="7cdaf-158">**Registeredtask. RunEx**</span><span class="sxs-lookup"><span data-stu-id="7cdaf-158">**RegisteredTask.RunEx**</span></span>](registeredtask-runex.md)
</dt> </dl>

 

 





