---
title: Identityprivacy (papextensionstype)-Element
description: Gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird. | Identityprivacy (papextensionstype)-Element
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Identityprivacy-Element EAPHost
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
ms.openlocfilehash: 2701352ee0e192dfd2d33fc2647b9ec6df96dd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530644"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="1fec0-105">Das identityprivacy (Peer-extensionstype)-Element</span><span class="sxs-lookup"><span data-stu-id="1fec0-105">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="1fec0-106">Das **identityprivacy (papextensionstype)** -Element gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fec0-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="1fec0-107">Das **identityprivacy** -Element wird durch das " [**Peer-extensionstype**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) "-Element definiert.</span><span class="sxs-lookup"><span data-stu-id="1fec0-107">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fec0-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fec0-108">Remarks</span></span>

<span data-ttu-id="1fec0-109">Das **identityprivacy** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="1fec0-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fec0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fec0-110">Requirements</span></span>



| <span data-ttu-id="1fec0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fec0-111">Requirement</span></span> | <span data-ttu-id="1fec0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="1fec0-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1fec0-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fec0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1fec0-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fec0-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1fec0-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fec0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1fec0-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fec0-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fec0-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fec0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="1fec0-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="1fec0-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1fec0-119">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="1fec0-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="1fec0-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="1fec0-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1fec0-121">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="1fec0-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="1fec0-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1fec0-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="1fec0-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="1fec0-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1fec0-124">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="1fec0-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="1fec0-125">mspeapconnectionpropertiesv2-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="1fec0-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





