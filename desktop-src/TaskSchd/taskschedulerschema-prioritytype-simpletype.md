---
title: einfacher prioritytype-Typ
description: Definiert die minimalen und maximalen Werte für das Priority-Element (settingstype).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- einfacher prioritytype-Typ Taskplaner
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040851"
---
# <a name="prioritytype-simple-type"></a><span data-ttu-id="3e6d3-104">einfacher prioritytype-Typ</span><span class="sxs-lookup"><span data-stu-id="3e6d3-104">priorityType Simple Type</span></span>

<span data-ttu-id="3e6d3-105">Definiert die minimalen und maximalen Werte für das [**Priority-Element (settingstype)**](taskschedulerschema-priority-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3e6d3-105">Defines the minimum and maximum values for the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="3e6d3-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="3e6d3-106">Enumeration values</span></span>

<span data-ttu-id="3e6d3-107">Der einfache **prioritytype** -Typ definiert die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="3e6d3-107">The **priorityType** simple type defines the following values.</span></span>



| <span data-ttu-id="3e6d3-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3e6d3-108">Value</span></span> | <span data-ttu-id="3e6d3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e6d3-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="3e6d3-110">0</span><span class="sxs-lookup"><span data-stu-id="3e6d3-110">0</span></span>     | <span data-ttu-id="3e6d3-111">Minimale Ganzzahl zulässig.</span><span class="sxs-lookup"><span data-stu-id="3e6d3-111">Minimum integer allowed.</span></span><br/> |
| <span data-ttu-id="3e6d3-112">10</span><span class="sxs-lookup"><span data-stu-id="3e6d3-112">10</span></span>    | <span data-ttu-id="3e6d3-113">Maximale Ganzzahl zulässig.</span><span class="sxs-lookup"><span data-stu-id="3e6d3-113">Maximum integer allowed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3e6d3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e6d3-114">Requirements</span></span>



| <span data-ttu-id="3e6d3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e6d3-115">Requirement</span></span> | <span data-ttu-id="3e6d3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3e6d3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3e6d3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e6d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e6d3-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e6d3-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3e6d3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e6d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e6d3-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e6d3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e6d3-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e6d3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e6d3-122">Einfache Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="3e6d3-122">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3e6d3-123">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="3e6d3-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





