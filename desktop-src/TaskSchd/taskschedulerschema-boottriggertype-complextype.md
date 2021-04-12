---
title: komplexer boottriggertype-Typ
description: Definiert das untergeordnete Element und die Sequenzierungs Informationen für das boottrigger-Element.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- komplexer boottriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478192"
---
# <a name="boottriggertype-complex-type"></a><span data-ttu-id="b7c87-104">komplexer boottriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="b7c87-104">bootTriggerType Complex Type</span></span>

<span data-ttu-id="b7c87-105">Definiert das untergeordnete Element und die Sequenzierungs Informationen für das [**boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="b7c87-105">Defines the child element and sequencing information for the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="bootTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b7c87-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7c87-106">Child elements</span></span>



| <span data-ttu-id="b7c87-107">Element</span><span class="sxs-lookup"><span data-stu-id="b7c87-107">Element</span></span>                                                            | <span data-ttu-id="b7c87-108">type</span><span class="sxs-lookup"><span data-stu-id="b7c87-108">Type</span></span>     | <span data-ttu-id="b7c87-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7c87-109">Description</span></span>                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7c87-110">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="b7c87-110">**Delay**</span></span>](taskschedulerschema-delay-boottriggertype-element.md) | <span data-ttu-id="b7c87-111">duration</span><span class="sxs-lookup"><span data-stu-id="b7c87-111">duration</span></span> | <span data-ttu-id="b7c87-112">Zeitspanne zwischen dem Starten des Systems und dem Auslösen des Auslösers.</span><span class="sxs-lookup"><span data-stu-id="b7c87-112">Amount of time between when the system is booted and when the trigger is fired.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="b7c87-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7c87-113">Remarks</span></span>

<span data-ttu-id="b7c87-114">Zusätzlich zum untergeordneten-Element, das hier definiert ist, verwendet das [**boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b7c87-114">In addition to the child element defined here, the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c87-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7c87-115">Requirements</span></span>



| <span data-ttu-id="b7c87-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7c87-116">Requirement</span></span> | <span data-ttu-id="b7c87-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b7c87-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b7c87-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7c87-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c87-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7c87-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b7c87-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7c87-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c87-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7c87-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7c87-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7c87-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c87-123">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="b7c87-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b7c87-124">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b7c87-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





