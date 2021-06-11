---
title: IdentityPrivacy (PeapExtensionsType) -Element (v1)
description: Das IdentityPrivacy-Element (PeapExtensionsType) gibt an, ob die echte Identität eines Benutzers im Schema mspeapconnectionpropertiesv1 gesendet wird.
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- Element EAPHost
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
ms.openlocfilehash: 7195ce43fb3f1a1f1710fe7aee3f5f74e18f3786
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989215"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="db2fd-104">IdentityPrivacy(PeapExtensionsType)-Element</span><span class="sxs-lookup"><span data-stu-id="db2fd-104">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="db2fd-105">Das **IdentityPrivacy-Element (PeapExtensionsType)** gibt an, ob die echte Identität eines Benutzers oder eine anonyme Identität gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="db2fd-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="db2fd-106">Das -Element wird durch das [**PeapExtensionsType-Element**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="db2fd-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="db2fd-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db2fd-107">Remarks</span></span>

<span data-ttu-id="db2fd-108">Das **IdentityPrivacy-Element** ist optional.</span><span class="sxs-lookup"><span data-stu-id="db2fd-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="db2fd-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="db2fd-109">Requirements</span></span>



| <span data-ttu-id="db2fd-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db2fd-110">Requirement</span></span> | <span data-ttu-id="db2fd-111">Wert</span><span class="sxs-lookup"><span data-stu-id="db2fd-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="db2fd-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db2fd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="db2fd-113">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db2fd-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="db2fd-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db2fd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="db2fd-115">Nur Windows Server 2008 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db2fd-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db2fd-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db2fd-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="db2fd-117">**Definitionskontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="db2fd-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="db2fd-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="db2fd-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="db2fd-119">**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**</span><span class="sxs-lookup"><span data-stu-id="db2fd-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="db2fd-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="db2fd-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="db2fd-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="db2fd-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="db2fd-122">EAPHost und Legacyschema</span><span class="sxs-lookup"><span data-stu-id="db2fd-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="db2fd-123">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="db2fd-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="db2fd-124">mspeapconnectionpropertiesv1-Schemaelemente</span><span class="sxs-lookup"><span data-stu-id="db2fd-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="db2fd-125">**IdentityPrivacy(PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="db2fd-125">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





