---
title: Aktions Sammlungsobjekt
description: Skript Objekt, das die von der Aufgabe ausgeführten Aktionen enthält.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- Aktionen Taskplaner, Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner
- Taskplaner des Aktions Sammlungs Objekts, beschrieben
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519143"
---
# <a name="actioncollection-object"></a><span data-ttu-id="cc562-106">Aktions Sammlungsobjekt</span><span class="sxs-lookup"><span data-stu-id="cc562-106">ActionCollection object</span></span>

<span data-ttu-id="cc562-107">Skript Objekt, das die von der Aufgabe ausgeführten Aktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="cc562-107">Scripting object that contains the actions performed by the task.</span></span>

## <a name="members"></a><span data-ttu-id="cc562-108">Member</span><span class="sxs-lookup"><span data-stu-id="cc562-108">Members</span></span>

<span data-ttu-id="cc562-109">Das Objekt " **Aktions Sammlung** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cc562-109">The **ActionCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="cc562-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="cc562-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cc562-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc562-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cc562-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="cc562-112">Methods</span></span>

<span data-ttu-id="cc562-113">Das Objekt " **Aktions Sammlung** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cc562-113">The **ActionCollection** object has these methods.</span></span>



| <span data-ttu-id="cc562-114">Methode</span><span class="sxs-lookup"><span data-stu-id="cc562-114">Method</span></span>                                    | <span data-ttu-id="cc562-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc562-115">Description</span></span>                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="cc562-116">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="cc562-116">**Clear**</span></span>](actioncollection-clear.md)   | <span data-ttu-id="cc562-117">Löscht alle Aktionen aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="cc562-117">Clears all the actions from the collection.</span></span><br/>      |
| [<span data-ttu-id="cc562-118">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="cc562-118">**Create**</span></span>](actioncollection-create.md) | <span data-ttu-id="cc562-119">Erstellt eine neue Aktion und fügt Sie der Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc562-119">Creates and adds a new action to the collection.</span></span><br/> |
| [<span data-ttu-id="cc562-120">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="cc562-120">**Remove**</span></span>](actioncollection-remove.md) | <span data-ttu-id="cc562-121">Entfernt eine angegebene Aktion aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="cc562-121">Removes a specified action from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="cc562-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc562-122">Properties</span></span>

<span data-ttu-id="cc562-123">Das Objekt " **Aktions Sammlung** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc562-123">The **ActionCollection** object has these properties.</span></span>



| <span data-ttu-id="cc562-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc562-124">Property</span></span>                                               | <span data-ttu-id="cc562-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="cc562-125">Access type</span></span>           | <span data-ttu-id="cc562-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc562-126">Description</span></span>                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="cc562-127">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="cc562-127">**Context**</span></span>](actioncollection-context.md)<br/> | <span data-ttu-id="cc562-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cc562-128">Read/write</span></span><br/> | <span data-ttu-id="cc562-129">Ruft den Bezeichner des Prinzipals für den Task ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="cc562-129">Gets or sets the identifier of the principal for the task.</span></span><br/> |
| [<span data-ttu-id="cc562-130">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="cc562-130">**Count**</span></span>](actioncollection-count.md)<br/>     | <span data-ttu-id="cc562-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cc562-131">Read-only</span></span><br/>  | <span data-ttu-id="cc562-132">Ruft die Anzahl von Aktionen in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="cc562-132">Gets the number of actions in the collection.</span></span><br/>              |
| [<span data-ttu-id="cc562-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="cc562-133">**Item**</span></span>](actioncollection-item.md)<br/>       | <span data-ttu-id="cc562-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cc562-134">Read-only</span></span><br/>  | <span data-ttu-id="cc562-135">Ruft eine angegebene Aktion aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="cc562-135">Gets a specified action from the collection.</span></span><br/>               |
| [<span data-ttu-id="cc562-136">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="cc562-136">**XmlText**</span></span>](actioncollection-xmltext.md)<br/> | <span data-ttu-id="cc562-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cc562-137">Read/write</span></span><br/> | <span data-ttu-id="cc562-138">Ruft eine XML-formatierte Version der Auflistung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="cc562-138">Gets or sets an XML-formatted version of the collection.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="cc562-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc562-139">Remarks</span></span>

<span data-ttu-id="cc562-140">Beim Lesen oder Schreiben von XML werden die Aktionen einer Aufgabe im [**Actions**](taskschedulerschema-actions-tasktype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="cc562-140">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="cc562-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc562-141">Examples</span></span>

<span data-ttu-id="cc562-142">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md), [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den täglichen Auslösung [(Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen wöchentlichen Aufruf [(](weekly-trigger-example--scripting-.md)Skripterstellung), Beispiel für LOGON-Beispiel [(Skript](logon-trigger-example--scripting-.md)Erstellung) oder [Beispiel](boot-trigger-example--scripting-.md)für</span><span class="sxs-lookup"><span data-stu-id="cc562-142">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc562-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc562-143">Requirements</span></span>



| <span data-ttu-id="cc562-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc562-144">Requirement</span></span> | <span data-ttu-id="cc562-145">Wert</span><span class="sxs-lookup"><span data-stu-id="cc562-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc562-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc562-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cc562-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc562-147">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cc562-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc562-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cc562-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc562-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc562-150">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cc562-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc562-151"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cc562-151"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cc562-152">DLL</span><span class="sxs-lookup"><span data-stu-id="cc562-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc562-153"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc562-153"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





