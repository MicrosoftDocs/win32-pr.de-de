---
title: Randomdelay (timetriggertype)-Element
description: Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird. | Randomdelay (timetriggertype)-Element
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Randomdelay-Element Taskplaner
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354324"
---
# <a name="randomdelay-timetriggertype-element"></a><span data-ttu-id="3eb7e-105">Randomdelay (timetriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="3eb7e-105">RandomDelay (timeTriggerType) Element</span></span>

<span data-ttu-id="3eb7e-106">Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="3eb7e-107">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="3eb7e-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="3eb7e-108">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="3eb7e-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="3eb7e-109">Das-Element wird durch den komplexen Typ " [**timetriggertype**](taskschedulerschema-timetriggertype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-109">The element is defined by the [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3eb7e-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3eb7e-110">Parent element</span></span>



| <span data-ttu-id="3eb7e-111">Element</span><span class="sxs-lookup"><span data-stu-id="3eb7e-111">Element</span></span>                                                                                    | <span data-ttu-id="3eb7e-112">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="3eb7e-112">Derived from</span></span>                                                               | <span data-ttu-id="3eb7e-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3eb7e-113">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="3eb7e-114">**Timetrigger (triggergroup)**</span><span class="sxs-lookup"><span data-stu-id="3eb7e-114">**TimeTrigger (triggerGroup)**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md) | [<span data-ttu-id="3eb7e-115">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="3eb7e-115">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md) | <span data-ttu-id="3eb7e-116">Gibt einen-Auslösers an, der einen Task startet, wenn der--ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="3eb7e-116">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3eb7e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3eb7e-117">Remarks</span></span>

<span data-ttu-id="3eb7e-118">Informationen zur C++-Entwicklung finden Sie unter [**randomdelay-Eigenschaft von Itime-**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay)Auslösung.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-118">For C++ development, see [**RandomDelay Property of ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span></span>

<span data-ttu-id="3eb7e-119">Informationen zur Skript Entwicklung finden Sie unter [**timeauslöst. randomdelay**](timetrigger-randomdelay.md).</span><span class="sxs-lookup"><span data-stu-id="3eb7e-119">For script development, see [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3eb7e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3eb7e-120">Requirements</span></span>



| <span data-ttu-id="3eb7e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3eb7e-121">Requirement</span></span> | <span data-ttu-id="3eb7e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3eb7e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3eb7e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3eb7e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3eb7e-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3eb7e-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3eb7e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3eb7e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3eb7e-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3eb7e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





