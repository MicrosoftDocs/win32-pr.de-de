---
title: komplexer weekstype-Typ
description: Definiert das untergeordnete Element und die Sequenzierungs Informationen für das Week-Element.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- komplexer weekstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105350"
---
# <a name="weekstype-complex-type"></a><span data-ttu-id="4bcbc-104">komplexer weekstype-Typ</span><span class="sxs-lookup"><span data-stu-id="4bcbc-104">weeksType Complex Type</span></span>

<span data-ttu-id="4bcbc-105">Definiert das untergeordnete Element und die Sequenzierungs Informationen für das [**Week**](taskschedulerschema-week-weekstype-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="4bcbc-105">Defines the child element and sequencing information for the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4bcbc-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4bcbc-106">Child elements</span></span>



| <span data-ttu-id="4bcbc-107">Element</span><span class="sxs-lookup"><span data-stu-id="4bcbc-107">Element</span></span>                                                    | <span data-ttu-id="4bcbc-108">type</span><span class="sxs-lookup"><span data-stu-id="4bcbc-108">Type</span></span>                                                        | <span data-ttu-id="4bcbc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bcbc-109">Description</span></span>                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="4bcbc-110">**Mitte**</span><span class="sxs-lookup"><span data-stu-id="4bcbc-110">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="4bcbc-111">**weektype**</span><span class="sxs-lookup"><span data-stu-id="4bcbc-111">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="4bcbc-112">Gibt die Woche an, in der die Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bcbc-112">Specifies the week in which the task is run.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4bcbc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bcbc-113">Requirements</span></span>



| <span data-ttu-id="4bcbc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bcbc-114">Requirement</span></span> | <span data-ttu-id="4bcbc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4bcbc-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4bcbc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bcbc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4bcbc-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bcbc-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4bcbc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bcbc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4bcbc-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bcbc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bcbc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bcbc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcbc-121">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4bcbc-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





