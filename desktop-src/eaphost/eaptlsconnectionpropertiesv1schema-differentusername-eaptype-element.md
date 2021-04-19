---
title: Differentusername (eaptype)-Element
description: Erfahren Sie mehr über das differenentusername (eaptype)-Element. Dieses Element bestimmt, welcher Benutzername von EAP-TLS verwendet werden soll.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Differentusername-Element EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341749"
---
# <a name="differentusername-eaptype-element"></a><span data-ttu-id="823ed-105">Differentusername (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="823ed-105">DifferentUsername (EapType) Element</span></span>

<span data-ttu-id="823ed-106">Das **differenentusername (eaptype)** -Element bestimmt, welcher Benutzername von EAP-TLS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="823ed-106">The **DifferentUsername (EapType)** element determines which user name EAP-TLS is to use.</span></span>

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

<span data-ttu-id="823ed-107">Das **differenentusername** -Element wird durch das [**eaptype**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="823ed-107">The **DifferentUsername** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="823ed-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="823ed-108">Remarks</span></span>

<span data-ttu-id="823ed-109">Wenn das **differenentusername** -Element true ist, sollte EAP-TLS einen anderen Benutzernamen als den Namen verwenden, der im Zertifikat angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823ed-109">If the **DifferentUserName** element is TRUE, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="823ed-110">Wenn das **differenentusername** -Element false ist, verwendet EAP-TLS den Benutzernamen, der im Zertifikat angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="823ed-110">If the **DifferentUserName** element is FALSE, EAP-TLS uses the user name that appears on the certificate.</span></span>

<span data-ttu-id="823ed-111">Das **differenentusername** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="823ed-111">The **DifferentUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="823ed-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="823ed-112">Requirements</span></span>



| <span data-ttu-id="823ed-113">Role</span><span class="sxs-lookup"><span data-stu-id="823ed-113">Role</span></span> | <span data-ttu-id="823ed-114">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="823ed-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="823ed-115">Client</span><span class="sxs-lookup"><span data-stu-id="823ed-115">Client</span></span><br/> | <span data-ttu-id="823ed-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="823ed-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="823ed-117">Server</span><span class="sxs-lookup"><span data-stu-id="823ed-117">Server</span></span><br/> | <span data-ttu-id="823ed-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="823ed-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="823ed-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="823ed-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="823ed-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="823ed-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="823ed-121">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="823ed-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="823ed-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="823ed-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="823ed-123">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="823ed-123">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="823ed-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="823ed-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="823ed-125">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="823ed-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="823ed-126">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="823ed-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="823ed-127">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="823ed-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





