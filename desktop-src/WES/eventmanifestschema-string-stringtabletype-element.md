---
title: String (stringtabletype)-Element
description: Definiert eine lokalisierte Zeichenfolge.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- Zeichen folgen Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956655"
---
# <a name="string-stringtabletype-element"></a><span data-ttu-id="6f16a-104">String (stringtabletype)-Element</span><span class="sxs-lookup"><span data-stu-id="6f16a-104">string (StringTableType) Element</span></span>

<span data-ttu-id="6f16a-105">Definiert eine lokalisierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6f16a-105">Defines a localized string.</span></span>

``` syntax
<xs:element name="string">
    <xs:complexType>
        <xs:attribute name="id"
            type="string"
            use="required"
         />
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="stringType"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6f16a-106">Das **String** -Element wird durch den komplexen [**stringtabletype**](eventmanifestschema-stringtabletype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="6f16a-106">The **string** element is defined by the [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="6f16a-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f16a-107">Attributes</span></span>



| <span data-ttu-id="6f16a-108">Name</span><span class="sxs-lookup"><span data-stu-id="6f16a-108">Name</span></span>       | <span data-ttu-id="6f16a-109">type</span><span class="sxs-lookup"><span data-stu-id="6f16a-109">Type</span></span>   | <span data-ttu-id="6f16a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f16a-110">Description</span></span>                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f16a-111">id</span><span class="sxs-lookup"><span data-stu-id="6f16a-111">id</span></span>         | <span data-ttu-id="6f16a-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6f16a-112">string</span></span> | <span data-ttu-id="6f16a-113">Ein Bezeichner, der die Zeichenfolge innerhalb der Zeichen folgen Tabelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6f16a-113">An identifier that uniquely identifies the string within the string table.</span></span><br/> |
| <span data-ttu-id="6f16a-114">StringType</span><span class="sxs-lookup"><span data-stu-id="6f16a-114">stringType</span></span> | <span data-ttu-id="6f16a-115">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6f16a-115">string</span></span> | <span data-ttu-id="6f16a-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6f16a-116">Not used.</span></span><br/>                                                                  |
| <span data-ttu-id="6f16a-117">value</span><span class="sxs-lookup"><span data-stu-id="6f16a-117">value</span></span>      | <span data-ttu-id="6f16a-118">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6f16a-118">string</span></span> | <span data-ttu-id="6f16a-119">Die lokalisierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6f16a-119">The localized string.</span></span><br/>                                                      |



## <a name="requirements"></a><span data-ttu-id="6f16a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f16a-120">Requirements</span></span>



| <span data-ttu-id="6f16a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f16a-121">Requirement</span></span> | <span data-ttu-id="6f16a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6f16a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6f16a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f16a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6f16a-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f16a-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6f16a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f16a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6f16a-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f16a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f16a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f16a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f16a-128">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="6f16a-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="6f16a-129">**STRINGTABLE (localizationtype)**</span><span class="sxs-lookup"><span data-stu-id="6f16a-129">**stringTable (LocalizationType)**</span></span>](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





