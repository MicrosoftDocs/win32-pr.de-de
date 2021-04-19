---
title: Treuhändrootca (servervalidationparameters)-Element (v1)
description: Zeichnet den Fingerabdruck der Stamm Zertifizierungsstellen (CAS) auf, die vom Client als vertrauenswürdig eingestuft werden. | Treuhändrootca-Element (servervalidationparameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
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
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389077"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="511fd-105">Treuhändrootca-Element (servervalidationparameters)</span><span class="sxs-lookup"><span data-stu-id="511fd-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="511fd-106">Das Element " **thumbdrootca (servervalidationparameters)** " erfasst den Fingerabdruck der Stamm Zertifizierungsstellen, die vom Client als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="511fd-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="511fd-107">Das Element " **treuhändrootca** " wird durch den komplexen [**servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="511fd-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="511fd-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="511fd-108">Remarks</span></span>

<span data-ttu-id="511fd-109">Der Thumb-Abdruck ist eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="511fd-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="511fd-110">Das Element " **treuhändrootca** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="511fd-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="511fd-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="511fd-111">Requirements</span></span>



| <span data-ttu-id="511fd-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="511fd-112">Requirement</span></span> | <span data-ttu-id="511fd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="511fd-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="511fd-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="511fd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="511fd-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="511fd-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="511fd-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="511fd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="511fd-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="511fd-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="511fd-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="511fd-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="511fd-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="511fd-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="511fd-120">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="511fd-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="511fd-121">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="511fd-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="511fd-122">**ServerValidation (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="511fd-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="511fd-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="511fd-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="511fd-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="511fd-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="511fd-125">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="511fd-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="511fd-126">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="511fd-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





