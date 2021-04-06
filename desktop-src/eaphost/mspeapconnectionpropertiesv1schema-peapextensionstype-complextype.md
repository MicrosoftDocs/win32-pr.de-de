---
title: Komplexer Typ von "Peer apextensionstype"
description: Enthält in Windows 7 vorgenommene Schema Erweiterungen. Zukünftige Schema Erweiterungen werden von PeapExtensionsTypeV2 behandelt.
ms.assetid: a8fb8474-a375-4401-83b0-4fa87d637209
keywords:
- Komplexer Typ von "etapextensionstype" EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cb8c698122c5a466ae95f728838425a5f10c665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742841"
---
# <a name="peapextensionstype-complex-type"></a><span data-ttu-id="d63f0-105">Komplexer Typ von "Peer apextensionstype"</span><span class="sxs-lookup"><span data-stu-id="d63f0-105">PeapExtensionsType Complex Type</span></span>

<span data-ttu-id="d63f0-106">Der komplexe Typ " **etapextensionstype** " enthält in Windows 7 vorgenommene Schema Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="d63f0-106">The **PeapExtensionsType** complex type contains schema enhancements made in Windows 7.</span></span> <span data-ttu-id="d63f0-107">Zukünftige Schema Erweiterungen werden von [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md)behandelt.</span><span class="sxs-lookup"><span data-stu-id="d63f0-107">Future schema enhancements will be handled by [**PeapExtensionsTypeV2**](mspeapconnectionpropertiesv2-peapextensionstypev2-complextype.md).</span></span>

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PerformServerValidation"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:AcceptServerName"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:IdentityPrivacy"
         />
        <xs:element
            minOccurs="0"
            ref="extendedPeap:PeapExtensionsV2"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d63f0-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d63f0-108">Child elements</span></span>



| <span data-ttu-id="d63f0-109">Element</span><span class="sxs-lookup"><span data-stu-id="d63f0-109">Element</span></span>                                                                                                                               | <span data-ttu-id="d63f0-110">type</span><span class="sxs-lookup"><span data-stu-id="d63f0-110">Type</span></span> | <span data-ttu-id="d63f0-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d63f0-111">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------|------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d63f0-112">**extendedpeer: performservervalidation**</span><span class="sxs-lookup"><span data-stu-id="d63f0-112">**extendedPeap:PerformServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |      | <span data-ttu-id="d63f0-113">Windows 7 und höher: gibt an, ob die Server Validierung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d63f0-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                          |
| [<span data-ttu-id="d63f0-114">**extendedetap: akzeptservername**</span><span class="sxs-lookup"><span data-stu-id="d63f0-114">**extendedPeap:AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)               |      | <span data-ttu-id="d63f0-115">Windows 7 und höher: gibt an, ob der Name eines Servers gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="d63f0-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                            |
| [<span data-ttu-id="d63f0-116">**extendedpeer: identityprivacy**</span><span class="sxs-lookup"><span data-stu-id="d63f0-116">**extendedPeap:IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv1schema-identityprivacy-peapextensionstype-element.md)                 |      | <span data-ttu-id="d63f0-117">Windows 7 und höher: gibt an, ob die tatsächliche Identität eines Benutzers oder eine anonyme Identität gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d63f0-117">Windows 7 and later: indicates whether a user's true identity or an anonymous identity is sent.</span></span><br/> |
| [<span data-ttu-id="d63f0-118">**extendedpeer: PeapExtensionsV2**</span><span class="sxs-lookup"><span data-stu-id="d63f0-118">**extendedPeap:PeapExtensionsV2**</span></span>](mspeapconnectionpropertiesv1-peapextensionsv2-peapextensionstype-element.md)                     |      | <span data-ttu-id="d63f0-119">Windows 7 und höher: ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="d63f0-119">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                 |



## <a name="remarks"></a><span data-ttu-id="d63f0-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d63f0-120">Remarks</span></span>

<span data-ttu-id="d63f0-121">Das Element " **Peer-extensionstype** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="d63f0-121">The **PeapExtensionsType** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63f0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d63f0-122">Requirements</span></span>



| <span data-ttu-id="d63f0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d63f0-123">Requirement</span></span> | <span data-ttu-id="d63f0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d63f0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d63f0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d63f0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d63f0-126">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d63f0-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d63f0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d63f0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d63f0-128">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d63f0-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d63f0-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d63f0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63f0-130">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="d63f0-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d63f0-131">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="d63f0-131">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d63f0-132">komplexe mspeapconnectionpropertiesv1-Schema Typen</span><span class="sxs-lookup"><span data-stu-id="d63f0-132">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





