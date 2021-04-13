---
title: Requirecryptobinding (eaptype)-Element
description: Gibt an, ob die Authentifizierung mit Servern durch die kryptobindung unterstützt wird.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Requirecryptobinding-Element EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392125"
---
# <a name="requirecryptobinding-eaptype-element"></a><span data-ttu-id="4350b-104">Requirecryptobinding (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="4350b-104">RequireCryptoBinding (EapType) Element</span></span>

<span data-ttu-id="4350b-105">Das Element **requirecryptobinding (eaptype)** gibt an, ob die Authentifizierung mit Servern durch die kryptobindung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4350b-105">The **RequireCryptoBinding (EapType)** element indicates whether to authenticate with servers that support cryptobinding.</span></span>

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

<span data-ttu-id="4350b-106">Das Element " **requirecryptobinding** " wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="4350b-106">The **RequireCryptoBinding** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4350b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4350b-107">Remarks</span></span>

<span data-ttu-id="4350b-108">Wenn das Element " **requirecryptobinding** " den Wert "true" hat, wird die Authentifizierung mit Servern durchführt, die cryptobinding nicht unterstützen. Wenn der Wert false ist, wird die Authentifizierung nur bei Servern durchführt, die cryptobinding unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4350b-108">If the **RequireCryptoBinding** element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="4350b-109">Das Element " **requirecryptobinding** " ist optional.</span><span class="sxs-lookup"><span data-stu-id="4350b-109">The **RequireCryptoBinding** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4350b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4350b-110">Requirements</span></span>



| <span data-ttu-id="4350b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4350b-111">Requirement</span></span> | <span data-ttu-id="4350b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4350b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4350b-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4350b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4350b-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4350b-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4350b-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4350b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4350b-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4350b-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4350b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4350b-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="4350b-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="4350b-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4350b-119">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="4350b-119">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="4350b-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="4350b-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4350b-121">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="4350b-121">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="4350b-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4350b-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="4350b-123">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="4350b-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4350b-124">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="4350b-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4350b-125">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="4350b-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





