---
title: Data (comhandlertype)-Element
description: Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Datenelement Taskplaner
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956922"
---
# <a name="data-comhandlertype-element"></a><span data-ttu-id="3c1cd-104">Data (comhandlertype)-Element</span><span class="sxs-lookup"><span data-stu-id="3c1cd-104">Data (comHandlerType) Element</span></span>

<span data-ttu-id="3c1cd-105">Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3c1cd-105">Specifies additional data associated with the handler.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="3c1cd-106">Das **Data** -Element wird durch den komplexen [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="3c1cd-106">The **Data** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3c1cd-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="3c1cd-107">Parent element</span></span>



| <span data-ttu-id="3c1cd-108">Element</span><span class="sxs-lookup"><span data-stu-id="3c1cd-108">Element</span></span>                                                                  | <span data-ttu-id="3c1cd-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="3c1cd-109">Derived from</span></span>                                                             | <span data-ttu-id="3c1cd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c1cd-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="3c1cd-111">**Comhandler**</span><span class="sxs-lookup"><span data-stu-id="3c1cd-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="3c1cd-112">**comhandlertype**</span><span class="sxs-lookup"><span data-stu-id="3c1cd-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="3c1cd-113">Gibt eine Aktion an, die einen Handler auslöst.</span><span class="sxs-lookup"><span data-stu-id="3c1cd-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3c1cd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c1cd-114">Remarks</span></span>

<span data-ttu-id="3c1cd-115">Anwendungen definieren die Handlerdaten mithilfe der [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) -Eigenschaft der [**icomhandleraction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3c1cd-115">Applications define the handler data using the [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c1cd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c1cd-116">Requirements</span></span>



| <span data-ttu-id="3c1cd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c1cd-117">Requirement</span></span> | <span data-ttu-id="3c1cd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3c1cd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c1cd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c1cd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c1cd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c1cd-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3c1cd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c1cd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c1cd-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c1cd-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c1cd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c1cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1cd-124">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="3c1cd-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





