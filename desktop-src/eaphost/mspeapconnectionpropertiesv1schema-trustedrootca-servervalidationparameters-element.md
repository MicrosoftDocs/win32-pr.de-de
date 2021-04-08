---
title: Treuhändrootca-Element (servervalidationparameters)
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
ms.openlocfilehash: e62b691c5075f1a42f87e558a9a1f0795b90e8bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869684"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="d91b4-105">Treuhändrootca-Element (servervalidationparameters)</span><span class="sxs-lookup"><span data-stu-id="d91b4-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="d91b4-106">Das Element " **thumbdrootca (servervalidationparameters)** " erfasst den Fingerabdruck der Stamm Zertifizierungsstellen, die vom Client als vertrauenswürdig eingestuft werden.</span><span class="sxs-lookup"><span data-stu-id="d91b4-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="d91b4-107">Das Element " **treuhändrootca** " wird durch den komplexen [**servervalidationparameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="d91b4-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="d91b4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d91b4-108">Remarks</span></span>

<span data-ttu-id="d91b4-109">Der Thumb-Abdruck ist eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.</span><span class="sxs-lookup"><span data-stu-id="d91b4-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="d91b4-110">Das Element " **treuhändrootca** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="d91b4-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d91b4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d91b4-111">Requirements</span></span>



| <span data-ttu-id="d91b4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d91b4-112">Requirement</span></span> | <span data-ttu-id="d91b4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d91b4-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d91b4-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d91b4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d91b4-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d91b4-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d91b4-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d91b4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d91b4-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d91b4-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d91b4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d91b4-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="d91b4-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d91b4-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d91b4-120">**Servervalidationparameters**</span><span class="sxs-lookup"><span data-stu-id="d91b4-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="d91b4-121">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="d91b4-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d91b4-122">**ServerValidation (eaptype)**</span><span class="sxs-lookup"><span data-stu-id="d91b4-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="d91b4-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d91b4-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="d91b4-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="d91b4-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d91b4-125">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="d91b4-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d91b4-126">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="d91b4-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





