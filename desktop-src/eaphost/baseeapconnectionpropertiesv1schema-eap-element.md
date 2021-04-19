---
title: EAP-Element (Verbindungs Eigenschaften)
description: Erfahren Sie mehr über das EAP-Element. Dieses Element erfasst den ausgewählten Methodentyp und die Methoden spezifische Konfiguration. | EAP-Element (Verbindungs Eigenschaften)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- EAP-Element EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357185"
---
# <a name="eap-element-connection-properties"></a><span data-ttu-id="4a497-106">EAP-Element (Verbindungs Eigenschaften)</span><span class="sxs-lookup"><span data-stu-id="4a497-106">Eap Element (connection properties)</span></span>

<span data-ttu-id="4a497-107">Das **EAP** -Element erfasst den ausgewählten Methodentyp und die Methoden spezifische Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4a497-107">The **Eap** element captures the method type selected and method-specific configuration.</span></span>

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a><span data-ttu-id="4a497-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a497-108">Remarks</span></span>

<span data-ttu-id="4a497-109">Die-Methode kann die konstituierenden Elemente innerhalb des **EAP** -Elements definieren.</span><span class="sxs-lookup"><span data-stu-id="4a497-109">The method can define the constituent elements inside the **Eap** element.</span></span> <span data-ttu-id="4a497-110">Die-Methode führt auch eine Schema Validierung für die Elemente in **EAP** aus.</span><span class="sxs-lookup"><span data-stu-id="4a497-110">The method also performs schema validation on the elements in **Eap**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a497-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a497-111">Requirements</span></span>



| <span data-ttu-id="4a497-112">Role</span><span class="sxs-lookup"><span data-stu-id="4a497-112">Role</span></span> | <span data-ttu-id="4a497-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="4a497-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="4a497-114">Client</span><span class="sxs-lookup"><span data-stu-id="4a497-114">Client</span></span><br/> | <span data-ttu-id="4a497-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a497-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a497-116">Server</span><span class="sxs-lookup"><span data-stu-id="4a497-116">Server</span></span><br/> | <span data-ttu-id="4a497-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a497-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a497-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a497-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a497-119">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="4a497-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4a497-120">baseeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="4a497-120">baseeapconnectionpropertiesv1 Schema</span></span>](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





