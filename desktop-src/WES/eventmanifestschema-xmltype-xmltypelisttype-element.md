---
title: XmlType (xmltypelisttype)-Element
description: Definiert einen XML-Typ.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- XmlType-Element EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342207"
---
# <a name="xmltype-xmltypelisttype-element"></a><span data-ttu-id="ad99b-104">XmlType (xmltypelisttype)-Element</span><span class="sxs-lookup"><span data-stu-id="ad99b-104">xmlType (XmlTypeListType) Element</span></span>

<span data-ttu-id="ad99b-105">Definiert einen XML-Typ.</span><span class="sxs-lookup"><span data-stu-id="ad99b-105">Defines an XML type.</span></span>

``` syntax
<xs:element name="xmlType">
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
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="ad99b-106">Das **XmlType** -Element wird durch den komplexen [**xmltypelisttype**](eventmanifestschema-xmltypelisttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ad99b-106">The **xmlType** element is defined by the [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="ad99b-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="ad99b-107">Attributes</span></span>



| <span data-ttu-id="ad99b-108">Name</span><span class="sxs-lookup"><span data-stu-id="ad99b-108">Name</span></span>   | <span data-ttu-id="ad99b-109">type</span><span class="sxs-lookup"><span data-stu-id="ad99b-109">Type</span></span>      | <span data-ttu-id="ad99b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad99b-110">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad99b-111">name</span><span class="sxs-lookup"><span data-stu-id="ad99b-111">name</span></span>   | <span data-ttu-id="ad99b-112">**QName**</span><span class="sxs-lookup"><span data-stu-id="ad99b-112">**QName**</span></span> | <span data-ttu-id="ad99b-113">Der Name des Ausgabe Typs.</span><span class="sxs-lookup"><span data-stu-id="ad99b-113">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="ad99b-114">Symbol</span><span class="sxs-lookup"><span data-stu-id="ad99b-114">symbol</span></span> | <span data-ttu-id="ad99b-115">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad99b-115">string</span></span>    | <span data-ttu-id="ad99b-116">Das Symbol, mit dem auf den Ausgabetyp in der Anwendung verwiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad99b-116">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="ad99b-117">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Ausgabetyp in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad99b-117">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="ad99b-118">value</span><span class="sxs-lookup"><span data-stu-id="ad99b-118">value</span></span>  | <span data-ttu-id="ad99b-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad99b-119">string</span></span>    | <span data-ttu-id="ad99b-120">Ein ganzzahliger Wert, der den Ausgabetyp in der Liste der von Ihnen definierten Ausgabetypen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ad99b-120">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="ad99b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad99b-121">Requirements</span></span>



| <span data-ttu-id="ad99b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad99b-122">Requirement</span></span> | <span data-ttu-id="ad99b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ad99b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad99b-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad99b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ad99b-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad99b-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ad99b-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad99b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ad99b-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad99b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad99b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad99b-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad99b-129">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="ad99b-129">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="ad99b-130">**xmltypes (typelisttype)**</span><span class="sxs-lookup"><span data-stu-id="ad99b-130">**xmlTypes (TypeListType)**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





