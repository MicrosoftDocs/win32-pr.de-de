---
title: AnonymousUserName (identityprivacyparameters)-Element
description: Enthält eine anonyme Identität, die anstelle der true-Identifizierung eines Benutzers verwendet wird. Sie wird während der ersten Phase der Peer-Authentifizierung gesendet, wenn die Identität als nur-Text gesendet wird.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- AnonymousUserName-Element EAPHost
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392055"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a><span data-ttu-id="d5d8f-105">AnonymousUserName (identityprivacyparameters)-Element</span><span class="sxs-lookup"><span data-stu-id="d5d8f-105">AnonymousUserName (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="d5d8f-106">Das **AnonymousUserName (identityprivacyparameters)** -Element enthält eine anonyme Identität, die anstelle der true-Identifikation eines Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5d8f-106">The **AnonymousUserName (IdentityPrivacyParameters)** element contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="d5d8f-107">Sie wird während der ersten Phase der Peer-Authentifizierung gesendet, wenn die **Identität** als nur-Text gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5d8f-107">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span>

<span data-ttu-id="d5d8f-108">Die Verwendung der anonymen Identität wird vom [**enableidentityprivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) -Element bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d5d8f-108">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

<span data-ttu-id="d5d8f-109">Das **AnonymousUserName** -Element wird durch die [identityprivacyparameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="d5d8f-109">The **AnonymousUserName** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d8f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5d8f-110">Remarks</span></span>

<span data-ttu-id="d5d8f-111">Das **AnonymousUserName** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5d8f-111">The **AnonymousUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d8f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5d8f-112">Requirements</span></span>



| <span data-ttu-id="d5d8f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5d8f-113">Requirement</span></span> | <span data-ttu-id="d5d8f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d5d8f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d5d8f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5d8f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d8f-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5d8f-116">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d5d8f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5d8f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d8f-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5d8f-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5d8f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5d8f-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5d8f-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d5d8f-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d5d8f-121">Identityprivacyparameters</span><span class="sxs-lookup"><span data-stu-id="d5d8f-121">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="d5d8f-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="d5d8f-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d5d8f-123">**"Peer Erweiterungen"**</span><span class="sxs-lookup"><span data-stu-id="d5d8f-123">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="d5d8f-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="d5d8f-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d5d8f-125">mspeapconnectionpropertiesv2-Schema</span><span class="sxs-lookup"><span data-stu-id="d5d8f-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d5d8f-126">mspeapconnectionpropertiesv2-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="d5d8f-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





