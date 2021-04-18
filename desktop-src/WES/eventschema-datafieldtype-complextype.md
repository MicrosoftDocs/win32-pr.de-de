---
title: Komplexer DataType-Typ (Windows-Ereignisprotokoll)
description: Definiert ein Datenelement.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- DataType Complex-Typ EventLog
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341057"
---
# <a name="datatype-complex-type"></a><span data-ttu-id="2292f-104">Komplexer DataType-Typ</span><span class="sxs-lookup"><span data-stu-id="2292f-104">DataType Complex Type</span></span>

<span data-ttu-id="2292f-105">Definiert ein Datenelement.</span><span class="sxs-lookup"><span data-stu-id="2292f-105">Defines a data item.</span></span>

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="2292f-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="2292f-106">Attributes</span></span>



| <span data-ttu-id="2292f-107">Name</span><span class="sxs-lookup"><span data-stu-id="2292f-107">Name</span></span> | <span data-ttu-id="2292f-108">type</span><span class="sxs-lookup"><span data-stu-id="2292f-108">Type</span></span>   | <span data-ttu-id="2292f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2292f-109">Description</span></span>                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2292f-110">Name</span><span class="sxs-lookup"><span data-stu-id="2292f-110">Name</span></span> | <span data-ttu-id="2292f-111">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2292f-111">string</span></span> | <span data-ttu-id="2292f-112">Der Name eines Datenelements, das in der Vorlage definiert wurde (siehe den komplexen Typ " [**templateitemtype**](eventmanifestschema-templateitemtype-complextype.md) ").</span><span class="sxs-lookup"><span data-stu-id="2292f-112">The name of a data item that was defined in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |
| <span data-ttu-id="2292f-113">type</span><span class="sxs-lookup"><span data-stu-id="2292f-113">Type</span></span> | <span data-ttu-id="2292f-114">QName</span><span class="sxs-lookup"><span data-stu-id="2292f-114">QName</span></span>  | <span data-ttu-id="2292f-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2292f-115">Not used.</span></span><br/>                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="2292f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2292f-116">Remarks</span></span>

<span data-ttu-id="2292f-117">Das Datenelement kann ein Datenelement der obersten Ebene oder ein Datenelement in einer Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="2292f-117">The data item can be a top-level data item or a data item in a structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2292f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2292f-118">Requirements</span></span>



| <span data-ttu-id="2292f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2292f-119">Requirement</span></span> | <span data-ttu-id="2292f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2292f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2292f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2292f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2292f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2292f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2292f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2292f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2292f-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2292f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





