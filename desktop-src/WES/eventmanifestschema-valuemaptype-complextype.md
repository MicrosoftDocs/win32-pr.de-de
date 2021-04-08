---
title: Komplexer Typ valuemaptype
description: Definiert eine Liste von Name-Wert-Zuordnungen zwischen ganzzahligen Werten und Zeichen folgen Werten.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- "\"Valuemaptype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28fde51466ba506802c8dbc5379f1628fd943fa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739713"
---
# <a name="valuemaptype-complex-type"></a><span data-ttu-id="4f98c-104">Komplexer Typ valuemaptype</span><span class="sxs-lookup"><span data-stu-id="4f98c-104">ValueMapType Complex Type</span></span>

<span data-ttu-id="4f98c-105">Definiert eine Liste von Name-Wert-Zuordnungen zwischen ganzzahligen Werten und Zeichen folgen Werten.</span><span class="sxs-lookup"><span data-stu-id="4f98c-105">Defines a list of name/value mappings between integer values and string values.</span></span>

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4f98c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f98c-106">Child elements</span></span>



| <span data-ttu-id="4f98c-107">Element</span><span class="sxs-lookup"><span data-stu-id="4f98c-107">Element</span></span>                                                     | <span data-ttu-id="4f98c-108">type</span><span class="sxs-lookup"><span data-stu-id="4f98c-108">Type</span></span>                                                                           | <span data-ttu-id="4f98c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f98c-109">Description</span></span>                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="4f98c-110">**bilden**</span><span class="sxs-lookup"><span data-stu-id="4f98c-110">**map**</span></span>](eventmanifestschema-map-valuemaptype-element.md) | [<span data-ttu-id="4f98c-111">**Valuemapvaluetype**</span><span class="sxs-lookup"><span data-stu-id="4f98c-111">**ValueMapValueType**</span></span>](eventmanifestschema-valuemapvaluetype-complextype.md) | <span data-ttu-id="4f98c-112">Definiert die Zuordnung zwischen einem ganzzahligen Wert und einem Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="4f98c-112">Defines the mapping between an integer value and a string value.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="4f98c-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="4f98c-113">Attributes</span></span>



| <span data-ttu-id="4f98c-114">Name</span><span class="sxs-lookup"><span data-stu-id="4f98c-114">Name</span></span>   | <span data-ttu-id="4f98c-115">type</span><span class="sxs-lookup"><span data-stu-id="4f98c-115">Type</span></span>                                                              | <span data-ttu-id="4f98c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f98c-116">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f98c-117">name</span><span class="sxs-lookup"><span data-stu-id="4f98c-117">name</span></span>   | <span data-ttu-id="4f98c-118">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4f98c-118">string</span></span>                                                            | <span data-ttu-id="4f98c-119">Der Name der Wertzuordnung.</span><span class="sxs-lookup"><span data-stu-id="4f98c-119">The name of the value map.</span></span> <span data-ttu-id="4f98c-120">Verwenden Sie den Namen in einem Datenelement, um auf die Zuordnungen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="4f98c-120">Use the name in a data element to reference the mappings.</span></span><br/>                                                                                                                                                                                                                     |
| <span data-ttu-id="4f98c-121">Symbol</span><span class="sxs-lookup"><span data-stu-id="4f98c-121">symbol</span></span> | [<span data-ttu-id="4f98c-122">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="4f98c-122">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="4f98c-123">Das Symbol, das verwendet werden soll, um auf die Zuordnungen in der Anwendung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="4f98c-123">The symbol to use to reference the mappings in your application.</span></span> <span data-ttu-id="4f98c-124">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f98c-124">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="4f98c-125">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="4f98c-125">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4f98c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f98c-126">Requirements</span></span>



| <span data-ttu-id="4f98c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f98c-127">Requirement</span></span> | <span data-ttu-id="4f98c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4f98c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4f98c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f98c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4f98c-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f98c-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4f98c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f98c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4f98c-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f98c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





