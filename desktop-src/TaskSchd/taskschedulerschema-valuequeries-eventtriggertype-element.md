---
title: Valuequeries (eventtriggertype)-Element
description: Enthält eine Sequenz von-Elementen, die jeweils einen Namen und einen XPath-Abfrage Wert enthalten.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Valuequeries-Element Taskplaner
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949570"
---
# <a name="valuequeries-eventtriggertype-element"></a><span data-ttu-id="6342f-104">Valuequeries (eventtriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="6342f-104">ValueQueries (eventTriggerType) Element</span></span>

<span data-ttu-id="6342f-105">Enthält eine Sequenz von-Elementen, die jeweils einen Namen und einen XPath-Abfrage Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="6342f-105">Contains a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="6342f-106">Die Abfragen werden auf ein Ereignis angewendet, das von dem im [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) Element angegebenen Ereignis Abonnement zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6342f-106">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="6342f-107">Der Name des XPath-Abfrage Werts kann als Variable im Aktions Abschnitt einer Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6342f-107">The name for the XPath query value can be used as a variable in the action section of a task.</span></span>

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

<span data-ttu-id="6342f-108">Das **valuequeries** -Element wird durch den komplexen [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="6342f-108">The **ValueQueries** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6342f-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="6342f-109">Parent element</span></span>



| <span data-ttu-id="6342f-110">Element</span><span class="sxs-lookup"><span data-stu-id="6342f-110">Element</span></span>                                                                                      | <span data-ttu-id="6342f-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="6342f-111">Derived from</span></span>                                                                 | <span data-ttu-id="6342f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6342f-112">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="6342f-113">**EventTrigger (triggergroup)**</span><span class="sxs-lookup"><span data-stu-id="6342f-113">**EventTrigger (triggerGroup)**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="6342f-114">**eventtriggertype**</span><span class="sxs-lookup"><span data-stu-id="6342f-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="6342f-115">Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="6342f-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6342f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6342f-116">Remarks</span></span>

<span data-ttu-id="6342f-117">Informationen zur C++-Entwicklung finden Sie unter [**valuequeries-Eigenschaft von ieventvent**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span><span class="sxs-lookup"><span data-stu-id="6342f-117">For C++ development, see [**ValueQueries Property of IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).</span></span>

<span data-ttu-id="6342f-118">Informationen zur Skript Entwicklung finden Sie unter [**EventTrigger. valuequeries**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="6342f-118">For script development, see [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6342f-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6342f-119">Examples</span></span>

<span data-ttu-id="6342f-120">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Ereignis Auslösers mit diesem Element angibt, finden Sie unter [Event-auslöserbeispiel (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6342f-120">For a complete example of the XML for a task that specifies a an event trigger using this element, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6342f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6342f-121">Requirements</span></span>



| <span data-ttu-id="6342f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6342f-122">Requirement</span></span> | <span data-ttu-id="6342f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6342f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6342f-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6342f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6342f-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6342f-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6342f-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6342f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6342f-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6342f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

