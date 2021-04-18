---
title: Treuhändrootca (servervalidationparameters)-Element-Verbindung
description: Erfasst den Fingerabdruck der Stamm Zertifizierungsstellen, die vom Client als vertrauenswürdig eingestuft werden. | Treuhändrootca-Element (servervalidationparameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
keywords:
- Treuhändrootca-Element EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106364403"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a><span data-ttu-id="e7d86-105">Treuhänder-Element (servervalidationparameters) für Verbindungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e7d86-105">TrustedRootCA (ServerValidationParameters) Element for connection properties</span></span>

<span data-ttu-id="e7d86-106">Das Element " **Treuhänder" (servervalidationparameters)** erfasst den Fingerabdruck der Stamm Zertifizierungsstellen, die vom Client als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="e7d86-106">The **TrustedRootCA (ServerValidationParameters)** element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="e7d86-107">Das Element " **treuhändrootca** " wird durch den komplexen [**servervalidationparameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="e7d86-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d86-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7d86-108">Remarks</span></span>

<span data-ttu-id="e7d86-109">Der Thumb-Abdruck ist eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="e7d86-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="e7d86-110">Das Element " **treuhändrootca** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7d86-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d86-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7d86-111">Requirements</span></span>



| <span data-ttu-id="e7d86-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7d86-112">Requirement</span></span> | <span data-ttu-id="e7d86-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e7d86-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7d86-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7d86-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e7d86-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7d86-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7d86-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7d86-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e7d86-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7d86-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7d86-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7d86-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7d86-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="e7d86-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e7d86-120">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="e7d86-120">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="e7d86-121">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="e7d86-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e7d86-122">**ServerValidation (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="e7d86-122">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="e7d86-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e7d86-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e7d86-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="e7d86-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e7d86-125">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="e7d86-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e7d86-126">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="e7d86-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





