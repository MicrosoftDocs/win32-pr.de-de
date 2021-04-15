---
title: Komplexer renderinginfotype-Typ
description: Definiert die gerenderten Nachrichten für das Ereignis.
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- Renderinginfotype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478792"
---
# <a name="renderinginfotype-complex-type"></a><span data-ttu-id="0c32c-104">Komplexer renderinginfotype-Typ</span><span class="sxs-lookup"><span data-stu-id="0c32c-104">RenderingInfoType Complex Type</span></span>

<span data-ttu-id="0c32c-105">Definiert die gerenderten Nachrichten für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0c32c-105">Defines the rendered messages for the event.</span></span>

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0c32c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c32c-106">Child elements</span></span>



| <span data-ttu-id="0c32c-107">Element</span><span class="sxs-lookup"><span data-stu-id="0c32c-107">Element</span></span>                                                             | <span data-ttu-id="0c32c-108">type</span><span class="sxs-lookup"><span data-stu-id="0c32c-108">Type</span></span>   | <span data-ttu-id="0c32c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c32c-109">Description</span></span>                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="0c32c-110">**Channel**</span><span class="sxs-lookup"><span data-stu-id="0c32c-110">**Channel**</span></span>](eventschema-task-renderingtype-element.md)           | <span data-ttu-id="0c32c-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c32c-111">string</span></span> | <span data-ttu-id="0c32c-112">Die gerenderte Meldungs Zeichenfolge des Kanals, der im Ereignis angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0c32c-112">The rendered message string of the channel specified in the event.</span></span><br/> |
| [<span data-ttu-id="0c32c-113">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="0c32c-113">**Keyword**</span></span>](eventschema-keyword-keywords-element.md)             | <span data-ttu-id="0c32c-114">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c32c-114">string</span></span> | <span data-ttu-id="0c32c-115">Die gerenderte Meldungs Zeichenfolge eines im Ereignis angegebenen Schlüssel Worts.</span><span class="sxs-lookup"><span data-stu-id="0c32c-115">The rendered message string of a keyword specified in the event.</span></span><br/>   |
| [<span data-ttu-id="0c32c-116">**Keywords**</span><span class="sxs-lookup"><span data-stu-id="0c32c-116">**Keywords**</span></span>](eventschema-keywords-renderingtype-element.md)      |        | <span data-ttu-id="0c32c-117">Eine Liste von gerenderten Schlüsselwörtern.</span><span class="sxs-lookup"><span data-stu-id="0c32c-117">A list of rendered keywords.</span></span><br/>                                       |
| [<span data-ttu-id="0c32c-118">**Geringen**</span><span class="sxs-lookup"><span data-stu-id="0c32c-118">**Level**</span></span>](eventschema-level-renderingtype-element.md)            | <span data-ttu-id="0c32c-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c32c-119">string</span></span> | <span data-ttu-id="0c32c-120">Die gerenderte Meldungs Zeichenfolge der im Ereignis angegebenen Ebene.</span><span class="sxs-lookup"><span data-stu-id="0c32c-120">The rendered message string of the level specified in the event.</span></span><br/>   |
| [<span data-ttu-id="0c32c-121">**`Message`**</span><span class="sxs-lookup"><span data-stu-id="0c32c-121">**Message**</span></span>](eventschema-message-renderingtype-element.md)        | <span data-ttu-id="0c32c-122">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c32c-122">string</span></span> | <span data-ttu-id="0c32c-123">Die gerenderte Meldungs Zeichenfolge des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="0c32c-123">The rendered message string of the event.</span></span><br/>                          |
| [<span data-ttu-id="0c32c-124">**Opcode**</span><span class="sxs-lookup"><span data-stu-id="0c32c-124">**Opcode**</span></span>](eventschema-opcode-renderingtype-element.md)          | <span data-ttu-id="0c32c-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c32c-125">string</span></span> | <span data-ttu-id="0c32c-126">Die gerenderte Meldungs Zeichenfolge des im Ereignis angegebenen OpCodes.</span><span class="sxs-lookup"><span data-stu-id="0c32c-126">The rendered message string of the opcode specified in the event.</span></span><br/>  |
| [<span data-ttu-id="0c32c-127">**Anbieter**</span><span class="sxs-lookup"><span data-stu-id="0c32c-127">**Provider**</span></span>](eventschema-publisher-renderinginfotype-element.md) | <span data-ttu-id="0c32c-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c32c-128">string</span></span> | <span data-ttu-id="0c32c-129">Die gerenderte Nachrichten Zeichenfolge für den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="0c32c-129">The rendered message string for the provider.</span></span><br/>                      |
| [<span data-ttu-id="0c32c-130">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="0c32c-130">**Task**</span></span>](eventschema-task-renderingtype-element.md)              | <span data-ttu-id="0c32c-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c32c-131">string</span></span> | <span data-ttu-id="0c32c-132">Die gerenderte Meldungs Zeichenfolge der im Ereignis angegebenen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="0c32c-132">The rendered message string of the task specified in the event.</span></span><br/>    |



## <a name="attributes"></a><span data-ttu-id="0c32c-133">Attributes</span><span class="sxs-lookup"><span data-stu-id="0c32c-133">Attributes</span></span>



| <span data-ttu-id="0c32c-134">Name</span><span class="sxs-lookup"><span data-stu-id="0c32c-134">Name</span></span>    | <span data-ttu-id="0c32c-135">type</span><span class="sxs-lookup"><span data-stu-id="0c32c-135">Type</span></span>     | <span data-ttu-id="0c32c-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c32c-136">Description</span></span>                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c32c-137">Kultur</span><span class="sxs-lookup"><span data-stu-id="0c32c-137">Culture</span></span> | <span data-ttu-id="0c32c-138">language</span><span class="sxs-lookup"><span data-stu-id="0c32c-138">language</span></span> | <span data-ttu-id="0c32c-139">Der Sprachen Name (z. b. en-US), der das Gebiets Schema identifiziert, das zum Rendering der Nachrichten Zeichenfolgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c32c-139">The language name (for example, en-US) that identifies the locale used to render the message strings.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0c32c-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c32c-140">Remarks</span></span>

<span data-ttu-id="0c32c-141">Dieser Abschnitt enthält nur Ereignisse, die mit dem [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector) Sammlungs Dienst erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="0c32c-141">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c32c-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c32c-142">Requirements</span></span>



| <span data-ttu-id="0c32c-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c32c-143">Requirement</span></span> | <span data-ttu-id="0c32c-144">Wert</span><span class="sxs-lookup"><span data-stu-id="0c32c-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c32c-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c32c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0c32c-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c32c-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c32c-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c32c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0c32c-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c32c-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

