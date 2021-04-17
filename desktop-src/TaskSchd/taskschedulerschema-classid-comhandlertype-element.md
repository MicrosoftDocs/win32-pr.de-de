---
title: ClassID-Element (comhandlertype)
description: Gibt den Bezeichner der Handlerklasse an.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- ClassID-Element Taskplaner
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479239"
---
# <a name="classid-comhandlertype-element"></a><span data-ttu-id="4b650-104">ClassID-Element (comhandlertype)</span><span class="sxs-lookup"><span data-stu-id="4b650-104">ClassId (comHandlerType) Element</span></span>

<span data-ttu-id="4b650-105">Gibt den Bezeichner der Handlerklasse an.</span><span class="sxs-lookup"><span data-stu-id="4b650-105">Specifies the identifier of the handler class.</span></span>

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

<span data-ttu-id="4b650-106">Das **ClassID-** Element wird durch den komplexen [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="4b650-106">The **ClassId** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4b650-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="4b650-107">Parent element</span></span>



| <span data-ttu-id="4b650-108">Element</span><span class="sxs-lookup"><span data-stu-id="4b650-108">Element</span></span>                                                                  | <span data-ttu-id="4b650-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="4b650-109">Derived from</span></span>                                                             | <span data-ttu-id="4b650-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b650-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="4b650-111">**Comhandler**</span><span class="sxs-lookup"><span data-stu-id="4b650-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="4b650-112">**comhandlertype**</span><span class="sxs-lookup"><span data-stu-id="4b650-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="4b650-113">Gibt eine Aktion an, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="4b650-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4b650-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b650-114">Remarks</span></span>

<span data-ttu-id="4b650-115">Anwendungen definieren den Klassen Bezeichner mithilfe der [**ClassID-**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) Eigenschaft der [**icomhandleraction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4b650-115">Applications define the class identifier using the [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b650-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b650-116">Requirements</span></span>



| <span data-ttu-id="4b650-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b650-117">Requirement</span></span> | <span data-ttu-id="4b650-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4b650-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b650-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b650-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4b650-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b650-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b650-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b650-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4b650-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b650-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b650-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b650-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b650-124">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="4b650-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





