---
title: messagetable (metadataType)-Element
description: Enthält Verweise auf Zeichen folgen, die im Abschnitt mit den Metadaten des Ereignis Instrumentations Manifests verwendet werden. Die Zeichen folgen werden in einer Gruppe von Nachrichten Elementen und IDs zusammengefasst.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103082"
---
# <a name="messagetable-metadatatype-element"></a><span data-ttu-id="441c1-105">messagetable (metadataType)-Element</span><span class="sxs-lookup"><span data-stu-id="441c1-105">messageTable (MetadataType) Element</span></span>

<span data-ttu-id="441c1-106">Enthält Verweise auf Zeichen folgen, die im Abschnitt mit den Metadaten des Ereignis Instrumentations Manifests verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="441c1-106">Contains references to strings that are used in the event instrumentation manifest metadata section.</span></span> <span data-ttu-id="441c1-107">Die Zeichen folgen werden in einer Gruppe von [**Nachrichten**](eventmanifestschema-message-messagetable-element.md) Elementen und IDs zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="441c1-107">The strings are stored in a group of [**message**](eventmanifestschema-message-messagetable-element.md) elements and IDs paired together.</span></span>

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

<span data-ttu-id="441c1-108">Das **messagetable** -Element wird durch den komplexen [**metadataType**](eventmanifestschema-metadatatype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="441c1-108">The **messageTable** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="441c1-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="441c1-109">Child elements</span></span>



| <span data-ttu-id="441c1-110">Element</span><span class="sxs-lookup"><span data-stu-id="441c1-110">Element</span></span>                                                             | <span data-ttu-id="441c1-111">type</span><span class="sxs-lookup"><span data-stu-id="441c1-111">Type</span></span> | <span data-ttu-id="441c1-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="441c1-112">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="441c1-113">**Nachricht**</span><span class="sxs-lookup"><span data-stu-id="441c1-113">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="441c1-114">Gibt einen Verweis auf eine Zeichenfolge im Lokalisierungs Abschnitt des Manifests an.</span><span class="sxs-lookup"><span data-stu-id="441c1-114">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="441c1-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="441c1-115">Attributes</span></span>



| <span data-ttu-id="441c1-116">Name</span><span class="sxs-lookup"><span data-stu-id="441c1-116">Name</span></span>    | <span data-ttu-id="441c1-117">type</span><span class="sxs-lookup"><span data-stu-id="441c1-117">Type</span></span>   | <span data-ttu-id="441c1-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="441c1-118">Description</span></span>                                                              |
|---------|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="441c1-119">message</span><span class="sxs-lookup"><span data-stu-id="441c1-119">message</span></span> | <span data-ttu-id="441c1-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="441c1-120">string</span></span> | <span data-ttu-id="441c1-121">Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="441c1-121">A reference to the localized string in the string table.</span></span><br/>      |
| <span data-ttu-id="441c1-122">mId</span><span class="sxs-lookup"><span data-stu-id="441c1-122">mid</span></span>     | <span data-ttu-id="441c1-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="441c1-123">string</span></span> | <span data-ttu-id="441c1-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="441c1-124">Not used.</span></span><br/>                                                     |
| <span data-ttu-id="441c1-125">Symbol</span><span class="sxs-lookup"><span data-stu-id="441c1-125">symbol</span></span>  | <span data-ttu-id="441c1-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="441c1-126">string</span></span> | <span data-ttu-id="441c1-127">Das Symbol, mit dem auf die Meldung verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="441c1-127">The symbol used to reference the message.</span></span><br/>                     |
| <span data-ttu-id="441c1-128">value</span><span class="sxs-lookup"><span data-stu-id="441c1-128">value</span></span>   | <span data-ttu-id="441c1-129">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="441c1-129">string</span></span> | <span data-ttu-id="441c1-130">Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="441c1-130">The number to use as the message identifier for this message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="441c1-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="441c1-131">Requirements</span></span>



| <span data-ttu-id="441c1-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="441c1-132">Requirement</span></span> | <span data-ttu-id="441c1-133">Wert</span><span class="sxs-lookup"><span data-stu-id="441c1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="441c1-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="441c1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="441c1-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="441c1-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="441c1-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="441c1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="441c1-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="441c1-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="441c1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="441c1-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="441c1-139">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="441c1-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="441c1-140">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="441c1-140">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

<span data-ttu-id="441c1-141">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="441c1-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="441c1-142">**Metadaten (instrumentationmanifest)**</span><span class="sxs-lookup"><span data-stu-id="441c1-142">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





