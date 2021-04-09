---
title: Executiontimelimit (settingstype)-Element
description: Die Zeitspanne, die zum Ausführen der Aufgabe zulässig ist.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Executiontimelimit-Element Taskplaner
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858722"
---
# <a name="executiontimelimit-settingstype-element"></a><span data-ttu-id="6ed35-104">Executiontimelimit (settingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="6ed35-104">ExecutionTimeLimit (settingsType) Element</span></span>

<span data-ttu-id="6ed35-105">Die Zeitspanne, die zum Ausführen der Aufgabe zulässig ist. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="6ed35-105">Amount of time allowed to complete the task.The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="6ed35-106">Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="6ed35-106">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="6ed35-107">Mit dem Wert PT0S kann der Task unbegrenzt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed35-107">A value of PT0S will enable the task to run indefinitely.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

<span data-ttu-id="6ed35-108">Das **executiontimelimit** -Element wird durch den komplexen [**settingstype**](taskschedulerschema-settingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="6ed35-108">The **ExecutionTimeLimit** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6ed35-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="6ed35-109">Parent element</span></span>



| <span data-ttu-id="6ed35-110">Element</span><span class="sxs-lookup"><span data-stu-id="6ed35-110">Element</span></span>                                                           | <span data-ttu-id="6ed35-111">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="6ed35-111">Derived from</span></span>                                                         | <span data-ttu-id="6ed35-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ed35-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ed35-113">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="6ed35-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="6ed35-114">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="6ed35-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="6ed35-115">Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6ed35-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6ed35-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ed35-116">Remarks</span></span>

<span data-ttu-id="6ed35-117">Informationen zur C++-Entwicklung finden Sie unter [**executiontimelimit-Eigenschaft von itasksettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span><span class="sxs-lookup"><span data-stu-id="6ed35-117">For C++ development, see [**ExecutionTimeLimit Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span></span>

<span data-ttu-id="6ed35-118">Informationen zur Skript Entwicklung finden Sie unter [**TaskSettings.Executiontimelimit**](tasksettings-executiontimelimit.md).</span><span class="sxs-lookup"><span data-stu-id="6ed35-118">For script development, see [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ed35-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ed35-119">Requirements</span></span>



| <span data-ttu-id="6ed35-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ed35-120">Requirement</span></span> | <span data-ttu-id="6ed35-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6ed35-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ed35-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ed35-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed35-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ed35-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ed35-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ed35-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed35-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ed35-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ed35-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ed35-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed35-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="6ed35-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





