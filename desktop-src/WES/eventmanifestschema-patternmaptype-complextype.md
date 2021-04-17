---
title: Komplexer Typ von patternmaptype
description: Nicht verwendet. Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um nach einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge zu suchen, und die andere wird verwendet, um die Zeichenfolge zu ändern
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- "\"Patternmaptype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477391"
---
# <a name="patternmaptype-complex-type"></a><span data-ttu-id="3c02d-106">Komplexer Typ von patternmaptype</span><span class="sxs-lookup"><span data-stu-id="3c02d-106">PatternMapType Complex Type</span></span>

<span data-ttu-id="3c02d-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c02d-107">Not used.</span></span> <span data-ttu-id="3c02d-108">Definiert eine Zuordnung zwischen zwei regulären Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="3c02d-108">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="3c02d-109">Ein Ausdruck wird verwendet, um nach einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge zu suchen, und die andere wird verwendet, um die Zeichenfolge zu ändern</span><span class="sxs-lookup"><span data-stu-id="3c02d-109">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3c02d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c02d-110">Child elements</span></span>



| <span data-ttu-id="3c02d-111">Element</span><span class="sxs-lookup"><span data-stu-id="3c02d-111">Element</span></span>                                                       | <span data-ttu-id="3c02d-112">type</span><span class="sxs-lookup"><span data-stu-id="3c02d-112">Type</span></span>                                                                               | <span data-ttu-id="3c02d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c02d-113">Description</span></span>                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c02d-114">**bilden**</span><span class="sxs-lookup"><span data-stu-id="3c02d-114">**map**</span></span>](eventmanifestschema-map-patternmaptype-element.md) | [<span data-ttu-id="3c02d-115">**Patternmapvaluetype**</span><span class="sxs-lookup"><span data-stu-id="3c02d-115">**PatternMapValueType**</span></span>](eventmanifestschema-patternmapvaluetype-complextype.md) | <span data-ttu-id="3c02d-116">Definiert die regulären Ausdrücke, mit denen eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge gesucht und geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3c02d-116">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="3c02d-117">Attributes</span><span class="sxs-lookup"><span data-stu-id="3c02d-117">Attributes</span></span>



| <span data-ttu-id="3c02d-118">Name</span><span class="sxs-lookup"><span data-stu-id="3c02d-118">Name</span></span>   | <span data-ttu-id="3c02d-119">type</span><span class="sxs-lookup"><span data-stu-id="3c02d-119">Type</span></span>                                                              | <span data-ttu-id="3c02d-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c02d-120">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c02d-121">format</span><span class="sxs-lookup"><span data-stu-id="3c02d-121">format</span></span> | <span data-ttu-id="3c02d-122">anyURI</span><span class="sxs-lookup"><span data-stu-id="3c02d-122">anyURI</span></span>                                                            | <span data-ttu-id="3c02d-123">Die zu verwendende Engine für reguläre Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="3c02d-123">The regular expression engine to use.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3c02d-124">name</span><span class="sxs-lookup"><span data-stu-id="3c02d-124">name</span></span>   | <span data-ttu-id="3c02d-125">**QName**</span><span class="sxs-lookup"><span data-stu-id="3c02d-125">**QName**</span></span>                                                         | <span data-ttu-id="3c02d-126">Der Name der Musterzuordnung.</span><span class="sxs-lookup"><span data-stu-id="3c02d-126">The name of the pattern map.</span></span> <span data-ttu-id="3c02d-127">Verwenden Sie den Namen in einem Datenelement, um auf die Zuordnungen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="3c02d-127">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="3c02d-128">Symbol</span><span class="sxs-lookup"><span data-stu-id="3c02d-128">symbol</span></span> | [<span data-ttu-id="3c02d-129">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="3c02d-129">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="3c02d-130">Das Symbol, das verwendet werden soll, um auf die Zuordnungen in der Anwendung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="3c02d-130">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="3c02d-131">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c02d-131">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="3c02d-132">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="3c02d-132">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3c02d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c02d-133">Requirements</span></span>



| <span data-ttu-id="3c02d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c02d-134">Requirement</span></span> | <span data-ttu-id="3c02d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3c02d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c02d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c02d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3c02d-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c02d-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3c02d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c02d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3c02d-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c02d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





