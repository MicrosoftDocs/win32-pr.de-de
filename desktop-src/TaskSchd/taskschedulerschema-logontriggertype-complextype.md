---
title: komplexer logontriggertype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Logon-Auslöserelement.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- komplexer logontriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340015"
---
# <a name="logontriggertype-complex-type"></a><span data-ttu-id="42d46-104">komplexer logontriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="42d46-104">logonTriggerType Complex Type</span></span>

<span data-ttu-id="42d46-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**Logon-Auslöserelement**](taskschedulerschema-logontrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="42d46-105">Defines the child elements and sequencing information for the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
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

## <a name="child-elements"></a><span data-ttu-id="42d46-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42d46-106">Child elements</span></span>



| <span data-ttu-id="42d46-107">Element</span><span class="sxs-lookup"><span data-stu-id="42d46-107">Element</span></span>                                                               | <span data-ttu-id="42d46-108">type</span><span class="sxs-lookup"><span data-stu-id="42d46-108">Type</span></span>                                                                    | <span data-ttu-id="42d46-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42d46-109">Description</span></span>                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42d46-110">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="42d46-110">**Delay**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)   | <span data-ttu-id="42d46-111">duration</span><span class="sxs-lookup"><span data-stu-id="42d46-111">duration</span></span>                                                                | <span data-ttu-id="42d46-112">Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="42d46-112">Amount of time between when the user logs on and when the task is started.</span></span><br/>         |
| [<span data-ttu-id="42d46-113">**UserID**</span><span class="sxs-lookup"><span data-stu-id="42d46-113">**UserId**</span></span>](taskschedulerschema-userid-logontriggertype-element.md) | [<span data-ttu-id="42d46-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="42d46-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="42d46-115">Der Bezeichner des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="42d46-115">Identifier of the user.</span></span> <span data-ttu-id="42d46-116">Der Task wird gestartet, wenn sich dieser Benutzer auf dem Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="42d46-116">The task is started when this user logs onto the computer.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="42d46-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42d46-117">Remarks</span></span>

<span data-ttu-id="42d46-118">Zusätzlich zu den hier definierten untergeordneten Elementen verwendet das [**logontrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.</span><span class="sxs-lookup"><span data-stu-id="42d46-118">In addition to the child elements defined here, the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d46-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42d46-119">Requirements</span></span>



| <span data-ttu-id="42d46-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42d46-120">Requirement</span></span> | <span data-ttu-id="42d46-121">Wert</span><span class="sxs-lookup"><span data-stu-id="42d46-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42d46-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42d46-122">Minimum supported client</span></span><br/> | <span data-ttu-id="42d46-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42d46-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="42d46-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42d46-124">Minimum supported server</span></span><br/> | <span data-ttu-id="42d46-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42d46-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42d46-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42d46-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d46-127">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="42d46-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="42d46-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="42d46-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





