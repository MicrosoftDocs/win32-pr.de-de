---
title: Tlsextensions (V1-Schema)
description: Erfahren Sie mehr über das tlsextensions (eaptype)-Element. Dieses Element ermöglicht zukünftige Erweiterungen des Schemas.
ms.assetid: f968d91d-e226-44a9-98db-347cbedfa201
keywords:
- EAPHost-Element
topic_type:
- apiref
api_name:
- TLSExtensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f1ab2a6f00a4a8a9d530fa41865b2fd0cf0b8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338086"
---
# <a name="tlsextensions-v1-schema"></a><span data-ttu-id="6b091-105">Tlsextensions (V1-Schema)</span><span class="sxs-lookup"><span data-stu-id="6b091-105">TLSExtensions (v1 schema)</span></span>

<span data-ttu-id="6b091-106">Das **tlsextensions (eaptype)** -Element ermöglicht zukünftige Erweiterungen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="6b091-106">The **TLSExtensions (EapType)** element enables future enhancements to the schema.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: TLSExtensions"
 />
```

<span data-ttu-id="6b091-107">Das-Element wird durch das [**eaptype**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="6b091-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b091-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b091-108">Remarks</span></span>

<span data-ttu-id="6b091-109">Das **tlsextensions** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="6b091-109">The **TLSExtensions** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b091-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b091-110">Requirements</span></span>



| <span data-ttu-id="6b091-111">Role</span><span class="sxs-lookup"><span data-stu-id="6b091-111">Role</span></span> | <span data-ttu-id="6b091-112">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="6b091-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="6b091-113">Client</span><span class="sxs-lookup"><span data-stu-id="6b091-113">Client</span></span><br/> | <span data-ttu-id="6b091-114">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b091-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6b091-115">Server</span><span class="sxs-lookup"><span data-stu-id="6b091-115">Server</span></span><br/> | <span data-ttu-id="6b091-116">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b091-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b091-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b091-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b091-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="6b091-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6b091-119">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="6b091-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="6b091-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="6b091-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6b091-121">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="6b091-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="6b091-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6b091-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="6b091-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="6b091-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6b091-124">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="6b091-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="6b091-125">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="6b091-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6b091-126">**Tlsextensions (tlsextensionstype)**</span><span class="sxs-lookup"><span data-stu-id="6b091-126">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 





