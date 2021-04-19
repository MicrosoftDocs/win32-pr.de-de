---
title: Performservervalidation (eaptype)
description: Erfahren Sie mehr über das performservervalidation-Element. Dieses Element gibt an, ob die Server Validierung ausgeführt wird. | Performservervalidation (eaptype)
ms.assetid: f6233bff-18e4-45b4-b598-839fa198f676
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
ms.openlocfilehash: 655379676bd117b89a6fe41a8d6895260e71a2bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363092"
---
# <a name="performservervalidation-eaptype"></a><span data-ttu-id="bec94-106">Performservervalidation (eaptype)</span><span class="sxs-lookup"><span data-stu-id="bec94-106">PerformServerValidation (EapType)</span></span>

<span data-ttu-id="bec94-107">Das **performservervalidation (eaptype)** -Element gibt an, ob die Server Validierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bec94-107">The **PerformServerValidation (EapType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS:PerformServerValidation "
 />
```

<span data-ttu-id="bec94-108">Das-Element wird durch das [**eaptype**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="bec94-108">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec94-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bec94-109">Remarks</span></span>

<span data-ttu-id="bec94-110">Das **performservervalidation** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="bec94-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec94-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bec94-111">Requirements</span></span>



| <span data-ttu-id="bec94-112">Role</span><span class="sxs-lookup"><span data-stu-id="bec94-112">Role</span></span> | <span data-ttu-id="bec94-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="bec94-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="bec94-114">Client</span><span class="sxs-lookup"><span data-stu-id="bec94-114">Client</span></span><br/> | <span data-ttu-id="bec94-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bec94-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bec94-116">Server</span><span class="sxs-lookup"><span data-stu-id="bec94-116">Server</span></span><br/> | <span data-ttu-id="bec94-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bec94-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bec94-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bec94-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="bec94-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="bec94-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bec94-120">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="bec94-120">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="bec94-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="bec94-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bec94-122">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="bec94-122">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="bec94-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bec94-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bec94-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="bec94-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bec94-125">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="bec94-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bec94-126">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="bec94-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bec94-127">**Performservervalidation (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="bec94-127">**PerformServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv2shema-tlsextensions-tlsextensionstype-element.md)
</dt> </dl>

 

 





