---
title: TriggerCollection-Objekt (Windows. UI. XAML. h)
description: Skript Objekt, das zum Hinzufügen, entfernen und Abrufen der Trigger einer Aufgabe verwendet wird.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- Trigger Taskplaner, triggerauflistungs Objekt
- TriggerCollection-Objekt Taskplaner
- TriggerCollection-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103274"
---
# <a name="triggercollection-object"></a><span data-ttu-id="1f8d3-106">TriggerCollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="1f8d3-106">TriggerCollection object</span></span>

<span data-ttu-id="1f8d3-107">Skript Objekt, das zum Hinzufügen, entfernen und Abrufen der Trigger einer Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-107">Scripting object that is used to add to, remove from, and retrieve the triggers of a task.</span></span>

## <a name="members"></a><span data-ttu-id="1f8d3-108">Member</span><span class="sxs-lookup"><span data-stu-id="1f8d3-108">Members</span></span>

<span data-ttu-id="1f8d3-109">Das **TriggerCollection** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1f8d3-109">The **TriggerCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="1f8d3-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="1f8d3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f8d3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f8d3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f8d3-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1f8d3-112">Methods</span></span>

<span data-ttu-id="1f8d3-113">Das **TriggerCollection** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-113">The **TriggerCollection** object has these methods.</span></span>



| <span data-ttu-id="1f8d3-114">Methode</span><span class="sxs-lookup"><span data-stu-id="1f8d3-114">Method</span></span>                                     | <span data-ttu-id="1f8d3-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f8d3-115">Description</span></span>                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f8d3-116">**Klartext**</span><span class="sxs-lookup"><span data-stu-id="1f8d3-116">**Clear**</span></span>](triggercollection-clear.md)   | <span data-ttu-id="1f8d3-117">Löscht alle Trigger aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-117">Clears all triggers from the collection.</span></span><br/>                                        |
| [<span data-ttu-id="1f8d3-118">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="1f8d3-118">**Create**</span></span>](triggercollection-create.md) | <span data-ttu-id="1f8d3-119">Erstellt einen neuen-Auslösers für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-119">Creates a new trigger for the task.</span></span><br/>                                             |
| [<span data-ttu-id="1f8d3-120">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="1f8d3-120">**Remove**</span></span>](triggercollection-remove.md) | <span data-ttu-id="1f8d3-121">Entfernt den angegebenen Trigger aus der Auflistung von Triggern, die vom Task verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-121">Removes the specified trigger from the collection of triggers used by the task.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1f8d3-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f8d3-122">Properties</span></span>

<span data-ttu-id="1f8d3-123">Das **TriggerCollection** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-123">The **TriggerCollection** object has these properties.</span></span>



| <span data-ttu-id="1f8d3-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f8d3-124">Property</span></span>                                            | <span data-ttu-id="1f8d3-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1f8d3-125">Access type</span></span>          | <span data-ttu-id="1f8d3-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f8d3-126">Description</span></span>                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="1f8d3-127">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="1f8d3-127">**Count**</span></span>](triggercollection-count.md)<br/> | <span data-ttu-id="1f8d3-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f8d3-128">Read-only</span></span><br/> | <span data-ttu-id="1f8d3-129">Ruft die Anzahl der Trigger in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-129">Gets the number of triggers in the collection.</span></span><br/>  |
| [<span data-ttu-id="1f8d3-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f8d3-130">**Item**</span></span>](triggercollection-item.md)<br/>   | <span data-ttu-id="1f8d3-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f8d3-131">Read-only</span></span><br/> | <span data-ttu-id="1f8d3-132">Ruft den angegebenen-Auslösers aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-132">Gets the specified trigger from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f8d3-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f8d3-133">Remarks</span></span>

<span data-ttu-id="1f8d3-134">Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Trigger für die Aufgabe im [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f8d3-134">When reading or writing XML for a task, the triggers for the task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="1f8d3-135">Informationen zu den einzelnen Auslösertypen finden Sie unter [Auslösertypen](trigger-types.md)</span><span class="sxs-lookup"><span data-stu-id="1f8d3-135">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1f8d3-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f8d3-136">Examples</span></span>

<span data-ttu-id="1f8d3-137">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="1f8d3-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f8d3-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f8d3-138">Requirements</span></span>



| <span data-ttu-id="1f8d3-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f8d3-139">Requirement</span></span> | <span data-ttu-id="1f8d3-140">Wert</span><span class="sxs-lookup"><span data-stu-id="1f8d3-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8d3-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f8d3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1f8d3-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f8d3-142">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1f8d3-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f8d3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1f8d3-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f8d3-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1f8d3-145">Header</span><span class="sxs-lookup"><span data-stu-id="1f8d3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f8d3-146"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f8d3-146"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="1f8d3-147">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1f8d3-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f8d3-148"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1f8d3-148"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="1f8d3-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1f8d3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f8d3-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f8d3-150"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="1f8d3-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f8d3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f8d3-152">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="1f8d3-152">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





