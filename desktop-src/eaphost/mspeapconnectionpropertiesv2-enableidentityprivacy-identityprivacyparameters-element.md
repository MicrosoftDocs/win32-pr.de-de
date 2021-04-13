---
title: Enableidentityprivacy (identityprivacyparameters)-Element
description: Gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird. | Enableidentityprivacy (identityprivacyparameters)-Element
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Enableidentityprivacy-Element EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353769"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a><span data-ttu-id="2a930-105">Enableidentityprivacy (identityprivacyparameters)-Element</span><span class="sxs-lookup"><span data-stu-id="2a930-105">EnableIdentityPrivacy (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="2a930-106">Das **enableidentityprivacy (identityprivacyparameters)** -Element gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a930-106">The **EnableIdentityPrivacy (IdentityPrivacyParameters)** element Indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="2a930-107">Das **enableidentityprivacy** -Element wird durch die [identityprivacyparameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="2a930-107">The **EnableIdentityPrivacy** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="2a930-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a930-108">Remarks</span></span>

<span data-ttu-id="2a930-109">Das **enableidentityprivacy** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="2a930-109">The **EnableIdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a930-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a930-110">Requirements</span></span>



| <span data-ttu-id="2a930-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a930-111">Requirement</span></span> | <span data-ttu-id="2a930-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2a930-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2a930-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a930-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2a930-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a930-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2a930-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a930-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2a930-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a930-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a930-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a930-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a930-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="2a930-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2a930-119">Identityprivacyparameters</span><span class="sxs-lookup"><span data-stu-id="2a930-119">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="2a930-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="2a930-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2a930-121">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="2a930-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="2a930-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2a930-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="2a930-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="2a930-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2a930-124">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="2a930-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2a930-125">mspeapconnectionpropertiesv2-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="2a930-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





