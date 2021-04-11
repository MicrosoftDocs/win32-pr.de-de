---
title: Comhandler-Element (Aktionsgruppe)
description: Gibt eine Aktion an, die einen Handler auslöst.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Comhandler-Element Taskplaner
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956923"
---
# <a name="comhandler-actiongroup-element"></a><span data-ttu-id="f9ad4-104">Comhandler-Element (Aktionsgruppe)</span><span class="sxs-lookup"><span data-stu-id="f9ad4-104">ComHandler (actionGroup) Element</span></span>

<span data-ttu-id="f9ad4-105">Gibt eine Aktion an, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-105">Specifies an action that fires a handler.</span></span>

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

<span data-ttu-id="f9ad4-106">Das **comhandler** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-106">The **ComHandler** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f9ad4-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f9ad4-107">Parent element</span></span>



| <span data-ttu-id="f9ad4-108">Element</span><span class="sxs-lookup"><span data-stu-id="f9ad4-108">Element</span></span>                                                         | <span data-ttu-id="f9ad4-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f9ad4-109">Derived from</span></span>                                                       | <span data-ttu-id="f9ad4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9ad4-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f9ad4-111">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="f9ad4-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="f9ad4-112">**Aktions sType**</span><span class="sxs-lookup"><span data-stu-id="f9ad4-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="f9ad4-113">Enthält die Aktionen, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f9ad4-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9ad4-114">Child elements</span></span>



| <span data-ttu-id="f9ad4-115">Element</span><span class="sxs-lookup"><span data-stu-id="f9ad4-115">Element</span></span>                                                               | <span data-ttu-id="f9ad4-116">type</span><span class="sxs-lookup"><span data-stu-id="f9ad4-116">Type</span></span>                                                         | <span data-ttu-id="f9ad4-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9ad4-117">Description</span></span>                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="f9ad4-118">**ClassID**</span><span class="sxs-lookup"><span data-stu-id="f9ad4-118">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="f9ad4-119">**guidtype**</span><span class="sxs-lookup"><span data-stu-id="f9ad4-119">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="f9ad4-120">Gibt den Bezeichner der Handlerklasse an.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-120">Specifies the identifier of the handler class.</span></span><br/>         |
| [<span data-ttu-id="f9ad4-121">**Daten**</span><span class="sxs-lookup"><span data-stu-id="f9ad4-121">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="f9ad4-122">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f9ad4-122">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="f9ad4-123">Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-123">Specifies additional data associated with the handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9ad4-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9ad4-124">Remarks</span></span>

<span data-ttu-id="f9ad4-125">Anwendungen definieren eine com- [**handleraktion mithilfe der icomhandleraction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-125">Applications define a COM handler action using the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

### <a name="attributes"></a><span data-ttu-id="f9ad4-126">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9ad4-126">Attributes</span></span>

<span data-ttu-id="f9ad4-127">Das folgende Attribut wird vom komplexen Typ " [**aktionbasetype**](taskschedulerschema-actionbasetype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-127">The following attribute is defined by the [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) complex type.</span></span>

-   <span data-ttu-id="f9ad4-128">ID: Bezeichner der von der Aufgabe ausgeführten Aktion.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-128">ID: Identifier of the action performed by the task.</span></span>

## <a name="examples"></a><span data-ttu-id="f9ad4-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9ad4-129">Examples</span></span>

<span data-ttu-id="f9ad4-130">Der folgende XML-Code definiert eine com-handleraktion.</span><span class="sxs-lookup"><span data-stu-id="f9ad4-130">The following XML defines a COM handler action.</span></span>


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a><span data-ttu-id="f9ad4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9ad4-131">Requirements</span></span>



| <span data-ttu-id="f9ad4-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9ad4-132">Requirement</span></span> | <span data-ttu-id="f9ad4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f9ad4-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9ad4-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9ad4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ad4-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9ad4-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9ad4-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9ad4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ad4-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9ad4-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9ad4-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9ad4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ad4-139">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="f9ad4-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





