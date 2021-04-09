---
title: Stoponidleend (idlesettingstype)-Element
description: Gibt an, dass der Taskplaner den Task beendet, wenn die Leerlauf Bedingung vor dem Abschluss der Aufgabe endet.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Stoponidleend-Element Taskplaner
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957069"
---
# <a name="stoponidleend-idlesettingstype-element"></a><span data-ttu-id="7cc61-104">Stoponidleend (idlesettingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="7cc61-104">StopOnIdleEnd (idleSettingsType) Element</span></span>

<span data-ttu-id="7cc61-105">Gibt an, dass der Taskplaner den Task beendet, wenn die Leerlauf Bedingung vor dem Abschluss der Aufgabe endet.</span><span class="sxs-lookup"><span data-stu-id="7cc61-105">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span>

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="7cc61-106">Das **stoponidleend** -Element wird durch den komplexen [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="7cc61-106">The **StopOnIdleEnd** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7cc61-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="7cc61-107">Parent element</span></span>



| <span data-ttu-id="7cc61-108">Element</span><span class="sxs-lookup"><span data-stu-id="7cc61-108">Element</span></span>                                                                       | <span data-ttu-id="7cc61-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="7cc61-109">Derived from</span></span>                                                                 | <span data-ttu-id="7cc61-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7cc61-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cc61-111">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="7cc61-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="7cc61-112">**idlesettingstype**</span><span class="sxs-lookup"><span data-stu-id="7cc61-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="7cc61-113">Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="7cc61-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7cc61-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cc61-114">Remarks</span></span>

<span data-ttu-id="7cc61-115">Informationen zur C++-Entwicklung finden Sie unter [**stoponidleend-Eigenschaft von iidlesettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span><span class="sxs-lookup"><span data-stu-id="7cc61-115">For C++ development, see [**StopOnIdleEnd Property of IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span></span>

<span data-ttu-id="7cc61-116">Informationen zur Skript Entwicklung finden Sie unter [**idlesettings. stoponidleend**](idlesettings-stoponidleend.md).</span><span class="sxs-lookup"><span data-stu-id="7cc61-116">For script development, see [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7cc61-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cc61-117">Examples</span></span>

<span data-ttu-id="7cc61-118">Der folgende XML-Code definiert eine Leerlauf Einstellung, die angibt, dass die Aufgabe nicht ausgeführt werden soll, wenn die Leerlauf Bedingung endet.</span><span class="sxs-lookup"><span data-stu-id="7cc61-118">The following XML defines an idle setting that indicates the task should not be performed when the idle condition ends.</span></span>


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="7cc61-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cc61-119">Requirements</span></span>



| <span data-ttu-id="7cc61-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cc61-120">Requirement</span></span> | <span data-ttu-id="7cc61-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7cc61-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7cc61-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cc61-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc61-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cc61-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7cc61-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cc61-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc61-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cc61-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cc61-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cc61-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc61-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="7cc61-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





