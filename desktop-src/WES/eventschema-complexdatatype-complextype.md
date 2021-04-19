---
title: Komplexer complexdatatype-Typ
description: Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- "\"Complexdatatype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339356"
---
# <a name="complexdatatype-complex-type"></a><span data-ttu-id="6990d-104">Komplexer complexdatatype-Typ</span><span class="sxs-lookup"><span data-stu-id="6990d-104">ComplexDataType Complex Type</span></span>

<span data-ttu-id="6990d-105">Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="6990d-105">Defines a structure that contains one or more data items.</span></span>

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6990d-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6990d-106">Child elements</span></span>



| <span data-ttu-id="6990d-107">Element</span><span class="sxs-lookup"><span data-stu-id="6990d-107">Element</span></span>                                                  | <span data-ttu-id="6990d-108">type</span><span class="sxs-lookup"><span data-stu-id="6990d-108">Type</span></span>                                                      | <span data-ttu-id="6990d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6990d-109">Description</span></span>                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6990d-110">**Daten**</span><span class="sxs-lookup"><span data-stu-id="6990d-110">**Data**</span></span>](eventschema-data-complexdatatype-element.md) | [<span data-ttu-id="6990d-111">**DataType**</span><span class="sxs-lookup"><span data-stu-id="6990d-111">**DataType**</span></span>](eventschema-datafieldtype-complextype.md) | <span data-ttu-id="6990d-112">Die Liste der Datenelemente in der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="6990d-112">The list of data items in the structure.</span></span> <span data-ttu-id="6990d-113">Die Liste der Elemente wird in derselben Reihenfolge wie in der Vorlage definiert.</span><span class="sxs-lookup"><span data-stu-id="6990d-113">The list of items are in the same order as defined in the template.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="6990d-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="6990d-114">Attributes</span></span>



| <span data-ttu-id="6990d-115">Name</span><span class="sxs-lookup"><span data-stu-id="6990d-115">Name</span></span> | <span data-ttu-id="6990d-116">type</span><span class="sxs-lookup"><span data-stu-id="6990d-116">Type</span></span>   | <span data-ttu-id="6990d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6990d-117">Description</span></span>                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6990d-118">Name</span><span class="sxs-lookup"><span data-stu-id="6990d-118">Name</span></span> | <span data-ttu-id="6990d-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6990d-119">string</span></span> | <span data-ttu-id="6990d-120">Der Name der Struktur.</span><span class="sxs-lookup"><span data-stu-id="6990d-120">The name of the structure.</span></span> <span data-ttu-id="6990d-121">Dies ist der Name, der angegeben wird, wenn Sie die Struktur in der Vorlage definiert haben (siehe den komplexen Typ " [**templateitemtype**](eventmanifestschema-templateitemtype-complextype.md) ").</span><span class="sxs-lookup"><span data-stu-id="6990d-121">This is the name that is specified when you defined the structure in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6990d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6990d-122">Remarks</span></span>

<span data-ttu-id="6990d-123">Die [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) -Funktion rendert den Inhalt einer Struktur als binäres Blob. die-Funktion stellt die einzelnen Datenelemente der-Struktur nicht dar.</span><span class="sxs-lookup"><span data-stu-id="6990d-123">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders the contents of a structure as a binary blob; the function does not render the individual data items of the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6990d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6990d-124">Requirements</span></span>



| <span data-ttu-id="6990d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6990d-125">Requirement</span></span> | <span data-ttu-id="6990d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6990d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6990d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6990d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6990d-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6990d-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6990d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6990d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6990d-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6990d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





