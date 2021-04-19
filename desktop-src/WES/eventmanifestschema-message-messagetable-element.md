---
title: Message (messagetable)-Element
description: Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests. | Message (messagetable)-Element
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- Message-Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363072"
---
# <a name="message-messagetable-element"></a><span data-ttu-id="af274-105">Message (messagetable)-Element</span><span class="sxs-lookup"><span data-stu-id="af274-105">message (messageTable) Element</span></span>

<span data-ttu-id="af274-106">Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="af274-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="af274-107">Das **Message** -Element wird durch das [**messagetable**](eventmanifestschema-messagetable-instrumentationtype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="af274-107">The **message** element is defined by the [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="af274-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="af274-108">Attributes</span></span>



| <span data-ttu-id="af274-109">Name</span><span class="sxs-lookup"><span data-stu-id="af274-109">Name</span></span>    | <span data-ttu-id="af274-110">type</span><span class="sxs-lookup"><span data-stu-id="af274-110">Type</span></span>   | <span data-ttu-id="af274-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af274-111">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af274-112">message</span><span class="sxs-lookup"><span data-stu-id="af274-112">message</span></span> | <span data-ttu-id="af274-113">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="af274-113">string</span></span> | <span data-ttu-id="af274-114">Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="af274-114">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="af274-115">mId</span><span class="sxs-lookup"><span data-stu-id="af274-115">mid</span></span>     | <span data-ttu-id="af274-116">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="af274-116">string</span></span> | <span data-ttu-id="af274-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af274-117">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="af274-118">Symbol</span><span class="sxs-lookup"><span data-stu-id="af274-118">symbol</span></span>  | <span data-ttu-id="af274-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="af274-119">string</span></span> | <span data-ttu-id="af274-120">Der symbolische Name, den der Nachrichten Compiler für diese Meldungs Zeichenfolge erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="af274-120">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="af274-121">value</span><span class="sxs-lookup"><span data-stu-id="af274-121">value</span></span>   | <span data-ttu-id="af274-122">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="af274-122">string</span></span> | <span data-ttu-id="af274-123">Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="af274-123">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="af274-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af274-124">Requirements</span></span>



| <span data-ttu-id="af274-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af274-125">Requirement</span></span> | <span data-ttu-id="af274-126">Wert</span><span class="sxs-lookup"><span data-stu-id="af274-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af274-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af274-127">Minimum supported client</span></span><br/> | <span data-ttu-id="af274-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af274-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af274-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af274-129">Minimum supported server</span></span><br/> | <span data-ttu-id="af274-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af274-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af274-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af274-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="af274-132">**Übergeordnete Elemente**</span><span class="sxs-lookup"><span data-stu-id="af274-132">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="af274-133">**messagetable (eventstype)**</span><span class="sxs-lookup"><span data-stu-id="af274-133">**messageTable (EventsType)**</span></span>](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[<span data-ttu-id="af274-134">**messagetable (metadataType)**</span><span class="sxs-lookup"><span data-stu-id="af274-134">**messageTable (MetadataType)**</span></span>](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





