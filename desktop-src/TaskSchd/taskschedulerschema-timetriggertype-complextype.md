---
title: komplexer timetriggertype-Typ
description: Definiert den Basistyp für das Time-Auslöserelement.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- komplexer timetriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342187"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="b2d07-104">komplexer timetriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="b2d07-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="b2d07-105">Definiert den Basistyp für das [**time-Auslöserelement**](taskschedulerschema-timetrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b2d07-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="b2d07-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2d07-106">Child elements</span></span>



| <span data-ttu-id="b2d07-107">Element</span><span class="sxs-lookup"><span data-stu-id="b2d07-107">Element</span></span>                                                                        | <span data-ttu-id="b2d07-108">type</span><span class="sxs-lookup"><span data-stu-id="b2d07-108">Type</span></span>     | <span data-ttu-id="b2d07-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2d07-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2d07-110">**Randomdelay**</span><span class="sxs-lookup"><span data-stu-id="b2d07-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="b2d07-111">duration</span><span class="sxs-lookup"><span data-stu-id="b2d07-111">duration</span></span> | <span data-ttu-id="b2d07-112">Gibt die Verzögerungszeit an, die der Startzeit des Auslösers nach dem Zufallsprinzip hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b2d07-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="b2d07-113">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S (z. b. P2DT5S ist eine Verzögerung von 2 Tagen, 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="b2d07-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="b2d07-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2d07-114">Remarks</span></span>

<span data-ttu-id="b2d07-115">Beachten Sie, dass dieses Element keine untergeordneten Elemente zu den durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definierten Elementen hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b2d07-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d07-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2d07-116">Requirements</span></span>



| <span data-ttu-id="b2d07-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2d07-117">Requirement</span></span> | <span data-ttu-id="b2d07-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b2d07-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2d07-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2d07-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d07-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2d07-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2d07-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2d07-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d07-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2d07-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2d07-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2d07-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d07-124">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="b2d07-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b2d07-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="b2d07-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





