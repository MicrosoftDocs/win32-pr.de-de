---
title: Comhandleraction-Objekt
description: Skript Objekt, das eine Aktion darstellt, die einen Handler auslöst.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- COM-handleraktion Taskplaner, Objekt
- Comhandleraction-Objekt Taskplaner
- Comhandleraction-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475045"
---
# <a name="comhandleraction-object"></a><span data-ttu-id="d607e-106">Comhandleraction-Objekt</span><span class="sxs-lookup"><span data-stu-id="d607e-106">ComHandlerAction object</span></span>

<span data-ttu-id="d607e-107">Skript Objekt, das eine Aktion darstellt, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="d607e-107">Scripting object that represents an action that fires a handler.</span></span>

## <a name="members"></a><span data-ttu-id="d607e-108">Member</span><span class="sxs-lookup"><span data-stu-id="d607e-108">Members</span></span>

<span data-ttu-id="d607e-109">Das **comhandleraction** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d607e-109">The **ComHandlerAction** object has these types of members:</span></span>

-   [<span data-ttu-id="d607e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d607e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d607e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d607e-111">Properties</span></span>

<span data-ttu-id="d607e-112">Das **comhandleraction** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d607e-112">The **ComHandlerAction** object has these properties.</span></span>



| <span data-ttu-id="d607e-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d607e-113">Property</span></span>                                               | <span data-ttu-id="d607e-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="d607e-114">Access type</span></span>           | <span data-ttu-id="d607e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d607e-115">Description</span></span>                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d607e-116">**ClassID**</span><span class="sxs-lookup"><span data-stu-id="d607e-116">**ClassId**</span></span>](comhandleraction-classid.md)<br/> | <span data-ttu-id="d607e-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d607e-117">Read/write</span></span><br/> | <span data-ttu-id="d607e-118">Ruft den Bezeichner der Handlerklasse ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d607e-118">Gets or sets the identifier of the handler class.</span></span><br/>                                              |
| [<span data-ttu-id="d607e-119">**Daten**</span><span class="sxs-lookup"><span data-stu-id="d607e-119">**Data**</span></span>](comhandleraction-data.md)<br/>       | <span data-ttu-id="d607e-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d607e-120">Read/write</span></span><br/> | <span data-ttu-id="d607e-121">Ruft zusätzliche Daten ab, die dem Handler zugeordnet sind, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d607e-121">Gets or sets additional data that is associated with the handler.</span></span><br/>                              |
| [<span data-ttu-id="d607e-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="d607e-122">**Id**</span></span>](action-id.md)<br/>                     | <span data-ttu-id="d607e-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d607e-123">Read/write</span></span><br/> | <span data-ttu-id="d607e-124">Wird vom [**Action**](action.md) -Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="d607e-124">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="d607e-125">Ruft den Bezeichner der Aktion ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="d607e-125">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="d607e-126">**type**</span><span class="sxs-lookup"><span data-stu-id="d607e-126">**Type**</span></span>](action-type.md)<br/>                 | <span data-ttu-id="d607e-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d607e-127">Read-only</span></span><br/>  | <span data-ttu-id="d607e-128">Wird vom [**Action**](action.md) -Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="d607e-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="d607e-129">Ruft den Typ der Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="d607e-129">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="d607e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d607e-130">Remarks</span></span>

<span data-ttu-id="d607e-131">COM-Handler müssen die [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) -Schnittstelle für das Taskplaner implementieren, um den Handler zu starten und anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="d607e-131">COM handlers must implement the [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) interface for the Task Scheduler to start and stop the handler.</span></span> <span data-ttu-id="d607e-132">Der com-Handler verwendet wiederum die Methoden des [**taskhandlerstatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) -Objekts, um den Status zurück an den Taskplaner zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d607e-132">In turn, the COM handler uses the methods of the [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) object to communicate the status back to the Task Scheduler.</span></span>

<span data-ttu-id="d607e-133">Beim Lesen oder Schreiben von XML wird eine com-handleraktion im [**comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="d607e-133">When reading or writing XML, a COM handler action is specified in the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d607e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d607e-134">Requirements</span></span>



| <span data-ttu-id="d607e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d607e-135">Requirement</span></span> | <span data-ttu-id="d607e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d607e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d607e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d607e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d607e-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d607e-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d607e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d607e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d607e-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d607e-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d607e-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d607e-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="d607e-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d607e-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d607e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d607e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d607e-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d607e-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d607e-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d607e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d607e-146">**Taskhandlerstatus**</span><span class="sxs-lookup"><span data-stu-id="d607e-146">**TaskHandlerStatus**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[<span data-ttu-id="d607e-147">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="d607e-147">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="d607e-148">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d607e-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





