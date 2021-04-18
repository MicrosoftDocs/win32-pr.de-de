---
title: Komplexer DefinitionType-Typ
description: Definiert eine Liste von Ereignissen, die von Ihrem Anbieter protokolliert werden können.
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- DefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341002"
---
# <a name="definitiontype-complex-type"></a><span data-ttu-id="f1708-104">Komplexer DefinitionType-Typ</span><span class="sxs-lookup"><span data-stu-id="f1708-104">DefinitionType Complex Type</span></span>

<span data-ttu-id="f1708-105">Definiert eine Liste von Ereignissen, die von Ihrem Anbieter protokolliert werden können.</span><span class="sxs-lookup"><span data-stu-id="f1708-105">Defines a list of events that your provider can log.</span></span>

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f1708-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1708-106">Child elements</span></span>



| <span data-ttu-id="f1708-107">Element</span><span class="sxs-lookup"><span data-stu-id="f1708-107">Element</span></span>                                                           | <span data-ttu-id="f1708-108">type</span><span class="sxs-lookup"><span data-stu-id="f1708-108">Type</span></span>                                                                                       | <span data-ttu-id="f1708-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1708-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1708-110">**Veranstalter**</span><span class="sxs-lookup"><span data-stu-id="f1708-110">**event**</span></span>](eventmanifestschema-event-definitiontype-element.md) | [<span data-ttu-id="f1708-111">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="f1708-111">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md)         | <span data-ttu-id="f1708-112">Definiert ein Ereignis, das von Ihrem Anbieter protokolliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1708-112">Defines an event that your provider can log.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f1708-113">**Task**</span><span class="sxs-lookup"><span data-stu-id="f1708-113">**task**</span></span>](eventmanifestschema-task-definitiontype-element.md)   | [<span data-ttu-id="f1708-114">**TaskEventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="f1708-114">**TaskEventDefinitionType**</span></span>](eventmanifestschema-taskeventdefinitiontype-complextype.md) | <span data-ttu-id="f1708-115">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1708-115">Not supported.</span></span><br/> <span data-ttu-id="f1708-116">**Windows Server 2008 und Windows Vista:** Definiert ein Aufgaben spezifisches Ereignis, das von Ihrem Anbieter protokolliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1708-116">**Windows Server 2008 and Windows Vista:** Defines a task-specific event that your provider can log.</span></span> <span data-ttu-id="f1708-117">(Beginnend mit dem Nachrichten Compiler, der mit der Windows 7-Version der Windows SDK ausgeliefert wird, werden aufgabenspezifische Ereignisse nicht mehr unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="f1708-117">(Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, task-specific events are no longer supported.)</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f1708-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1708-118">Requirements</span></span>



| <span data-ttu-id="f1708-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1708-119">Requirement</span></span> | <span data-ttu-id="f1708-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f1708-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1708-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1708-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1708-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1708-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1708-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1708-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1708-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1708-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





