---
title: komplexer triggerstype-Typ
description: Definiert die Gruppe (triggergroup) für alle Triggerelemente.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- komplexer triggerstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344721"
---
# <a name="triggerstype-complex-type"></a><span data-ttu-id="8df53-104">komplexer triggerstype-Typ</span><span class="sxs-lookup"><span data-stu-id="8df53-104">triggersType Complex Type</span></span>

<span data-ttu-id="8df53-105">Definiert die Gruppe ([**triggergroup) für alle Triggerelemente**](taskschedulerschema-triggergroup-group.md).</span><span class="sxs-lookup"><span data-stu-id="8df53-105">Defines the group ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) for all trigger elements.</span></span> <span data-ttu-id="8df53-106">Die Gruppe [**triggergroup**](taskschedulerschema-triggergroup-group.md) enthält die Liste der Trigger, die in einer Aufgabe verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8df53-106">The [**triggerGroup**](taskschedulerschema-triggergroup-group.md) group contains the list of triggers that can be used in a task.</span></span>

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="8df53-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df53-107">Requirements</span></span>



| <span data-ttu-id="8df53-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8df53-108">Requirement</span></span> | <span data-ttu-id="8df53-109">Wert</span><span class="sxs-lookup"><span data-stu-id="8df53-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8df53-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8df53-110">Minimum supported client</span></span><br/> | <span data-ttu-id="8df53-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8df53-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8df53-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8df53-112">Minimum supported server</span></span><br/> | <span data-ttu-id="8df53-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8df53-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8df53-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8df53-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df53-115">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="8df53-115">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





