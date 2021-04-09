---
description: Gibt an, ob die Komprimierung für den Daten Link für die Kopfzeile und die Datenübertragung verwendet wird.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Compression (ContextType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862763"
---
# <a name="compression-contexttype-element"></a><span data-ttu-id="ea82a-103">Compression (ContextType)-Element</span><span class="sxs-lookup"><span data-stu-id="ea82a-103">Compression (contextType) Element</span></span>

<span data-ttu-id="ea82a-104">Das **Compression (ContextType)** -Element gibt an, ob die Komprimierung für den Daten Link für den Header und die Datenübertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea82a-104">The **Compression (contextType)** element specifies if compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="ea82a-105">Bei diesem Element kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="ea82a-105">This element can be one of the following values.</span></span>

| <span data-ttu-id="ea82a-106">Wert</span><span class="sxs-lookup"><span data-stu-id="ea82a-106">Value</span></span>     | <span data-ttu-id="ea82a-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ea82a-107">Meaning</span></span>                       |
|-----------|-------------------------------|
| <span data-ttu-id="ea82a-108">Fähigen</span><span class="sxs-lookup"><span data-stu-id="ea82a-108">"ENABLE"</span></span>  | <span data-ttu-id="ea82a-109">Die Komprimierung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea82a-109">Compression will be used.</span></span>     |
| <span data-ttu-id="ea82a-110">Ier</span><span class="sxs-lookup"><span data-stu-id="ea82a-110">"DISABLE"</span></span> | <span data-ttu-id="ea82a-111">Die Komprimierung wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea82a-111">Compression will not be used.</span></span> |



 

<span data-ttu-id="ea82a-112">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ea82a-112">This element is optional.</span></span> <span data-ttu-id="ea82a-113">Wenn dieses Element nicht angegeben ist, verwendet das Mobile Breitbandsystem keine Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="ea82a-113">If this element is not specified, then the Mobile Broadband system will not use compression.</span></span>

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="ea82a-114">Das **Komprimierungs** Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="ea82a-114">The **Compression** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea82a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea82a-115">Requirements</span></span>



| <span data-ttu-id="ea82a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea82a-116">Requirement</span></span> | <span data-ttu-id="ea82a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ea82a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ea82a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea82a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ea82a-119">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ea82a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea82a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ea82a-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea82a-121">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ea82a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea82a-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea82a-123">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="ea82a-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ea82a-124">**contextType**</span><span class="sxs-lookup"><span data-stu-id="ea82a-124">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="ea82a-125">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="ea82a-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ea82a-126">**Kontext (mbnprofile)**</span><span class="sxs-lookup"><span data-stu-id="ea82a-126">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




