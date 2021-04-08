---
description: Identifiziert den Stamm Knoten des indikatorenabschnitts eines Instrumentierungs Manifests.
ms.assetid: f16f432b-466f-4a3c-bc1b-e80b876a2511
title: Counters-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11ced77890dba6d47f713642adf9b41d4b30f6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865107"
---
# <a name="counters-element"></a><span data-ttu-id="6bddf-103">Counters-Element</span><span class="sxs-lookup"><span data-stu-id="6bddf-103">counters Element</span></span>

<span data-ttu-id="6bddf-104">Identifiziert den Stamm Knoten des indikatorenabschnitts eines Instrumentierungs Manifests.</span><span class="sxs-lookup"><span data-stu-id="6bddf-104">Identifies the root node of the counters section of an instrumentation manifest.</span></span>

``` syntax
<xs:element name="counters"
    type="man:counters"
>
    <xs:key name="uniqueprovGUID">
        <xs:selector
            xpath="./man:provider"
         />
        <xs:field
            xpath="@providerGuid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetGUID">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@guid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetURI">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetName">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@name"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:key>
    <xs:unique name="uniqueCounterSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:unique>
    <xs:key name="uniqueCounterURI">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
</xs:element>
```

## <a name="remarks"></a><span data-ttu-id="6bddf-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bddf-105">Remarks</span></span>

<span data-ttu-id="6bddf-106">Der übergeordnete Knoten dieses Elements ist das [**Instrumentations**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) Element des Manifests.</span><span class="sxs-lookup"><span data-stu-id="6bddf-106">This element's parent node is the [**instrumentation**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) element of the manifest.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bddf-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6bddf-107">Requirements</span></span>



| <span data-ttu-id="6bddf-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6bddf-108">Requirement</span></span> | <span data-ttu-id="6bddf-109">Wert</span><span class="sxs-lookup"><span data-stu-id="6bddf-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6bddf-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6bddf-110">Minimum supported client</span></span><br/> | <span data-ttu-id="6bddf-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bddf-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6bddf-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6bddf-112">Minimum supported server</span></span><br/> | <span data-ttu-id="6bddf-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6bddf-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

