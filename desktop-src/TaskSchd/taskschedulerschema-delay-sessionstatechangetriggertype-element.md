---
title: Delay (sessionstatechangetriggertype)-Element
description: Enthält einen Wert, der die Länge der Verzögerung für einen Task Startzeitpunkt angibt, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Verzögertes Element Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106377"
---
# <a name="delay-sessionstatechangetriggertype-element"></a><span data-ttu-id="37676-104">Delay (sessionstatechangetriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="37676-104">Delay (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="37676-105">Enthält einen Wert, der die Länge der Verzögerung für einen Task Startzeitpunkt angibt, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="37676-105">Contains a value that indicates the delay length for a task start time, when a Terminal Server session state change is detected.</span></span> <span data-ttu-id="37676-106">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="37676-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="37676-107">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="37676-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="37676-108">Das **Delay** -Element wird durch den komplexen Typ [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="37676-108">The **Delay** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="37676-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="37676-109">Parent element</span></span>



| <span data-ttu-id="37676-110">Element</span><span class="sxs-lookup"><span data-stu-id="37676-110">Element</span></span>                       | <span data-ttu-id="37676-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="37676-111">Derived from</span></span>                                                                                           | <span data-ttu-id="37676-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37676-112">Description</span></span>                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37676-113">**Sessionstatechange-Auslösers**</span><span class="sxs-lookup"><span data-stu-id="37676-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="37676-114">**sessionstatechangetriggertype**</span><span class="sxs-lookup"><span data-stu-id="37676-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="37676-115">Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.</span><span class="sxs-lookup"><span data-stu-id="37676-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="37676-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37676-116">Remarks</span></span>

<span data-ttu-id="37676-117">Bei der Skripterstellung wird die Verzögerungs Verzögerung für den Sitzungs Statusänderung mithilfe der [**sessionstatechangeghost. Delay**](sessionstatechangetrigger-delay.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="37676-117">For scripting development, the session state change trigger delay is specified using the [**SessionStateChangeTrigger.Delay**](sessionstatechangetrigger-delay.md) property.</span></span>

<span data-ttu-id="37676-118">Bei der C++-Entwicklung wird die Verzögerungs Verzögerung der Sitzungs Statusänderung mithilfe der [**Delay-Eigenschaft von isessionstatechangelöst**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay)angegeben.</span><span class="sxs-lookup"><span data-stu-id="37676-118">For C++ development, the session state change trigger delay is specified using the [**Delay property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="37676-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37676-119">Requirements</span></span>



| <span data-ttu-id="37676-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37676-120">Requirement</span></span> | <span data-ttu-id="37676-121">Wert</span><span class="sxs-lookup"><span data-stu-id="37676-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37676-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37676-122">Minimum supported client</span></span><br/> | <span data-ttu-id="37676-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37676-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37676-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37676-124">Minimum supported server</span></span><br/> | <span data-ttu-id="37676-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37676-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





