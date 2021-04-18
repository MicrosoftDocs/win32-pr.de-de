---
title: Komplexer keywordtype-Typ
description: Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet. | Komplexer keywordtype-Typ
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- Keywordtype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351878"
---
# <a name="keywordtype-complex-type"></a><span data-ttu-id="2b3fa-105">Komplexer keywordtype-Typ</span><span class="sxs-lookup"><span data-stu-id="2b3fa-105">KeywordType Complex Type</span></span>

<span data-ttu-id="2b3fa-106">Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="2b3fa-107">Ein Schlüsselwort ist ein Tag, das Sie an ein Ereignis anfügen, um Ereignisse auf der Grundlage ihrer Verwendung zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="2b3fa-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2b3fa-108">Attributes</span></span>



| <span data-ttu-id="2b3fa-109">Name</span><span class="sxs-lookup"><span data-stu-id="2b3fa-109">Name</span></span>    | <span data-ttu-id="2b3fa-110">type</span><span class="sxs-lookup"><span data-stu-id="2b3fa-110">Type</span></span>                                                              | <span data-ttu-id="2b3fa-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b3fa-111">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3fa-112">mask</span><span class="sxs-lookup"><span data-stu-id="2b3fa-112">mask</span></span>    | [<span data-ttu-id="2b3fa-113">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="2b3fa-113">**HexInt64Type**</span></span>](eventmanifestschema-hex64type-simpletype.md)  | <span data-ttu-id="2b3fa-114">Eine Bitmaske, für die nur ein einzelnes Bit festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-114">A bitmask that must have only a single bit set.</span></span> <span data-ttu-id="2b3fa-115">Das Bit stellt eine Kategorie von Ereignissen dar (z. b. Lese-oder Schreib Ereignisse).</span><span class="sxs-lookup"><span data-stu-id="2b3fa-115">The bit represents a category of events (for example, read events or write events).</span></span> <span data-ttu-id="2b3fa-116">Sie können Bitwerte im Bereich von 0x0000000000000001 bis 0x0000800000000000 (Bits 0 bis 47) angeben.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-116">You can specify bit values in the range from 0x0000000000000001 through 0x0000800000000000 (bits 0 through 47).</span></span><br/>                                                         |
| <span data-ttu-id="2b3fa-117">message</span><span class="sxs-lookup"><span data-stu-id="2b3fa-117">message</span></span> | [<span data-ttu-id="2b3fa-118">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="2b3fa-118">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="2b3fa-119">Der lokalisierte Anzeige Name für das Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-119">The localized display name for the keyword.</span></span> <span data-ttu-id="2b3fa-120">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-120">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                                                                                       |
| <span data-ttu-id="2b3fa-121">name</span><span class="sxs-lookup"><span data-stu-id="2b3fa-121">name</span></span>    | <span data-ttu-id="2b3fa-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="2b3fa-122">**QName**</span></span>                                                         | <span data-ttu-id="2b3fa-123">Der Name des Schlüssel Worts.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-123">The name of the keyword.</span></span> <span data-ttu-id="2b3fa-124">Der Name muss innerhalb der Liste der Schlüsselwörter, die vom Anbieter definiert werden, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-124">The name must be unique within the list of keywords that the provider defines.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="2b3fa-125">Symbol</span><span class="sxs-lookup"><span data-stu-id="2b3fa-125">symbol</span></span>  | [<span data-ttu-id="2b3fa-126">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="2b3fa-126">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="2b3fa-127">Das Symbol, das verwendet wird, um auf das Schlüsselwort in Ihrer Anwendung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-127">The symbol to use to reference the keyword in your application.</span></span> <span data-ttu-id="2b3fa-128">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für das Schlüsselwort in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-128">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the keyword in the header file that the compiler generates.</span></span> <span data-ttu-id="2b3fa-129">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-129">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2b3fa-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b3fa-130">Remarks</span></span>

<span data-ttu-id="2b3fa-131">Die Winmeta.xml-Datei, die in der Windows SDK enthalten ist, enthält eine Liste von Schlüsselwörtern.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-131">The Winmeta.xml file that is included in the Windows SDK contains a list of keywords.</span></span> <span data-ttu-id="2b3fa-132">Diese Schlüsselwörter sind reserviert und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b3fa-132">These keywords are reserved and should not be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3fa-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b3fa-133">Requirements</span></span>



| <span data-ttu-id="2b3fa-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b3fa-134">Requirement</span></span> | <span data-ttu-id="2b3fa-135">Wert</span><span class="sxs-lookup"><span data-stu-id="2b3fa-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b3fa-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b3fa-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2b3fa-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b3fa-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2b3fa-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b3fa-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2b3fa-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b3fa-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





