---
title: komplexer comhandlertype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das comhandlerelement.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- komplexer comhandlertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040396"
---
# <a name="comhandlertype-complex-type"></a><span data-ttu-id="31fa8-104">komplexer comhandlertype-Typ</span><span class="sxs-lookup"><span data-stu-id="31fa8-104">comHandlerType Complex Type</span></span>

<span data-ttu-id="31fa8-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**comhandlerelement**](taskschedulerschema-comhandler-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="31fa8-105">Defines the child elements and sequencing information for the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="31fa8-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31fa8-106">Child elements</span></span>



| <span data-ttu-id="31fa8-107">Element</span><span class="sxs-lookup"><span data-stu-id="31fa8-107">Element</span></span>                                                               | <span data-ttu-id="31fa8-108">type</span><span class="sxs-lookup"><span data-stu-id="31fa8-108">Type</span></span>                                                         | <span data-ttu-id="31fa8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31fa8-109">Description</span></span>                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="31fa8-110">**ClassID**</span><span class="sxs-lookup"><span data-stu-id="31fa8-110">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="31fa8-111">**guidtype**</span><span class="sxs-lookup"><span data-stu-id="31fa8-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="31fa8-112">Gibt den Bezeichner der Handlerklasse an.</span><span class="sxs-lookup"><span data-stu-id="31fa8-112">Specifies the identifier of the handler class.</span></span><br/>          |
| [<span data-ttu-id="31fa8-113">**Daten**</span><span class="sxs-lookup"><span data-stu-id="31fa8-113">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="31fa8-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="31fa8-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="31fa8-115">Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="31fa8-115">Specifies additional data associated with the handler.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="31fa8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31fa8-116">Requirements</span></span>



| <span data-ttu-id="31fa8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31fa8-117">Requirement</span></span> | <span data-ttu-id="31fa8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="31fa8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31fa8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31fa8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31fa8-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31fa8-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31fa8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31fa8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31fa8-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31fa8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31fa8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31fa8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fa8-124">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="31fa8-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="31fa8-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="31fa8-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





