---
title: Actions (TaskType)-Element
description: Enthält die Aktionen, die vom Task ausgeführt werden.
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- Aktionen (TaskType)-Element Taskplaner
- Aktionen Taskplaner, XML
- Actions-Element Taskplaner
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391695"
---
# <a name="actions-tasktype-element"></a><span data-ttu-id="fbe7c-106">Actions (TaskType)-Element</span><span class="sxs-lookup"><span data-stu-id="fbe7c-106">Actions (taskType) Element</span></span>

<span data-ttu-id="fbe7c-107">Enthält die Aktionen, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-107">Contains the actions performed by the task.</span></span>

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

<span data-ttu-id="fbe7c-108">Das **Actions** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-108">The **Actions** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fbe7c-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="fbe7c-109">Parent element</span></span>



| <span data-ttu-id="fbe7c-110">Element</span><span class="sxs-lookup"><span data-stu-id="fbe7c-110">Element</span></span>                                          | <span data-ttu-id="fbe7c-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="fbe7c-111">Derived from</span></span>                                                 | <span data-ttu-id="fbe7c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbe7c-112">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="fbe7c-113">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-113">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="fbe7c-114">**taskType**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-114">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="fbe7c-115">Beschreibt den Task, der vom Taskplaner-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-115">Describes the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="fbe7c-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbe7c-116">Child elements</span></span>



| <span data-ttu-id="fbe7c-117">Element</span><span class="sxs-lookup"><span data-stu-id="fbe7c-117">Element</span></span>                                                                    | <span data-ttu-id="fbe7c-118">type</span><span class="sxs-lookup"><span data-stu-id="fbe7c-118">Type</span></span>                                                                       | <span data-ttu-id="fbe7c-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbe7c-119">Description</span></span>                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="fbe7c-120">**Comhandler**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-120">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="fbe7c-121">**comhandlertype**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-121">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="fbe7c-122">Gibt eine Aktion an, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-122">Specifies an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="fbe7c-123">**Exec**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-123">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="fbe7c-124">**exectype**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-124">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="fbe7c-125">Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-125">Specifies an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="fbe7c-126">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-126">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="fbe7c-127">**sendemailtype**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-127">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="fbe7c-128">Gibt eine Aktion an, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-128">Specifies an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="fbe7c-129">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-129">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="fbe7c-130">**showmessagetype**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-130">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="fbe7c-131">Gibt eine Aktion an, die ein Meldungs Feld anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-131">Specifies an action that shows a message box.</span></span><br/>               |



## <a name="attributes"></a><span data-ttu-id="fbe7c-132">Attributes</span><span class="sxs-lookup"><span data-stu-id="fbe7c-132">Attributes</span></span>



| <span data-ttu-id="fbe7c-133">Name</span><span class="sxs-lookup"><span data-stu-id="fbe7c-133">Name</span></span>    | <span data-ttu-id="fbe7c-134">type</span><span class="sxs-lookup"><span data-stu-id="fbe7c-134">Type</span></span> | <span data-ttu-id="fbe7c-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbe7c-135">Description</span></span>                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe7c-136">Kontext</span><span class="sxs-lookup"><span data-stu-id="fbe7c-136">Context</span></span> |      | <span data-ttu-id="fbe7c-137">Prinzipal Bezeichner des Benutzers, der der Sicherheitskontext für die Aktionen der Aufgabe ist.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-137">Principal identifier of the user who is the security context for the actions of the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fbe7c-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbe7c-138">Remarks</span></span>

<span data-ttu-id="fbe7c-139">Die zuvor aufgelisteten untergeordneten Elemente (Maximum 32) werden von der Gruppe " [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-139">The child elements listed previously (maximum 32) are defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) group.</span></span> <span data-ttu-id="fbe7c-140">Diese Elemente können in beliebiger Reihenfolge hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-140">These elements can be added in any order.</span></span>

<span data-ttu-id="fbe7c-141">Bei der C++-Entwicklung werden die Aktionen einer Aufgabe in der [**iaktioncollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-141">For C++ development, the actions of a task are defined in the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface.</span></span>

<span data-ttu-id="fbe7c-142">Bei der Skript Entwicklung werden die Aktionen einer Aufgabe im [**Aktions Sammlungs**](actioncollection.md) Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-142">For script development, the actions of a task are defined in the [**ActionCollection**](actioncollection.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="fbe7c-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbe7c-143">Examples</span></span>

<span data-ttu-id="fbe7c-144">Weitere Informationen und ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die eine einzelne Ausführungs Aktion enthält, finden Sie unter [time-triggerbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="fbe7c-144">For more information and a complete example of the XML for a task that contains a single execution action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbe7c-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbe7c-145">Requirements</span></span>



| <span data-ttu-id="fbe7c-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbe7c-146">Requirement</span></span> | <span data-ttu-id="fbe7c-147">Wert</span><span class="sxs-lookup"><span data-stu-id="fbe7c-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbe7c-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbe7c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fbe7c-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbe7c-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbe7c-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbe7c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fbe7c-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbe7c-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbe7c-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbe7c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe7c-153">**taskType**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-153">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[<span data-ttu-id="fbe7c-154">**Action Group**</span><span class="sxs-lookup"><span data-stu-id="fbe7c-154">**actionGroup**</span></span>](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[<span data-ttu-id="fbe7c-155">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="fbe7c-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="fbe7c-156">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="fbe7c-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





