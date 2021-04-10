---
title: einfacher multipleinstancespolicytype-Typ
description: Definiert die instanzrichtlinienkonstanten für das multipleinstancespolicy (settingstype)-Element.
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- multipleinstancespolicytype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956683"
---
# <a name="multipleinstancespolicytype-simple-type"></a><span data-ttu-id="23c5f-104">einfacher multipleinstancespolicytype-Typ</span><span class="sxs-lookup"><span data-stu-id="23c5f-104">multipleInstancesPolicyType Simple Type</span></span>

<span data-ttu-id="23c5f-105">Definiert die instanzrichtlinienkonstanten für das [**multipleinstancespolicy (settingstype)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="23c5f-105">Defines the instance policy constants for the [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="23c5f-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="23c5f-106">Enumeration values</span></span>

<span data-ttu-id="23c5f-107">Der einfache Typ " **multipleinstancespolicytype** " definiert die folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="23c5f-107">The **multipleInstancesPolicyType** simple type defines the following values.</span></span>



| <span data-ttu-id="23c5f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="23c5f-108">Value</span></span>        | <span data-ttu-id="23c5f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23c5f-109">Description</span></span>                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c5f-110">Parallel</span><span class="sxs-lookup"><span data-stu-id="23c5f-110">Parallel</span></span>     | <span data-ttu-id="23c5f-111">Startet eine neue Instanz, während eine vorhandene-Instanz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23c5f-111">Starts new instance while an existing instance is running.</span></span><br/>                           |
| <span data-ttu-id="23c5f-112">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="23c5f-112">Queue</span></span>        | <span data-ttu-id="23c5f-113">Startet eine neue Instanz der Aufgabe, nachdem alle anderen Instanzen der Aufgabe vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="23c5f-113">Starts new instance of task after all other instances of the task are complete.</span></span><br/>      |
| <span data-ttu-id="23c5f-114">Ignorumew</span><span class="sxs-lookup"><span data-stu-id="23c5f-114">IgnoreNew</span></span>    | <span data-ttu-id="23c5f-115">Standard.</span><span class="sxs-lookup"><span data-stu-id="23c5f-115">Default.</span></span> <span data-ttu-id="23c5f-116">Startet keine neue Instanz, wenn eine vorhandene Instanz der Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23c5f-116">Does not start new instance if an existing instance of the task is running.</span></span><br/> |
| <span data-ttu-id="23c5f-117">Stopp vorhanden</span><span class="sxs-lookup"><span data-stu-id="23c5f-117">StopExisting</span></span> | <span data-ttu-id="23c5f-118">Beendet eine vorhandene Instanz der Aufgabe vor dem Starten der neuen Instanz.</span><span class="sxs-lookup"><span data-stu-id="23c5f-118">Stops an existing instance of the task before it starts new instance.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="23c5f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23c5f-119">Requirements</span></span>



| <span data-ttu-id="23c5f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23c5f-120">Requirement</span></span> | <span data-ttu-id="23c5f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="23c5f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23c5f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23c5f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23c5f-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23c5f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23c5f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23c5f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23c5f-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23c5f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23c5f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23c5f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23c5f-127">Einfache Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="23c5f-127">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="23c5f-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="23c5f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





