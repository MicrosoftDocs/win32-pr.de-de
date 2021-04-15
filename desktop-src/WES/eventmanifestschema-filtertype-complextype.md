---
title: Komplexer FilterType-Typ
description: Definiert einen Daten Filter, den eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- "\"FilterType Complex Type Event Log\""
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479275"
---
# <a name="filtertype-complex-type"></a><span data-ttu-id="e7287-104">Komplexer FilterType-Typ</span><span class="sxs-lookup"><span data-stu-id="e7287-104">FilterType Complex Type</span></span>

<span data-ttu-id="e7287-105">Definiert einen Daten Filter, den eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e7287-105">Defines a data filter that a session uses to filter events based on event data.</span></span>

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="e7287-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="e7287-106">Attributes</span></span>



| <span data-ttu-id="e7287-107">Name</span><span class="sxs-lookup"><span data-stu-id="e7287-107">Name</span></span>    | <span data-ttu-id="e7287-108">type</span><span class="sxs-lookup"><span data-stu-id="e7287-108">Type</span></span>                                                              | <span data-ttu-id="e7287-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7287-109">Description</span></span>                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7287-110">message</span><span class="sxs-lookup"><span data-stu-id="e7287-110">message</span></span> | [<span data-ttu-id="e7287-111">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="e7287-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="e7287-112">Die lokalisierte Beschreibung für den Filter.</span><span class="sxs-lookup"><span data-stu-id="e7287-112">The localized description for the filter.</span></span> <span data-ttu-id="e7287-113">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="e7287-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span><br/>                                   |
| <span data-ttu-id="e7287-114">name</span><span class="sxs-lookup"><span data-stu-id="e7287-114">name</span></span>    | <span data-ttu-id="e7287-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="e7287-115">**QName**</span></span>                                                         | <span data-ttu-id="e7287-116">Ein Name, der den Filter angibt.</span><span class="sxs-lookup"><span data-stu-id="e7287-116">A name that identifies the filter.</span></span><br/>                                                                                                                                                                                                    |
| <span data-ttu-id="e7287-117">Symbol</span><span class="sxs-lookup"><span data-stu-id="e7287-117">symbol</span></span>  | [<span data-ttu-id="e7287-118">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="e7287-118">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="e7287-119">Das Symbol, das für den Verweis auf den Filter in der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7287-119">The symbol to use to reference the filter in your application.</span></span> <span data-ttu-id="e7287-120">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Filter in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e7287-120">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the filter in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="e7287-121">tid</span><span class="sxs-lookup"><span data-stu-id="e7287-121">tid</span></span>     | <span data-ttu-id="e7287-122">token</span><span class="sxs-lookup"><span data-stu-id="e7287-122">token</span></span>                                                             | <span data-ttu-id="e7287-123">Ein Vorlagen Bezeichner, der die Filterdaten beschreibt, die die Sitzung an den Anbieter übergibt, wenn Sie den Anbieter aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e7287-123">A template identifier that describes the filter data that the session passes to the provider when it enables the provider.</span></span><br/>                                                                                                            |
| <span data-ttu-id="e7287-124">value</span><span class="sxs-lookup"><span data-stu-id="e7287-124">value</span></span>   | [<span data-ttu-id="e7287-125">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="e7287-125">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="e7287-126">Ein ganzzahliger Wert, der den Filter in der Liste der von Ihnen definierten Filter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7287-126">An integer value that uniquely identifies the filter within the list of filters that you define.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e7287-127">version</span><span class="sxs-lookup"><span data-stu-id="e7287-127">version</span></span> | [<span data-ttu-id="e7287-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="e7287-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="e7287-129">Ein ganzzahliger Wert, der diese Version des Filters identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7287-129">An integer value that identifies this version of the filter.</span></span> <span data-ttu-id="e7287-130">Wenn nicht angegeben, ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e7287-130">If not specified, the value is zero.</span></span><br/>                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="e7287-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7287-131">Requirements</span></span>



| <span data-ttu-id="e7287-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7287-132">Requirement</span></span> | <span data-ttu-id="e7287-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e7287-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e7287-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7287-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e7287-135">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7287-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e7287-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7287-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e7287-137">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7287-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





