---
title: komplexer triggerbasetype-Typ
description: Definiert das Attribut, die untergeordneten Basiselemente und die Sequenzierungs Informationen für alle komplexen Auslösertypen.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- komplexer triggerbasetype-Typ Taskplaner
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341297"
---
# <a name="triggerbasetype-complex-type"></a><span data-ttu-id="a164d-104">komplexer triggerbasetype-Typ</span><span class="sxs-lookup"><span data-stu-id="a164d-104">triggerBaseType Complex Type</span></span>

<span data-ttu-id="a164d-105">Definiert das Attribut, die untergeordneten Basiselemente und die Sequenzierungs Informationen für alle komplexen Auslösertypen.</span><span class="sxs-lookup"><span data-stu-id="a164d-105">Defines the attribute, base child elements, and sequencing information for all trigger complex types.</span></span>

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a164d-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a164d-106">Child elements</span></span>



| <span data-ttu-id="a164d-107">Element</span><span class="sxs-lookup"><span data-stu-id="a164d-107">Element</span></span>                                                                                      | <span data-ttu-id="a164d-108">type</span><span class="sxs-lookup"><span data-stu-id="a164d-108">Type</span></span>                                                                     | <span data-ttu-id="a164d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a164d-109">Description</span></span>                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a164d-110">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="a164d-110">**Enabled**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="a164d-111">boolean</span><span class="sxs-lookup"><span data-stu-id="a164d-111">boolean</span></span>                                                                  | <span data-ttu-id="a164d-112">Gibt an, dass der-Wert aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a164d-112">Specifies that the trigger is enabled.</span></span><br/>                                                                      |
| [<span data-ttu-id="a164d-113">**Endgrenze**</span><span class="sxs-lookup"><span data-stu-id="a164d-113">**EndBoundary**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="a164d-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="a164d-114">dateTime</span></span>                                                                 | <span data-ttu-id="a164d-115">Das Datum und die Uhrzeit der Deaktivierung des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="a164d-115">The date and time when the trigger is deactivated.</span></span><br/>                                                          |
| [<span data-ttu-id="a164d-116">**Executiontimelimit**</span><span class="sxs-lookup"><span data-stu-id="a164d-116">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="a164d-117">duration</span><span class="sxs-lookup"><span data-stu-id="a164d-117">duration</span></span>                                                                 | <span data-ttu-id="a164d-118">Gibt das Intervall an, in dem der-Task den Task starten kann.</span><span class="sxs-lookup"><span data-stu-id="a164d-118">Specifies the interval when the trigger can start the task.</span></span><br/>                                                 |
| [<span data-ttu-id="a164d-119">**Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="a164d-119">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="a164d-120">**Wiederholungstyp**</span><span class="sxs-lookup"><span data-stu-id="a164d-120">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="a164d-121">Gibt an, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Auslösen des Triggers wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="a164d-121">Specifies how often the task is run and how long the repetition pattern is repeated once the trigger fires.</span></span><br/> |
| [<span data-ttu-id="a164d-122">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="a164d-122">**StartBoundary**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="a164d-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="a164d-123">dateTime</span></span>                                                                 | <span data-ttu-id="a164d-124">Das Datum und die Uhrzeit der Aktivierung des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="a164d-124">The date and time when the trigger is activated.</span></span><br/>                                                            |



## <a name="attributes"></a><span data-ttu-id="a164d-125">Attributes</span><span class="sxs-lookup"><span data-stu-id="a164d-125">Attributes</span></span>



| <span data-ttu-id="a164d-126">Name</span><span class="sxs-lookup"><span data-stu-id="a164d-126">Name</span></span> | <span data-ttu-id="a164d-127">type</span><span class="sxs-lookup"><span data-stu-id="a164d-127">Type</span></span> | <span data-ttu-id="a164d-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a164d-128">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="a164d-129">id</span><span class="sxs-lookup"><span data-stu-id="a164d-129">id</span></span>   | <span data-ttu-id="a164d-130">id</span><span class="sxs-lookup"><span data-stu-id="a164d-130">ID</span></span>   | <span data-ttu-id="a164d-131">Der Bezeichner des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="a164d-131">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a164d-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a164d-132">Remarks</span></span>

<span data-ttu-id="a164d-133">Zu den komplexen Auslösertypen zählen die folgenden.</span><span class="sxs-lookup"><span data-stu-id="a164d-133">Trigger complex types include the following.</span></span>

-   [<span data-ttu-id="a164d-134">**boottriggertype**</span><span class="sxs-lookup"><span data-stu-id="a164d-134">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="a164d-135">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="a164d-135">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="a164d-136">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="a164d-136">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="a164d-137">**idletriggertype**</span><span class="sxs-lookup"><span data-stu-id="a164d-137">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="a164d-138">**logontriggertype**</span><span class="sxs-lookup"><span data-stu-id="a164d-138">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="a164d-139">**registrationtriggertype**</span><span class="sxs-lookup"><span data-stu-id="a164d-139">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="a164d-140">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="a164d-140">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a><span data-ttu-id="a164d-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a164d-141">Requirements</span></span>



| <span data-ttu-id="a164d-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a164d-142">Requirement</span></span> | <span data-ttu-id="a164d-143">Wert</span><span class="sxs-lookup"><span data-stu-id="a164d-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a164d-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a164d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a164d-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a164d-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a164d-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a164d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a164d-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a164d-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a164d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a164d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a164d-149">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="a164d-149">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a164d-150">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a164d-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





