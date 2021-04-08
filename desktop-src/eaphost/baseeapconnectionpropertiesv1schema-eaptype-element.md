---
title: Eaptype-Element (V1-Schema Verbindungs Eigenschaft)
description: Erfahren Sie mehr über das eaptype-Element. Dieses Element erfasst eine Methoden spezifische Konfiguration innerhalb des EAP-Elements. | Eaptype-Element (V1-Schema Verbindungs Eigenschaft)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- Eaptype-Element EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761661"
---
# <a name="eaptype-element-v1-schema-connection-property"></a><span data-ttu-id="644d5-106">Eaptype-Element (V1-Schema Verbindungs Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="644d5-106">EapType Element (v1 schema connection property)</span></span>

<span data-ttu-id="644d5-107">Das **eaptype** -Element erfasst eine Methoden spezifische Konfiguration innerhalb des EAP-Elements.</span><span class="sxs-lookup"><span data-stu-id="644d5-107">The **EapType** element captures method-specific configuration inside the Eap element.</span></span>

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="644d5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="644d5-108">Remarks</span></span>

<span data-ttu-id="644d5-109">Das **eaptype** -Element ist abstrakt. Jede Methode muss ein abgeleitetes Element in den Instanzdokumenten definieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="644d5-109">The **EapType** element is abstract; each method must define and use a derived element in the instance documents.</span></span>

## <a name="requirements"></a><span data-ttu-id="644d5-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="644d5-110">Requirements</span></span>



| <span data-ttu-id="644d5-111">Role</span><span class="sxs-lookup"><span data-stu-id="644d5-111">Role</span></span> | <span data-ttu-id="644d5-112">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="644d5-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="644d5-113">Client</span><span class="sxs-lookup"><span data-stu-id="644d5-113">Client</span></span><br/> | <span data-ttu-id="644d5-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="644d5-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="644d5-115">Server</span><span class="sxs-lookup"><span data-stu-id="644d5-115">Server</span></span><br/> | <span data-ttu-id="644d5-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="644d5-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="644d5-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="644d5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644d5-118">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="644d5-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="644d5-119">baseeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="644d5-119">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





