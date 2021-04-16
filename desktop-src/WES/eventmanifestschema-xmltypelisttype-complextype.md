---
title: Komplexer xmltypelisttype-Typ
description: Definiert einen Listen Ausgabetyp, den der Dienst verwendet, um zu bestimmen, wie ein Eingabe Datentyp dargestellt werden soll.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Xmltypelisttype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340797"
---
# <a name="xmltypelisttype-complex-type"></a><span data-ttu-id="9312c-104">Komplexer xmltypelisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="9312c-104">XmlTypeListType Complex Type</span></span>

<span data-ttu-id="9312c-105">Definiert einen Listen Ausgabetyp, den der Dienst verwendet, um zu bestimmen, wie ein Eingabe Datentyp dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9312c-105">Defines a list output types that the service uses to determine how to render an input data type.</span></span>

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension
                        base="XmlType"
                    >
                        <xs:attribute name="name"
                            type="QName"
                            use="required"
                         />
                        <xs:attribute name="value"
                            type="string"
                            use="required"
                         />
                        <xs:attribute name="symbol"
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9312c-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9312c-106">Child elements</span></span>



| <span data-ttu-id="9312c-107">Element</span><span class="sxs-lookup"><span data-stu-id="9312c-107">Element</span></span>                                                                | <span data-ttu-id="9312c-108">type</span><span class="sxs-lookup"><span data-stu-id="9312c-108">Type</span></span> | <span data-ttu-id="9312c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9312c-109">Description</span></span>                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [<span data-ttu-id="9312c-110">**xmlType**</span><span class="sxs-lookup"><span data-stu-id="9312c-110">**xmlType**</span></span>](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | <span data-ttu-id="9312c-111">Definiert einen XML-Typ.</span><span class="sxs-lookup"><span data-stu-id="9312c-111">Defines an XML type.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="9312c-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="9312c-112">Attributes</span></span>



| <span data-ttu-id="9312c-113">Name</span><span class="sxs-lookup"><span data-stu-id="9312c-113">Name</span></span>   | <span data-ttu-id="9312c-114">type</span><span class="sxs-lookup"><span data-stu-id="9312c-114">Type</span></span>                                                              | <span data-ttu-id="9312c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9312c-115">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9312c-116">name</span><span class="sxs-lookup"><span data-stu-id="9312c-116">name</span></span>   | <span data-ttu-id="9312c-117">**QName**</span><span class="sxs-lookup"><span data-stu-id="9312c-117">**QName**</span></span>                                                         | <span data-ttu-id="9312c-118">Der Name des Ausgabe Typs.</span><span class="sxs-lookup"><span data-stu-id="9312c-118">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="9312c-119">Symbol</span><span class="sxs-lookup"><span data-stu-id="9312c-119">symbol</span></span> | [<span data-ttu-id="9312c-120">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="9312c-120">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="9312c-121">Das Symbol, mit dem auf den Ausgabetyp in der Anwendung verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9312c-121">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="9312c-122">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Ausgabetyp in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9312c-122">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="9312c-123">value</span><span class="sxs-lookup"><span data-stu-id="9312c-123">value</span></span>  | <span data-ttu-id="9312c-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9312c-124">string</span></span>                                                            | <span data-ttu-id="9312c-125">Ein ganzzahliger Wert, der den Ausgabetyp in der Liste der von Ihnen definierten Ausgabetypen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9312c-125">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="9312c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9312c-126">Remarks</span></span>

<span data-ttu-id="9312c-127">Die \\ include \\Winmeta.xml-Datei, die im Windows SDK enthalten ist, enthält eine Liste vordefinierter Ausgabetypen.</span><span class="sxs-lookup"><span data-stu-id="9312c-127">The \\Include\\Winmeta.xml file, which is included in the Windows SDK, contains a list of predefined output types.</span></span>

## <a name="requirements"></a><span data-ttu-id="9312c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9312c-128">Requirements</span></span>



| <span data-ttu-id="9312c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9312c-129">Requirement</span></span> | <span data-ttu-id="9312c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9312c-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9312c-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9312c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9312c-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9312c-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9312c-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9312c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9312c-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9312c-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





