---
title: komplexer timeTriggerType-Typ
description: Definiert den Basistyp für das TimeTrigger-Element.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- komplexer timeTriggerType-Typ Taskplaner
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f44f0959a9f67e4bfee0b0ef5dd7f095ffbadce
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734135"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="d6f7e-104">komplexer timeTriggerType-Typ</span><span class="sxs-lookup"><span data-stu-id="d6f7e-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="d6f7e-105">Definiert den Basistyp für das [**TimeTrigger-Element.**](taskschedulerschema-timetrigger-triggergroup-element.md)</span><span class="sxs-lookup"><span data-stu-id="d6f7e-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d6f7e-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6f7e-106">Child elements</span></span>



| <span data-ttu-id="d6f7e-107">Element</span><span class="sxs-lookup"><span data-stu-id="d6f7e-107">Element</span></span>                                                                        | <span data-ttu-id="d6f7e-108">Typ</span><span class="sxs-lookup"><span data-stu-id="d6f7e-108">Type</span></span>     | <span data-ttu-id="d6f7e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6f7e-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6f7e-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="d6f7e-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="d6f7e-111">duration</span><span class="sxs-lookup"><span data-stu-id="d6f7e-111">duration</span></span> | <span data-ttu-id="d6f7e-112">Gibt die Verzögerungszeit an, die zufällig zur Startzeit des Triggers hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f7e-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="d6f7e-113">Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (p2DT5S ist z. B. eine Verzögerung von 2 Tagen und 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="d6f7e-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="d6f7e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6f7e-114">Remarks</span></span>

<span data-ttu-id="d6f7e-115">Beachten Sie, dass dieses Element keine untergeordneten Elemente zu den elementen hinzufüge, die vom komplexen [**triggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6f7e-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f7e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6f7e-116">Requirements</span></span>



| <span data-ttu-id="d6f7e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6f7e-117">Requirement</span></span> | <span data-ttu-id="d6f7e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d6f7e-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6f7e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6f7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f7e-120">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6f7e-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6f7e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6f7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f7e-122">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6f7e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6f7e-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d6f7e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f7e-124">komplexe Schematypen Taskplaner</span><span class="sxs-lookup"><span data-stu-id="d6f7e-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="d6f7e-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d6f7e-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





