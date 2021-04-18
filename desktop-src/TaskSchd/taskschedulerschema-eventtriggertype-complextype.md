---
title: komplexer eventtriggertype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das EventTrigger-Element.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- komplexer ereignistriggertyp Taskplaner
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345495"
---
# <a name="eventtriggertype-complex-type"></a><span data-ttu-id="584dc-104">komplexer eventtriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="584dc-104">eventTriggerType Complex Type</span></span>

<span data-ttu-id="584dc-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="584dc-105">Defines the child elements and sequencing information for the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="584dc-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="584dc-106">Child elements</span></span>



| <span data-ttu-id="584dc-107">Element</span><span class="sxs-lookup"><span data-stu-id="584dc-107">Element</span></span>                                                                           | <span data-ttu-id="584dc-108">type</span><span class="sxs-lookup"><span data-stu-id="584dc-108">Type</span></span>                                                                    | <span data-ttu-id="584dc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="584dc-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="584dc-110">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="584dc-110">**Delay**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="584dc-111">duration</span><span class="sxs-lookup"><span data-stu-id="584dc-111">duration</span></span>                                                                | <span data-ttu-id="584dc-112">Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="584dc-112">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="584dc-113">**Abonnement**</span><span class="sxs-lookup"><span data-stu-id="584dc-113">**Subscription**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | [<span data-ttu-id="584dc-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="584dc-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="584dc-115">Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.</span><span class="sxs-lookup"><span data-stu-id="584dc-115">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="584dc-116">**Valuequeries**</span><span class="sxs-lookup"><span data-stu-id="584dc-116">**ValueQueries**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="584dc-117">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="584dc-117">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)      | <span data-ttu-id="584dc-118">Gibt eine Sequenz von Elementen an, die jeweils einen Namen und einen XPath-Abfrage Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="584dc-118">Specifies a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="584dc-119">Die Abfragen werden auf ein Ereignis angewendet, das von dem im [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) Element angegebenen Ereignis Abonnement zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="584dc-119">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="584dc-120">Der Name des XPath-Abfrage Werts kann als Variable im [**Body**](taskschedulerschema-body-showmessagetype-element.md) -Element im [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) -Aktions Abschnitt einer Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="584dc-120">The name for the XPath query value can be used as a variable in the [**Body**](taskschedulerschema-body-showmessagetype-element.md) element in the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) action section of a task.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="584dc-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="584dc-121">Remarks</span></span>

<span data-ttu-id="584dc-122">Zusätzlich zum untergeordneten-Element, das hier definiert ist, verwendet das [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.</span><span class="sxs-lookup"><span data-stu-id="584dc-122">In addition to the child element defined here, the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="584dc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="584dc-123">Requirements</span></span>



| <span data-ttu-id="584dc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="584dc-124">Requirement</span></span> | <span data-ttu-id="584dc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="584dc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="584dc-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="584dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="584dc-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="584dc-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="584dc-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="584dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="584dc-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="584dc-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="584dc-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="584dc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="584dc-131">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="584dc-131">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="584dc-132">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="584dc-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





