---
title: Performservervalidation (Peer-extensionstype)-Element (v2-Schema)
description: Erfahren Sie mehr über das performservervalidation (Peer-extensionstype)-Element. Dieses Element gibt an, ob die Server Validierung ausgeführt wird. | Performservervalidation (Peer-extensionstype)-Element (v2-Schema)
ms.assetid: a9c383d4-2582-47dd-bdf1-dd4e6c1689f7
keywords:
- Performservervalidation-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 32bc213aa67e87eb8af0643a15f16b298cfb3204
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219301"
---
# <a name="performservervalidation-peapextensionstype-element-v2-schema"></a><span data-ttu-id="5d0ed-106">Performservervalidation (Peer-extensionstype)-Element (v2-Schema)</span><span class="sxs-lookup"><span data-stu-id="5d0ed-106">PerformServerValidation (PeapExtensionsType) Element (V2 schema)</span></span>

<span data-ttu-id="5d0ed-107">Das **performservervalidation (etapextensionstype)** -Element gibt an, ob die Server Validierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d0ed-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element name="PerformServerValidation"
    type="xs:boolean"
 />
```

<span data-ttu-id="5d0ed-108">Das Element " **performservervalidation** " wird durch das " [**Peer-extensionstype**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) "-Element definiert.</span><span class="sxs-lookup"><span data-stu-id="5d0ed-108">The **PerformServerValidation** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d0ed-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d0ed-109">Remarks</span></span>

<span data-ttu-id="5d0ed-110">Das **performservervalidation** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d0ed-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0ed-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d0ed-111">Requirements</span></span>



| <span data-ttu-id="5d0ed-112">Role</span><span class="sxs-lookup"><span data-stu-id="5d0ed-112">Role</span></span> | <span data-ttu-id="5d0ed-113">Minimale Version des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="5d0ed-113">Minimum OS version</span></span> |
|------|--------------------|
| <span data-ttu-id="5d0ed-114">Client</span><span class="sxs-lookup"><span data-stu-id="5d0ed-114">Client</span></span><br/> | <span data-ttu-id="5d0ed-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d0ed-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5d0ed-116">Server</span><span class="sxs-lookup"><span data-stu-id="5d0ed-116">Server</span></span><br/> | <span data-ttu-id="5d0ed-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d0ed-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5d0ed-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d0ed-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d0ed-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="5d0ed-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5d0ed-120">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="5d0ed-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="5d0ed-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="5d0ed-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5d0ed-122">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="5d0ed-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="5d0ed-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5d0ed-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="5d0ed-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="5d0ed-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5d0ed-125">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="5d0ed-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5d0ed-126">mspeapconnectionpropertiesv2-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="5d0ed-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





