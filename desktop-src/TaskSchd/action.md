---
title: Aktions Objekt
description: Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Aktions Objekten geerbt werden.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Aktions Objekt Taskplaner
- Taskplaner des Aktions Objekts, beschrieben
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518239"
---
# <a name="action-object"></a><span data-ttu-id="e0b95-105">Aktions Objekt</span><span class="sxs-lookup"><span data-stu-id="e0b95-105">Action object</span></span>

<span data-ttu-id="e0b95-106">Skript Objekt, das die allgemeinen Eigenschaften bereitstellt, die von allen Aktions Objekten geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="e0b95-106">Scripting object that provides the common properties that are inherited by all action objects.</span></span> <span data-ttu-id="e0b95-107">Ein Aktions Objekt wird von der [**Action Collection. Create**](actioncollection-create.md) -Methode erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0b95-107">An action object is created by the [**ActionCollection.Create**](actioncollection-create.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="e0b95-108">Member</span><span class="sxs-lookup"><span data-stu-id="e0b95-108">Members</span></span>

<span data-ttu-id="e0b95-109">Das **Aktions** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e0b95-109">The **Action** object has these types of members:</span></span>

-   [<span data-ttu-id="e0b95-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0b95-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0b95-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e0b95-111">Properties</span></span>

<span data-ttu-id="e0b95-112">Das **Aktions** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e0b95-112">The **Action** object has these properties.</span></span>



| <span data-ttu-id="e0b95-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e0b95-113">Property</span></span>                               | <span data-ttu-id="e0b95-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="e0b95-114">Access type</span></span>           | <span data-ttu-id="e0b95-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0b95-115">Description</span></span>                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [<span data-ttu-id="e0b95-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="e0b95-116">**Id**</span></span>](action-id.md)<br/>     | <span data-ttu-id="e0b95-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e0b95-117">Read/write</span></span><br/> | <span data-ttu-id="e0b95-118">Ruft den Bezeichner der Aktion ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e0b95-118">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="e0b95-119">**type**</span><span class="sxs-lookup"><span data-stu-id="e0b95-119">**Type**</span></span>](action-type.md)<br/> | <span data-ttu-id="e0b95-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e0b95-120">Read-only</span></span><br/>  | <span data-ttu-id="e0b95-121">Ruft den Typ der Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="e0b95-121">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="e0b95-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0b95-122">Remarks</span></span>

<span data-ttu-id="e0b95-123">Informationen zur Zusammenarbeit von Aktionen und Aufgaben finden Sie unter [Aufgaben Aktionen](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e0b95-123">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span> <span data-ttu-id="e0b95-124">Die folgende Tabelle enthält die Skript Objekte, die die Aktionen darstellen, die ausgeführt werden können:</span><span class="sxs-lookup"><span data-stu-id="e0b95-124">The following table contains the scripting objects that represent the actions that can be performed:</span></span>



| <span data-ttu-id="e0b95-125">API</span><span class="sxs-lookup"><span data-stu-id="e0b95-125">API</span></span>                                            | <span data-ttu-id="e0b95-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0b95-126">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e0b95-127">**Comhandleraction**</span><span class="sxs-lookup"><span data-stu-id="e0b95-127">**ComHandlerAction**</span></span>](comhandleraction.md)   | <span data-ttu-id="e0b95-128">Stellt eine Aktion dar, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="e0b95-128">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="e0b95-129">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="e0b95-129">**ExecAction**</span></span>](execaction.md)               | <span data-ttu-id="e0b95-130">Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="e0b95-130">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="e0b95-131">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="e0b95-131">**EmailAction**</span></span>](emailaction.md)             | <span data-ttu-id="e0b95-132">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="e0b95-132">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="e0b95-133">**Showmessageaction**</span><span class="sxs-lookup"><span data-stu-id="e0b95-133">**ShowMessageAction**</span></span>](showmessageaction.md) | <span data-ttu-id="e0b95-134">Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e0b95-134">Represents an action that shows a message box.</span></span>               |



 

<span data-ttu-id="e0b95-135">Beim Lesen oder Schreiben von XML werden die Aktionen einer Aufgabe im [**Actions**](taskschedulerschema-actions-tasktype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="e0b95-135">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="e0b95-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0b95-136">Examples</span></span>

<span data-ttu-id="e0b95-137">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md) , [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den täglichen Auslösung [(Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen wöchentlichen Aufruf [(](weekly-trigger-example--scripting-.md)Skripterstellung), Beispiel für LOGON-Beispiel [(Skript](logon-trigger-example--scripting-.md)Erstellung) oder [Beispiel](boot-trigger-example--scripting-.md)für</span><span class="sxs-lookup"><span data-stu-id="e0b95-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b95-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0b95-138">Requirements</span></span>



| <span data-ttu-id="e0b95-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0b95-139">Requirement</span></span> | <span data-ttu-id="e0b95-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e0b95-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b95-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0b95-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b95-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0b95-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e0b95-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0b95-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b95-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0b95-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0b95-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e0b95-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0b95-146"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e0b95-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e0b95-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b95-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b95-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b95-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b95-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0b95-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b95-150">Skript Objekte Taskplaner</span><span class="sxs-lookup"><span data-stu-id="e0b95-150">Task Scheduler Scripting Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="e0b95-151">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="e0b95-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





