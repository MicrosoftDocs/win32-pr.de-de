---
title: Duration (idlesettingstype)-Element
description: Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Duration-Element Taskplaner
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517564"
---
# <a name="duration-idlesettingstype-element"></a><span data-ttu-id="5f856-104">Duration (idlesettingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="5f856-104">Duration (idleSettingsType) Element</span></span>

<span data-ttu-id="5f856-105">Gibt an, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f856-105">Specifies how long the computer must be in an idle state before the task is run.</span></span> <span data-ttu-id="5f856-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="5f856-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="5f856-107">Der Mindestwert ist eine Minute.</span><span class="sxs-lookup"><span data-stu-id="5f856-107">The minimum value is one minute.</span></span> <span data-ttu-id="5f856-108">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="5f856-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Duration"
    default="PT10M"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="5f856-109">Das-Element wird durch den komplexen Typ [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="5f856-109">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5f856-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="5f856-110">Parent element</span></span>



| <span data-ttu-id="5f856-111">Element</span><span class="sxs-lookup"><span data-stu-id="5f856-111">Element</span></span>                                                                       | <span data-ttu-id="5f856-112">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="5f856-112">Derived from</span></span>                                                                 | <span data-ttu-id="5f856-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f856-113">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f856-114">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="5f856-114">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="5f856-115">**idlesettingstype**</span><span class="sxs-lookup"><span data-stu-id="5f856-115">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="5f856-116">Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="5f856-116">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5f856-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f856-117">Remarks</span></span>

<span data-ttu-id="5f856-118">Bei der Skriptprogrammierung wird diese Einstellung für den Leerlauf mithilfe der [**idlesettings. idleduration**](idlesettings-idleduration.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="5f856-118">For script programming, this idle setting is specified using the [**IdleSettings.IdleDuration**](idlesettings-idleduration.md) property.</span></span>

<span data-ttu-id="5f856-119">Bei der C++-Programmierung wird diese Einstellung für den Leerlauf mithilfe der [**iidlesettings:: idleduration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="5f856-119">For C++ programming, this idle setting is specified using the [**IIdleSettings::IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="5f856-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f856-120">Examples</span></span>

<span data-ttu-id="5f856-121">Der folgende XML-Code definiert eine Leerlauf Einstellung, die 5 Minuten für den Start der Aufgabe zulässt.</span><span class="sxs-lookup"><span data-stu-id="5f856-121">The following XML defines an idle setting that allows 5 minutes for the task to start.</span></span>


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="5f856-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f856-122">Requirements</span></span>



| <span data-ttu-id="5f856-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f856-123">Requirement</span></span> | <span data-ttu-id="5f856-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5f856-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5f856-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f856-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5f856-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f856-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5f856-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f856-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5f856-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f856-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f856-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f856-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f856-130">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="5f856-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5f856-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="5f856-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





