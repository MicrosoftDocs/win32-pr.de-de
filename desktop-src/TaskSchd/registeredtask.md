---
title: Registeredtask-Objekt
description: Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um den Task sofort auszuführen, alle laufenden Instanzen der Aufgabe zu erhalten, die zum Registrieren der Aufgabe verwendeten Anmelde Informationen zu erhalten oder festzulegen, sowie die Eigenschaften, die den Task beschreiben.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Registeredtask-Objekt Taskplaner
- Registeredtask-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740472"
---
# <a name="registeredtask-object"></a><span data-ttu-id="831e4-105">Registeredtask-Objekt</span><span class="sxs-lookup"><span data-stu-id="831e4-105">RegisteredTask object</span></span>

<span data-ttu-id="831e4-106">Skript Objekt, das die Methoden bereitstellt, die verwendet werden, um den Task sofort auszuführen, alle laufenden Instanzen der Aufgabe zu erhalten, die zum Registrieren der Aufgabe verwendeten Anmelde Informationen zu erhalten oder festzulegen, sowie die Eigenschaften, die den Task beschreiben.</span><span class="sxs-lookup"><span data-stu-id="831e4-106">Scripting object that provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.</span></span>

## <a name="members"></a><span data-ttu-id="831e4-107">Member</span><span class="sxs-lookup"><span data-stu-id="831e4-107">Members</span></span>

<span data-ttu-id="831e4-108">Das **registeredtask** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="831e4-108">The **RegisteredTask** object has these types of members:</span></span>

-   [<span data-ttu-id="831e4-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="831e4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="831e4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="831e4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="831e4-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="831e4-111">Methods</span></span>

<span data-ttu-id="831e4-112">Das **registeredtask** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="831e4-112">The **RegisteredTask** object has these methods.</span></span>



| <span data-ttu-id="831e4-113">Methode</span><span class="sxs-lookup"><span data-stu-id="831e4-113">Method</span></span>                                                                | <span data-ttu-id="831e4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="831e4-114">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="831e4-115">**Getinhaltungen**</span><span class="sxs-lookup"><span data-stu-id="831e4-115">**GetInstances**</span></span>](registeredtask-getinstances.md)                   | <span data-ttu-id="831e4-116">Gibt alle Instanzen der registrierten Aufgabe zurück, die zurzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="831e4-116">Returns all instances of the registered task that are currently running.</span></span><br/>             |
| [<span data-ttu-id="831e4-117">**Getruntimes**</span><span class="sxs-lookup"><span data-stu-id="831e4-117">**GetRunTimes**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | <span data-ttu-id="831e4-118">Ruft die Zeiten ab, zu denen die Ausführung der registrierten Aufgabe innerhalb eines angegebenen Zeitraums geplant ist.</span><span class="sxs-lookup"><span data-stu-id="831e4-118">Gets the times that the registered task is scheduled to run during a specified time.</span></span><br/> |
| [<span data-ttu-id="831e4-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="831e4-119">**GetSecurityDescriptor**</span></span>](registeredtask-getsecuritydescriptor.md) | <span data-ttu-id="831e4-120">Ruft die Sicherheits Beschreibung ab, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="831e4-120">Gets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="831e4-121">**Ausführen**</span><span class="sxs-lookup"><span data-stu-id="831e4-121">**Run**</span></span>](registeredtask-run.md)                                     | <span data-ttu-id="831e4-122">Führt die registrierte Aufgabe sofort aus.</span><span class="sxs-lookup"><span data-stu-id="831e4-122">Runs the registered task immediately.</span></span><br/>                                                |
| [<span data-ttu-id="831e4-123">**RunEx**</span><span class="sxs-lookup"><span data-stu-id="831e4-123">**RunEx**</span></span>](registeredtask-runex.md)                                 | <span data-ttu-id="831e4-124">Führt die registrierte Aufgabe sofort mit angegebenen Flags und einem Sitzungs Bezeichner aus.</span><span class="sxs-lookup"><span data-stu-id="831e4-124">Runs the registered task immediately using specified flags and a session identifier.</span></span><br/> |
| [<span data-ttu-id="831e4-125">**SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="831e4-125">**SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md) | <span data-ttu-id="831e4-126">Legt die Sicherheits Beschreibung fest, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="831e4-126">Sets the security descriptor that is used as credentials for the registered task.</span></span><br/>    |
| [<span data-ttu-id="831e4-127">**Stop**</span><span class="sxs-lookup"><span data-stu-id="831e4-127">**Stop**</span></span>](registeredtask-stop.md)                                   | <span data-ttu-id="831e4-128">Beendet die registrierte Aufgabe sofort.</span><span class="sxs-lookup"><span data-stu-id="831e4-128">Stops the registered task immediately.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="831e4-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="831e4-129">Properties</span></span>

<span data-ttu-id="831e4-130">Das **registeredtask** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="831e4-130">The **RegisteredTask** object has these properties.</span></span>



| <span data-ttu-id="831e4-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="831e4-131">Property</span></span>                                                                   | <span data-ttu-id="831e4-132">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="831e4-132">Access type</span></span>           | <span data-ttu-id="831e4-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="831e4-133">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="831e4-134">**Definition**</span><span class="sxs-lookup"><span data-stu-id="831e4-134">**Definition**</span></span>](registeredtask-definition.md)<br/>                 | <span data-ttu-id="831e4-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-135">Read-only</span></span><br/>  | <span data-ttu-id="831e4-136">Ruft die Definition der Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="831e4-136">Gets the definition of the task.</span></span><br/>                                               |
| [<span data-ttu-id="831e4-137">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="831e4-137">**Enabled**</span></span>](registeredtask-enabled.md)<br/>                       | <span data-ttu-id="831e4-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="831e4-138">Read/write</span></span><br/> | <span data-ttu-id="831e4-139">Ruft einen booleschen Wert ab, der angibt, ob die registrierte Aufgabe aktiviert ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="831e4-139">Gets or set a Boolean value that indicates if the registered task is enabled.</span></span><br/>  |
| [<span data-ttu-id="831e4-140">**Lastrauuntime**</span><span class="sxs-lookup"><span data-stu-id="831e4-140">**LastRunTime**</span></span>](registeredtask-lastruntime.md)<br/>               | <span data-ttu-id="831e4-141">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-141">Read-only</span></span><br/>  | <span data-ttu-id="831e4-142">Ruft den Zeitpunkt ab, zu dem die registrierte Aufgabe zuletzt ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="831e4-142">Gets the time the registered task was last run.</span></span><br/>                                |
| [<span data-ttu-id="831e4-143">**Lasttaskresult**</span><span class="sxs-lookup"><span data-stu-id="831e4-143">**LastTaskResult**</span></span>](registeredtask-lasttaskresult.md)<br/>         | <span data-ttu-id="831e4-144">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-144">Read-only</span></span><br/>  | <span data-ttu-id="831e4-145">Ruft die Ergebnisse ab, die bei der letzten Durchführung der registrierten Aufgabe zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="831e4-145">Gets the results that were returned the last time the registered task was run.</span></span><br/> |
| [<span data-ttu-id="831e4-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="831e4-146">**Name**</span></span>](registeredtask-name.md)<br/>                             | <span data-ttu-id="831e4-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-147">Read-only</span></span><br/>  | <span data-ttu-id="831e4-148">Ruft den Namen der registrierten Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="831e4-148">Gets the name of the registered task.</span></span><br/>                                          |
| [<span data-ttu-id="831e4-149">**NextRunTime**</span><span class="sxs-lookup"><span data-stu-id="831e4-149">**NextRunTime**</span></span>](registeredtask-nextruntime.md)<br/>               | <span data-ttu-id="831e4-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-150">Read-only</span></span><br/>  | <span data-ttu-id="831e4-151">Ruft den Zeitpunkt ab, zu dem die nächste Ausführung der registrierten Aufgabe geplant wird.</span><span class="sxs-lookup"><span data-stu-id="831e4-151">Gets the time when the registered task is next scheduled to run.</span></span><br/>               |
| [<span data-ttu-id="831e4-152">**Anzahl von Fehlern**</span><span class="sxs-lookup"><span data-stu-id="831e4-152">**NumberOfMissedRuns**</span></span>](registeredtask-numberofmissedruns.md)<br/> | <span data-ttu-id="831e4-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-153">Read-only</span></span><br/>  | <span data-ttu-id="831e4-154">Ruft ab, wie oft die registrierte Aufgabe einen geplanten Testlauf verpasst hat.</span><span class="sxs-lookup"><span data-stu-id="831e4-154">Gets the number of times the registered task has missed a scheduled run.</span></span><br/>       |
| [<span data-ttu-id="831e4-155">**ADS**</span><span class="sxs-lookup"><span data-stu-id="831e4-155">**Path**</span></span>](registeredtask-path.md)<br/>                             | <span data-ttu-id="831e4-156">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-156">Read-only</span></span><br/>  | <span data-ttu-id="831e4-157">Ruft den Pfad ab, in dem die registrierte Aufgabe gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="831e4-157">Gets the path to where the registered task is stored.</span></span><br/>                          |
| [<span data-ttu-id="831e4-158">**State**</span><span class="sxs-lookup"><span data-stu-id="831e4-158">**State**</span></span>](registeredtask-state.md)<br/>                           | <span data-ttu-id="831e4-159">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-159">Read-only</span></span><br/>  | <span data-ttu-id="831e4-160">Ruft den Betriebszustand der registrierten Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="831e4-160">Gets the operational state of the registered task.</span></span><br/>                             |
| [<span data-ttu-id="831e4-161">**Basi**</span><span class="sxs-lookup"><span data-stu-id="831e4-161">**XML**</span></span>](registeredtask-xml.md)<br/>                               | <span data-ttu-id="831e4-162">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="831e4-162">Read-only</span></span><br/>  | <span data-ttu-id="831e4-163">Ruft die XML-formatierten Registrierungsinformationen für die registrierte Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="831e4-163">Gets the XML-formatted registration information for the registered task.</span></span><br/>       |



 

## <a name="examples"></a><span data-ttu-id="831e4-164">Beispiele</span><span class="sxs-lookup"><span data-stu-id="831e4-164">Examples</span></span>

<span data-ttu-id="831e4-165">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md) und [Anzeigen von Aufgaben Namen und-Zuständen (Skripterstellung)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="831e4-165">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) and [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="831e4-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="831e4-166">Requirements</span></span>



| <span data-ttu-id="831e4-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="831e4-167">Requirement</span></span> | <span data-ttu-id="831e4-168">Wert</span><span class="sxs-lookup"><span data-stu-id="831e4-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="831e4-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="831e4-169">Minimum supported client</span></span><br/> | <span data-ttu-id="831e4-170">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="831e4-170">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="831e4-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="831e4-171">Minimum supported server</span></span><br/> | <span data-ttu-id="831e4-172">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="831e4-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="831e4-173">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="831e4-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="831e4-174"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="831e4-174"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="831e4-175">DLL</span><span class="sxs-lookup"><span data-stu-id="831e4-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="831e4-176"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="831e4-176"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





