---
title: Komplexer bitmapvaluetype-Typ
description: Definiert die Zuordnung zwischen einem Bitwert und einem Zeichen folgen Wert. | Komplexer bitmapvaluetype-Typ
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Bitmapvaluetype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961398"
---
# <a name="bitmapvaluetype-complex-type"></a><span data-ttu-id="b0e8c-105">Komplexer bitmapvaluetype-Typ</span><span class="sxs-lookup"><span data-stu-id="b0e8c-105">BitMapValueType Complex Type</span></span>

<span data-ttu-id="b0e8c-106">Definiert die Zuordnung zwischen einem Bitwert und einem Zeichen folgen Wert.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-106">Defines the mapping between a bit value and a string value.</span></span>

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
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

## <a name="attributes"></a><span data-ttu-id="b0e8c-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="b0e8c-107">Attributes</span></span>



| <span data-ttu-id="b0e8c-108">Name</span><span class="sxs-lookup"><span data-stu-id="b0e8c-108">Name</span></span>    | <span data-ttu-id="b0e8c-109">type</span><span class="sxs-lookup"><span data-stu-id="b0e8c-109">Type</span></span>                                                              | <span data-ttu-id="b0e8c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0e8c-110">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e8c-111">message</span><span class="sxs-lookup"><span data-stu-id="b0e8c-111">message</span></span> | [<span data-ttu-id="b0e8c-112">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="b0e8c-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="b0e8c-113">Der lokalisierte Zeichen folgen Wert, dem der Bitwert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-113">The localized string value to which the bit value maps.</span></span> <span data-ttu-id="b0e8c-114">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                  |
| <span data-ttu-id="b0e8c-115">Symbol</span><span class="sxs-lookup"><span data-stu-id="b0e8c-115">symbol</span></span>  | [<span data-ttu-id="b0e8c-116">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="b0e8c-116">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="b0e8c-117">Das Symbol, das für den Verweis auf die Karte in der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-117">The symbol to use to reference the map in your application.</span></span> <span data-ttu-id="b0e8c-118">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-118">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the map in the header file that the compiler generates.</span></span> <span data-ttu-id="b0e8c-119">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-119">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="b0e8c-120">value</span><span class="sxs-lookup"><span data-stu-id="b0e8c-120">value</span></span>   | [<span data-ttu-id="b0e8c-121">**HexInt32Type**</span><span class="sxs-lookup"><span data-stu-id="b0e8c-121">**HexInt32Type**</span></span>](eventmanifestschema-hex32type-simpletype.md)  | <span data-ttu-id="b0e8c-122">Der Bitwert, der dem Zeichen folgen Wert zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-122">The bit value to map to the string value.</span></span> <span data-ttu-id="b0e8c-123">Sie müssen eine hexadezimale Zahl angeben, für die ein einzelnes Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-123">You must specify a hexadecimal number that has a single bit set.</span></span><br/>                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="b0e8c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0e8c-124">Remarks</span></span>

<span data-ttu-id="b0e8c-125">Ordnet einen hexadezimalen Wert zu (die Zahl muss 0x vorangestellt sein), wobei ein einzelnes Bit auf einen Namen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b0e8c-125">Maps a hexadecimal value (the number must be preceded by 0x) with a single bit set to a name.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e8c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0e8c-126">Requirements</span></span>



| <span data-ttu-id="b0e8c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0e8c-127">Requirement</span></span> | <span data-ttu-id="b0e8c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b0e8c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0e8c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0e8c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e8c-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e8c-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b0e8c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0e8c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e8c-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e8c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





