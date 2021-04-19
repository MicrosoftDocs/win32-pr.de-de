---
title: Komplexer TaskEventDefinitionType-Typ
description: Definiert ein Aufgaben spezifisches Ereignis, das von Ihrem Anbieter protokolliert werden kann. | Komplexer TaskEventDefinitionType-Typ
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106370386"
---
# <a name="taskeventdefinitiontype-complex-type"></a><span data-ttu-id="e915c-105">Komplexer TaskEventDefinitionType-Typ</span><span class="sxs-lookup"><span data-stu-id="e915c-105">TaskEventDefinitionType Complex Type</span></span>

<span data-ttu-id="e915c-106">\[Beginnend mit dem Nachrichten Compiler, der mit der Windows 7-Version der Windows SDK ausgeliefert wird, ist der komplexe Typ TaskEventDefinitionType nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e915c-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, the TaskEventDefinitionType complex type is no longer available.</span></span> <span data-ttu-id="e915c-107">Verwenden Sie stattdessen aufgabenspezifische Opcodes, um die gleiche Funktionalität bereitzustellen.\]</span><span class="sxs-lookup"><span data-stu-id="e915c-107">Instead use task-specific opcodes to provide the same functionality.\]</span></span>

<span data-ttu-id="e915c-108">Definiert ein Aufgaben spezifisches Ereignis, das von Ihrem Anbieter protokolliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e915c-108">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e915c-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e915c-109">Child elements</span></span>



| <span data-ttu-id="e915c-110">Element</span><span class="sxs-lookup"><span data-stu-id="e915c-110">Element</span></span>                                                                      | <span data-ttu-id="e915c-111">type</span><span class="sxs-lookup"><span data-stu-id="e915c-111">Type</span></span>                                                                               | <span data-ttu-id="e915c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e915c-112">Description</span></span>                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e915c-113">**event**</span><span class="sxs-lookup"><span data-stu-id="e915c-113">**event**</span></span>                                                                    | [<span data-ttu-id="e915c-114">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="e915c-114">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="e915c-115">Ein Aufgaben spezifisches Ereignis, das mit einer Aufgabe veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="e915c-115">A task-specific event published with a task.</span></span><br/> |
| [<span data-ttu-id="e915c-116">**OpCode**</span><span class="sxs-lookup"><span data-stu-id="e915c-116">**opcode**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | <span data-ttu-id="e915c-117">Ein Aufgaben spezifischer Opcode für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e915c-117">A task-specific opcode that for an event.</span></span> <br/>   |



## <a name="attributes"></a><span data-ttu-id="e915c-118">Attributes</span><span class="sxs-lookup"><span data-stu-id="e915c-118">Attributes</span></span>



| <span data-ttu-id="e915c-119">Name</span><span class="sxs-lookup"><span data-stu-id="e915c-119">Name</span></span> | <span data-ttu-id="e915c-120">type</span><span class="sxs-lookup"><span data-stu-id="e915c-120">Type</span></span>      | <span data-ttu-id="e915c-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e915c-121">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="e915c-122">name</span><span class="sxs-lookup"><span data-stu-id="e915c-122">name</span></span> | <span data-ttu-id="e915c-123">**QName**</span><span class="sxs-lookup"><span data-stu-id="e915c-123">**QName**</span></span> | <span data-ttu-id="e915c-124">Der Name des aufgabenspezifischen OpCodes.</span><span class="sxs-lookup"><span data-stu-id="e915c-124">The name of the task-specific opcode.</span></span><br/> |
| <span data-ttu-id="e915c-125">name</span><span class="sxs-lookup"><span data-stu-id="e915c-125">name</span></span> | <span data-ttu-id="e915c-126">anyURI</span><span class="sxs-lookup"><span data-stu-id="e915c-126">anyURI</span></span>    | <span data-ttu-id="e915c-127">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="e915c-127">The name of the task.</span></span><br/>                 |



## <a name="requirements"></a><span data-ttu-id="e915c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e915c-128">Requirements</span></span>



| <span data-ttu-id="e915c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e915c-129">Requirement</span></span> | <span data-ttu-id="e915c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e915c-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e915c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e915c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e915c-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e915c-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e915c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e915c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e915c-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e915c-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





