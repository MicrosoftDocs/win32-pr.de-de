---
title: Resources (localizationtype)-Element
description: Definiert eine Gruppe von Zeichen folgen Tabellen, die die lokalisierten Zeichen folgen enthalten, auf die im Manifest verwiesen wird.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- Ressourcen Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341580"
---
# <a name="resources-localizationtype-element"></a><span data-ttu-id="32259-104">Resources (localizationtype)-Element</span><span class="sxs-lookup"><span data-stu-id="32259-104">resources (LocalizationType) Element</span></span>

<span data-ttu-id="32259-105">Definiert eine Gruppe von Zeichen folgen Tabellen, die die lokalisierten Zeichen folgen enthalten, auf die im Manifest verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="32259-105">Defines a group of string tables that contain the localized strings that you reference in your manifest.</span></span>

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="32259-106">Das **Resources** -Element wird durch den komplexen Typ [**localizationtype**](eventmanifestschema-localizationtype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="32259-106">The **resources** element is defined by the [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="32259-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32259-107">Child elements</span></span>



| <span data-ttu-id="32259-108">Element</span><span class="sxs-lookup"><span data-stu-id="32259-108">Element</span></span>                                                                  | <span data-ttu-id="32259-109">type</span><span class="sxs-lookup"><span data-stu-id="32259-109">Type</span></span>                                                                       | <span data-ttu-id="32259-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32259-110">Description</span></span>                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="32259-111">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="32259-111">**stringTable**</span></span>](eventmanifestschema-stringtable-resources-element.md) | [<span data-ttu-id="32259-112">**Stringtabletype**</span><span class="sxs-lookup"><span data-stu-id="32259-112">**StringTableType**</span></span>](eventmanifestschema-stringtabletype-complextype.md) | <span data-ttu-id="32259-113">Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können.</span><span class="sxs-lookup"><span data-stu-id="32259-113">Defines a list of localized strings that you can reference in your manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="32259-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="32259-114">Attributes</span></span>



| <span data-ttu-id="32259-115">Name</span><span class="sxs-lookup"><span data-stu-id="32259-115">Name</span></span>    | <span data-ttu-id="32259-116">type</span><span class="sxs-lookup"><span data-stu-id="32259-116">Type</span></span>   | <span data-ttu-id="32259-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32259-117">Description</span></span>                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32259-118">culture</span><span class="sxs-lookup"><span data-stu-id="32259-118">culture</span></span> | <span data-ttu-id="32259-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="32259-119">string</span></span> | <span data-ttu-id="32259-120">Ein Sprachen Name, der die Kultur der lokalisierten Zeichen folgen in der Zeichen folgen Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="32259-120">A language name that identifies the culture of the localized strings in the string table.</span></span> <span data-ttu-id="32259-121">Beispiel: "en-US" für Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="32259-121">For example, "en-US" for English (United States).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="32259-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32259-122">Requirements</span></span>



| <span data-ttu-id="32259-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32259-123">Requirement</span></span> | <span data-ttu-id="32259-124">Wert</span><span class="sxs-lookup"><span data-stu-id="32259-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32259-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32259-125">Minimum supported client</span></span><br/> | <span data-ttu-id="32259-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32259-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32259-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32259-127">Minimum supported server</span></span><br/> | <span data-ttu-id="32259-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32259-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32259-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32259-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="32259-130">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="32259-130">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="32259-131">**Lokalisierung (instrumentationmanifest)**</span><span class="sxs-lookup"><span data-stu-id="32259-131">**localization (instrumentationManifest)**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





