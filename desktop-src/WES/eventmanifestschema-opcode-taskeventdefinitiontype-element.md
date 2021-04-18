---
title: Opcode (TaskEventDefinitionType)-Element
description: Enthält einen aufgabenspezifischen Opcode für ein Ereignis. Für den Task, der die Ereignis Definitionen enthält, wird davon ausgegangen, dass alle Opcode-Definitionen aufgabenspezifisch sind.
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- Opcode-Element EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341031"
---
# <a name="opcode-taskeventdefinitiontype-element"></a><span data-ttu-id="0f364-105">Opcode (TaskEventDefinitionType)-Element</span><span class="sxs-lookup"><span data-stu-id="0f364-105">opcode (TaskEventDefinitionType) Element</span></span>

<span data-ttu-id="0f364-106">\[Beginnend mit dem Nachrichten Compiler, der mit der Windows 7-Version des Windows SDK ausgeliefert wird, ist dieses Element nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0f364-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="0f364-107">Enthält einen aufgabenspezifischen Opcode für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0f364-107">Contains a task-specific opcode for an event.</span></span> <span data-ttu-id="0f364-108">Für den Task, der die Ereignis Definitionen enthält, wird davon ausgegangen, dass alle Opcode-Definitionen aufgabenspezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="0f364-108">All of the opcode definitions are assumed to be task-specific for the task that contains the event definitions.</span></span>

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0f364-109">Das **Opcode** -Element wird durch den komplexen [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="0f364-109">The **opcode** element is defined by the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0f364-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0f364-110">Child elements</span></span>



| <span data-ttu-id="0f364-111">Element</span><span class="sxs-lookup"><span data-stu-id="0f364-111">Element</span></span>                                                   | <span data-ttu-id="0f364-112">type</span><span class="sxs-lookup"><span data-stu-id="0f364-112">Type</span></span>                                                                               | <span data-ttu-id="0f364-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f364-113">Description</span></span>                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0f364-114">**Veranstalter**</span><span class="sxs-lookup"><span data-stu-id="0f364-114">**event**</span></span>](eventmanifestschema-event-opcode-element.md) | [<span data-ttu-id="0f364-115">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="0f364-115">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="0f364-116">Ein Ereignis, das mit einer Aufgabe veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="0f364-116">An event that is published with a task.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0f364-117">Attributes</span><span class="sxs-lookup"><span data-stu-id="0f364-117">Attributes</span></span>



| <span data-ttu-id="0f364-118">Name</span><span class="sxs-lookup"><span data-stu-id="0f364-118">Name</span></span> | <span data-ttu-id="0f364-119">type</span><span class="sxs-lookup"><span data-stu-id="0f364-119">Type</span></span>      | <span data-ttu-id="0f364-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f364-120">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="0f364-121">name</span><span class="sxs-lookup"><span data-stu-id="0f364-121">name</span></span> | <span data-ttu-id="0f364-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="0f364-122">**QName**</span></span> | <span data-ttu-id="0f364-123">Der Name des aufgabenspezifischen OpCodes.</span><span class="sxs-lookup"><span data-stu-id="0f364-123">The name of the task-specific opcode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0f364-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f364-124">Requirements</span></span>



| <span data-ttu-id="0f364-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f364-125">Requirement</span></span> | <span data-ttu-id="0f364-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0f364-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f364-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f364-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0f364-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f364-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f364-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f364-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0f364-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f364-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f364-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f364-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f364-132">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="0f364-132">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="0f364-133">**Aufgabe (DefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="0f364-133">**task (DefinitionType)**</span></span>](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





