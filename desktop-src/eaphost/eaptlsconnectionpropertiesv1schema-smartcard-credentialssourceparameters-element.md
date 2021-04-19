---
title: Smartcard-Element ("kredentialssourceparameters")
description: Gibt an, dass EAP-TLS das Zertifikat von der Smartcard lesen soll.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Smartcard-Element EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342842"
---
# <a name="smartcard-credentialssourceparameters-element"></a><span data-ttu-id="3490e-104">Smartcard-Element ("kredentialssourceparameters")</span><span class="sxs-lookup"><span data-stu-id="3490e-104">SmartCard (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="3490e-105">Das **Smartcard-Element ("kredentialssourceparameters")** gibt an, dass EAP-TLS das Zertifikat von der Smartcard lesen soll.</span><span class="sxs-lookup"><span data-stu-id="3490e-105">The **SmartCard (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the Smart Card.</span></span>

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

<span data-ttu-id="3490e-106">Das **Smartcard** -Element wird durch den komplexen Typ " [**dedentialssourceparameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="3490e-106">The **SmartCard** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3490e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3490e-107">Remarks</span></span>

<span data-ttu-id="3490e-108">Die [**certifikatestore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) -und **Smartcard** -Elemente können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3490e-108">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and **SmartCard** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="3490e-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3490e-109">Requirements</span></span>



| <span data-ttu-id="3490e-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3490e-110">Requirement</span></span> | <span data-ttu-id="3490e-111">Wert</span><span class="sxs-lookup"><span data-stu-id="3490e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3490e-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3490e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3490e-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3490e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3490e-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3490e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3490e-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3490e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3490e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3490e-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="3490e-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="3490e-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3490e-118">**"Kredentialssourceparameters"**</span><span class="sxs-lookup"><span data-stu-id="3490e-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="3490e-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="3490e-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3490e-120">**"Kredentialssource" (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="3490e-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="3490e-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3490e-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3490e-122">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="3490e-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3490e-123">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="3490e-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3490e-124">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="3490e-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





