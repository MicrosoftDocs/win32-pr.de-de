---
title: Komplexer valuemapvaluetype-Typ
description: Definiert die Zuordnung zwischen einem ganzzahligen Wert und einem Zeichen folgen Wert. | Komplexer valuemapvaluetype-Typ
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- "\"Valuemapvaluetype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393914"
---
# <a name="valuemapvaluetype-complex-type"></a><span data-ttu-id="a08aa-105">Komplexer valuemapvaluetype-Typ</span><span class="sxs-lookup"><span data-stu-id="a08aa-105">ValueMapValueType Complex Type</span></span>

<span data-ttu-id="a08aa-106">Definiert die Zuordnung zwischen einem ganzzahligen Wert und einem Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="a08aa-106">Defines the mapping between an integer value and a string value.</span></span>

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="a08aa-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="a08aa-107">Attributes</span></span>



| <span data-ttu-id="a08aa-108">Name</span><span class="sxs-lookup"><span data-stu-id="a08aa-108">Name</span></span>    | <span data-ttu-id="a08aa-109">type</span><span class="sxs-lookup"><span data-stu-id="a08aa-109">Type</span></span>                                                              | <span data-ttu-id="a08aa-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a08aa-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a08aa-111">message</span><span class="sxs-lookup"><span data-stu-id="a08aa-111">message</span></span> | [<span data-ttu-id="a08aa-112">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="a08aa-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="a08aa-113">Der lokalisierte Zeichen folgen Wert, dem der ganzzahlige Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a08aa-113">The localized string value to which the integer value maps.</span></span> <span data-ttu-id="a08aa-114">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="a08aa-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                              |
| <span data-ttu-id="a08aa-115">Symbol</span><span class="sxs-lookup"><span data-stu-id="a08aa-115">symbol</span></span>  | [<span data-ttu-id="a08aa-116">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="a08aa-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a08aa-117">Das Symbol, das für den Verweis auf die Karte in der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a08aa-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="a08aa-118">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a08aa-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="a08aa-119">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="a08aa-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="a08aa-120">value</span><span class="sxs-lookup"><span data-stu-id="a08aa-120">value</span></span>   | [<span data-ttu-id="a08aa-121">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="a08aa-121">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="a08aa-122">Der ganzzahlige Wert, der dem Zeichen folgen Wert zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a08aa-122">The integer value to map to the string value.</span></span><br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a><span data-ttu-id="a08aa-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a08aa-123">Requirements</span></span>



| <span data-ttu-id="a08aa-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a08aa-124">Requirement</span></span> | <span data-ttu-id="a08aa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a08aa-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a08aa-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a08aa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a08aa-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a08aa-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a08aa-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a08aa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a08aa-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a08aa-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





