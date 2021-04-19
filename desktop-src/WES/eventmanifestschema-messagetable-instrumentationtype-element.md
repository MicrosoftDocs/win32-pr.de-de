---
title: messagetable (eventstype)-Element
description: Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests. | messagetable (eventstype)-Element
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- messagetable-Element EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366395"
---
# <a name="messagetable-eventstype-element"></a><span data-ttu-id="79a33-105">messagetable (eventstype)-Element</span><span class="sxs-lookup"><span data-stu-id="79a33-105">messageTable (EventsType) Element</span></span>

<span data-ttu-id="79a33-106">Enthält einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="79a33-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="79a33-107">Das **messagetable** -Element wird durch den komplexen [**eventstype**](eventmanifestschema-eventstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="79a33-107">The **messageTable** element is defined by the [**EventsType**](eventmanifestschema-eventstype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="79a33-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79a33-108">Child elements</span></span>



| <span data-ttu-id="79a33-109">Element</span><span class="sxs-lookup"><span data-stu-id="79a33-109">Element</span></span>                                                             | <span data-ttu-id="79a33-110">type</span><span class="sxs-lookup"><span data-stu-id="79a33-110">Type</span></span> | <span data-ttu-id="79a33-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79a33-111">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79a33-112">**Nachricht**</span><span class="sxs-lookup"><span data-stu-id="79a33-112">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="79a33-113">Gibt einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests an.</span><span class="sxs-lookup"><span data-stu-id="79a33-113">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="79a33-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="79a33-114">Attributes</span></span>



| <span data-ttu-id="79a33-115">Name</span><span class="sxs-lookup"><span data-stu-id="79a33-115">Name</span></span>    | <span data-ttu-id="79a33-116">type</span><span class="sxs-lookup"><span data-stu-id="79a33-116">Type</span></span>   | <span data-ttu-id="79a33-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79a33-117">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a33-118">message</span><span class="sxs-lookup"><span data-stu-id="79a33-118">message</span></span> | <span data-ttu-id="79a33-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79a33-119">string</span></span> | <span data-ttu-id="79a33-120">Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="79a33-120">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="79a33-121">mId</span><span class="sxs-lookup"><span data-stu-id="79a33-121">mid</span></span>     | <span data-ttu-id="79a33-122">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79a33-122">string</span></span> | <span data-ttu-id="79a33-123">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="79a33-123">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="79a33-124">Symbol</span><span class="sxs-lookup"><span data-stu-id="79a33-124">symbol</span></span>  | <span data-ttu-id="79a33-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79a33-125">string</span></span> | <span data-ttu-id="79a33-126">Der symbolische Name, den der Nachrichten Compiler für diese Meldungs Zeichenfolge erstellen soll.</span><span class="sxs-lookup"><span data-stu-id="79a33-126">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="79a33-127">value</span><span class="sxs-lookup"><span data-stu-id="79a33-127">value</span></span>   | <span data-ttu-id="79a33-128">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="79a33-128">string</span></span> | <span data-ttu-id="79a33-129">Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="79a33-129">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="79a33-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79a33-130">Requirements</span></span>



| <span data-ttu-id="79a33-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79a33-131">Requirement</span></span> | <span data-ttu-id="79a33-132">Wert</span><span class="sxs-lookup"><span data-stu-id="79a33-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79a33-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79a33-133">Minimum supported client</span></span><br/> | <span data-ttu-id="79a33-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79a33-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79a33-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79a33-135">Minimum supported server</span></span><br/> | <span data-ttu-id="79a33-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79a33-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79a33-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79a33-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="79a33-138">**Übergeordnete Elemente**</span><span class="sxs-lookup"><span data-stu-id="79a33-138">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="79a33-139">**Events (InstrumentationType)-Element**</span><span class="sxs-lookup"><span data-stu-id="79a33-139">**events (InstrumentationType) Element**</span></span>](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





