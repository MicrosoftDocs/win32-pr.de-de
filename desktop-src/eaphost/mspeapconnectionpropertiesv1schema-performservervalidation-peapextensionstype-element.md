---
title: Performservervalidation (etapextensionstype)-Element (V1-Schema)
description: Erfahren Sie mehr über das performservervalidation (Peer-extensionstype)-Element. Dieses Element gibt an, ob die Server Validierung ausgeführt wird. | Performservervalidation (etapextensionstype)-Element (V1-Schema)
ms.assetid: b0483ed0-a02f-4f60-b1ae-7c5e6be8e196
keywords:
- EAPHost-Element
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256d942d68c30788180f2d8080f963c1d79b401a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355130"
---
# <a name="performservervalidation-peapextensionstype-element-v1-schema"></a><span data-ttu-id="f49bb-106">Performservervalidation (etapextensionstype)-Element (V1-Schema)</span><span class="sxs-lookup"><span data-stu-id="f49bb-106">PerformServerValidation (PeapExtensionsType) element (v1 schema)</span></span>

<span data-ttu-id="f49bb-107">Das **performservervalidation (etapextensionstype)** -Element gibt an, ob die Server Validierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f49bb-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:PerformServerValidation"
 />
```

<span data-ttu-id="f49bb-108">Das-Element wird durch das-Element von " [**Peer**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) Type" definiert.</span><span class="sxs-lookup"><span data-stu-id="f49bb-108">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f49bb-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f49bb-109">Remarks</span></span>

<span data-ttu-id="f49bb-110">Das **performservervalidation** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="f49bb-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f49bb-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f49bb-111">Requirements</span></span>



| <span data-ttu-id="f49bb-112">Role</span><span class="sxs-lookup"><span data-stu-id="f49bb-112">Role</span></span> | <span data-ttu-id="f49bb-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="f49bb-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f49bb-114">Client</span><span class="sxs-lookup"><span data-stu-id="f49bb-114">Client</span></span><br/> | <span data-ttu-id="f49bb-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f49bb-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="f49bb-116">Server</span><span class="sxs-lookup"><span data-stu-id="f49bb-116">Server</span></span><br/> | <span data-ttu-id="f49bb-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f49bb-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f49bb-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f49bb-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f49bb-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="f49bb-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f49bb-120">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="f49bb-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="f49bb-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="f49bb-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f49bb-122">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="f49bb-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="f49bb-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f49bb-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f49bb-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="f49bb-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f49bb-125">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="f49bb-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f49bb-126">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="f49bb-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f49bb-127">**Performservervalidation (Peer-extensionstype)**</span><span class="sxs-lookup"><span data-stu-id="f49bb-127">**PerformServerValidation(PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





