---
title: Komplexer bitmaptype-Typ
description: Definiert eine Liste von Name-Wert-Zuordnungen zwischen Bitwerten und Zeichen folgen Werten.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- Bitmaptype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479215"
---
# <a name="bitmaptype-complex-type"></a><span data-ttu-id="f99bd-104">Komplexer bitmaptype-Typ</span><span class="sxs-lookup"><span data-stu-id="f99bd-104">BitMapType Complex Type</span></span>

<span data-ttu-id="f99bd-105">Definiert eine Liste von Name-Wert-Zuordnungen zwischen Bitwerten und Zeichen folgen Werten.</span><span class="sxs-lookup"><span data-stu-id="f99bd-105">Defines a list of name/value mappings between bit values and string values.</span></span>

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f99bd-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f99bd-106">Child elements</span></span>



| <span data-ttu-id="f99bd-107">Element</span><span class="sxs-lookup"><span data-stu-id="f99bd-107">Element</span></span>                                                   | <span data-ttu-id="f99bd-108">type</span><span class="sxs-lookup"><span data-stu-id="f99bd-108">Type</span></span>                                                                       | <span data-ttu-id="f99bd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f99bd-109">Description</span></span>                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f99bd-110">**bilden**</span><span class="sxs-lookup"><span data-stu-id="f99bd-110">**map**</span></span>](eventmanifestschema-map-bitmaptype-element.md) | [<span data-ttu-id="f99bd-111">**Bitmapvaluetype**</span><span class="sxs-lookup"><span data-stu-id="f99bd-111">**BitMapValueType**</span></span>](eventmanifestschema-bitmapvaluetype-complextype.md) | <span data-ttu-id="f99bd-112">Definiert die Zuordnung zwischen einem Bitwert und einem Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="f99bd-112">Defines the mapping between a bit value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="f99bd-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="f99bd-113">Attributes</span></span>



| <span data-ttu-id="f99bd-114">Name</span><span class="sxs-lookup"><span data-stu-id="f99bd-114">Name</span></span>   | <span data-ttu-id="f99bd-115">type</span><span class="sxs-lookup"><span data-stu-id="f99bd-115">Type</span></span>                                                              | <span data-ttu-id="f99bd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f99bd-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f99bd-117">name</span><span class="sxs-lookup"><span data-stu-id="f99bd-117">name</span></span>   | <span data-ttu-id="f99bd-118">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f99bd-118">string</span></span>                                                            | <span data-ttu-id="f99bd-119">Der Name der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="f99bd-119">The name of the bitmap.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f99bd-120">Symbol</span><span class="sxs-lookup"><span data-stu-id="f99bd-120">symbol</span></span> | [<span data-ttu-id="f99bd-121">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="f99bd-121">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="f99bd-122">Das Symbol, das verwendet werden soll, um auf die Zuordnungen in der Anwendung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="f99bd-122">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="f99bd-123">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f99bd-123">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="f99bd-124">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="f99bd-124">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f99bd-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f99bd-125">Requirements</span></span>



| <span data-ttu-id="f99bd-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f99bd-126">Requirement</span></span> | <span data-ttu-id="f99bd-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f99bd-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f99bd-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f99bd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f99bd-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f99bd-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f99bd-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f99bd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f99bd-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f99bd-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





