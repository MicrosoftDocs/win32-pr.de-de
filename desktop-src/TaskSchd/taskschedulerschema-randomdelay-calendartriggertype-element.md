---
title: Randomdelay (calendartriggertype)-Element
description: Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird. | Randomdelay (calendartriggertype)-Element
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
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
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353379"
---
# <a name="randomdelay-calendartriggertype-element"></a><span data-ttu-id="e4305-105">Randomdelay (calendartriggertype)-Element</span><span class="sxs-lookup"><span data-stu-id="e4305-105">RandomDelay (calendarTriggerType) Element</span></span>

<span data-ttu-id="e4305-106">Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e4305-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="e4305-107">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="e4305-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e4305-108">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="e4305-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="e4305-109">Das **randomdelay** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="e4305-109">The **RandomDelay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e4305-110">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e4305-110">Parent element</span></span>



| <span data-ttu-id="e4305-111">Element</span><span class="sxs-lookup"><span data-stu-id="e4305-111">Element</span></span>                                                                                            | <span data-ttu-id="e4305-112">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="e4305-112">Derived from</span></span>                                                                       | <span data-ttu-id="e4305-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4305-113">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4305-114">**Calendartrigger (triggergroup)**</span><span class="sxs-lookup"><span data-stu-id="e4305-114">**CalendarTrigger (triggerGroup)**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="e4305-115">**calendartriggertype**</span><span class="sxs-lookup"><span data-stu-id="e4305-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="e4305-116">Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.</span><span class="sxs-lookup"><span data-stu-id="e4305-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="e4305-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4305-117">Requirements</span></span>



| <span data-ttu-id="e4305-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4305-118">Requirement</span></span> | <span data-ttu-id="e4305-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e4305-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4305-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4305-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4305-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4305-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4305-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4305-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4305-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4305-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





