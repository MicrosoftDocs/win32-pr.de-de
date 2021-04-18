---
title: komplexer registrationtriggertype-Typ
description: Definiert untergeordnete Elemente und Sequenzierungs Informationen für das Registration-Auslöserelement.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- komplexer registrationtriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392082"
---
# <a name="registrationtriggertype-complex-type"></a><span data-ttu-id="38d63-104">komplexer registrationtriggertype-Typ</span><span class="sxs-lookup"><span data-stu-id="38d63-104">registrationTriggerType Complex Type</span></span>

<span data-ttu-id="38d63-105">Definiert untergeordnete Elemente und Sequenzierungs Informationen für das [**Registration-Auslöserelement**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="38d63-105">Defines child elements and sequencing information for the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationTriggerType">
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

## <a name="child-elements"></a><span data-ttu-id="38d63-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38d63-106">Child elements</span></span>



| <span data-ttu-id="38d63-107">Element</span><span class="sxs-lookup"><span data-stu-id="38d63-107">Element</span></span>                                                                    | <span data-ttu-id="38d63-108">type</span><span class="sxs-lookup"><span data-stu-id="38d63-108">Type</span></span>     | <span data-ttu-id="38d63-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38d63-109">Description</span></span>                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38d63-110">**Verzögern**</span><span class="sxs-lookup"><span data-stu-id="38d63-110">**Delay**</span></span>](taskschedulerschema-delay-registrationtriggertype-element.md) | <span data-ttu-id="38d63-111">duration</span><span class="sxs-lookup"><span data-stu-id="38d63-111">duration</span></span> | <span data-ttu-id="38d63-112">Gibt die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="38d63-112">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="38d63-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38d63-113">Remarks</span></span>

<span data-ttu-id="38d63-114">Zusätzlich zu den hier definierten untergeordneten Elementen verwendet das [**registrationtrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.</span><span class="sxs-lookup"><span data-stu-id="38d63-114">In addition to the child elements defined here, the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d63-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38d63-115">Requirements</span></span>



| <span data-ttu-id="38d63-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38d63-116">Requirement</span></span> | <span data-ttu-id="38d63-117">Wert</span><span class="sxs-lookup"><span data-stu-id="38d63-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38d63-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38d63-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38d63-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38d63-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38d63-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38d63-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38d63-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38d63-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38d63-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38d63-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d63-123">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="38d63-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="38d63-124">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="38d63-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





