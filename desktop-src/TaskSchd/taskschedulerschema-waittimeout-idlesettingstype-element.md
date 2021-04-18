---
title: WaitTimeout (idlesettingstype)-Element
description: Gibt die Zeitspanne an, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- WaitTimeout-Element Taskplaner
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518479"
---
# <a name="waittimeout-idlesettingstype-element"></a><span data-ttu-id="06960-104">WaitTimeout (idlesettingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="06960-104">WaitTimeout (idleSettingsType) Element</span></span>

<span data-ttu-id="06960-105">Gibt die Zeitspanne an, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.</span><span class="sxs-lookup"><span data-stu-id="06960-105">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="06960-106">Wenn für dieses Element kein Wert angegeben wird, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlauf Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="06960-106">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span> <span data-ttu-id="06960-107">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="06960-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="06960-108">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="06960-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="06960-109">Die zulässige minimal Zeit beträgt 1 Minute.</span><span class="sxs-lookup"><span data-stu-id="06960-109">The minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
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

<span data-ttu-id="06960-110">Das-Element wird durch den komplexen Typ [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="06960-110">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="06960-111">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="06960-111">Parent element</span></span>



| <span data-ttu-id="06960-112">Element</span><span class="sxs-lookup"><span data-stu-id="06960-112">Element</span></span>                                                                       | <span data-ttu-id="06960-113">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="06960-113">Derived from</span></span>                                                                 | <span data-ttu-id="06960-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06960-114">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06960-115">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="06960-115">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="06960-116">**idlesettingstype**</span><span class="sxs-lookup"><span data-stu-id="06960-116">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="06960-117">Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="06960-117">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="06960-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06960-118">Remarks</span></span>

<span data-ttu-id="06960-119">Bei der Skript Entwicklung wird diese Einstellung für den Leerlauf mithilfe der [**idlesettings. WaitTimeout**](idlesettings-waittimeout.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="06960-119">For script development, this idle setting is specified using the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property.</span></span>

<span data-ttu-id="06960-120">Bei der C++-Entwicklung wird diese Einstellung für den Leerlauf mithilfe der [**iidlesettings:: WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="06960-120">For C++ development, this idle setting is specified using the [**IIdleSettings::WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property.</span></span>

## <a name="examples"></a><span data-ttu-id="06960-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06960-121">Examples</span></span>

<span data-ttu-id="06960-122">Der folgende XML-Code definiert eine Leerlauf Einstellung, die 24 Stunden wartet, bis eine Leerlauf Bedingung auftritt.</span><span class="sxs-lookup"><span data-stu-id="06960-122">The following XML defines an idle setting that waits 24 hours for an idle condition to occur.</span></span>


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="06960-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06960-123">Requirements</span></span>



| <span data-ttu-id="06960-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06960-124">Requirement</span></span> | <span data-ttu-id="06960-125">Wert</span><span class="sxs-lookup"><span data-stu-id="06960-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="06960-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06960-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06960-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06960-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="06960-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06960-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06960-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06960-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06960-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06960-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06960-131">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="06960-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="06960-132">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="06960-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





