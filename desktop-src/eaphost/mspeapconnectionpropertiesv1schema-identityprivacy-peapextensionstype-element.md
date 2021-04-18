---
title: Identityprivacy (papextensionstype)-Element
description: Gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird. | Identityprivacy (papextensionstype)-Element
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- EAPHost-Element
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
ms.openlocfilehash: ed566e9be0b9e194d24106f1c82d9a9d6d1a199d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371859"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="895f9-105">Identityprivacy (papextensionstype)-Element</span><span class="sxs-lookup"><span data-stu-id="895f9-105">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="895f9-106">Das **identityprivacy (papextensionstype)** -Element gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="895f9-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="895f9-107">Das-Element wird durch das-Element von " [**Peer**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) Type" definiert.</span><span class="sxs-lookup"><span data-stu-id="895f9-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="895f9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="895f9-108">Remarks</span></span>

<span data-ttu-id="895f9-109">Das **identityprivacy** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="895f9-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="895f9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="895f9-110">Requirements</span></span>



| <span data-ttu-id="895f9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="895f9-111">Requirement</span></span> | <span data-ttu-id="895f9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="895f9-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="895f9-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="895f9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="895f9-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="895f9-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="895f9-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="895f9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="895f9-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="895f9-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="895f9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="895f9-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="895f9-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="895f9-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="895f9-119">**Peer-extensionstype**</span><span class="sxs-lookup"><span data-stu-id="895f9-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="895f9-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="895f9-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="895f9-121">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="895f9-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="895f9-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="895f9-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="895f9-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="895f9-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="895f9-124">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="895f9-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="895f9-125">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="895f9-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="895f9-126">**Identityprivacy (papextensionstype)**</span><span class="sxs-lookup"><span data-stu-id="895f9-126">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





