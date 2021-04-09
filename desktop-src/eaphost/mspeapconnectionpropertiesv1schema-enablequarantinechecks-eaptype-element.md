---
title: Enablequarantäne inechecks (eaptype)-Element
description: Erfahren Sie mehr über das enablequarantäne inechecks (eaptype)-Element. Dieses Element gibt an, ob NAP-Überprüfungen (Netzwerk Zugriffsschutz) durchgeführt werden sollen.
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Enablequarantäne-Element EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949133"
---
# <a name="enablequarantinechecks-eaptype-element"></a><span data-ttu-id="e87d2-105">Enablequarantäne inechecks (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="e87d2-105">EnableQuarantineChecks (EapType) Element</span></span>

<span data-ttu-id="e87d2-106">Das **enablequarantäne inechecks (eaptype)** -Element gibt an, ob Netzwerk Zugriffsschutz (NAP)-Überprüfungen durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e87d2-106">The **EnableQuarantineChecks (EapType)** element indicates whether to perform Network Access Protection (NAP) checks.</span></span>

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

<span data-ttu-id="e87d2-107">Das **enablequarantäne inechecks** -Element wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="e87d2-107">The **EnableQuarantineChecks** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e87d2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e87d2-108">Remarks</span></span>

<span data-ttu-id="e87d2-109">Wenn das **enablequarantäne** -Element auf "true" festgestellt wird, werden NAP-Überprüfungen durchgeführt. bei "false" werden keine NAP-Überprüfungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e87d2-109">If the **EnableQuarantineChecks** element is TRUE, then PEAP will perform NAP checks; if FALSE, PEAP will not perform NAP checks.</span></span> <span data-ttu-id="e87d2-110">Das **enablequarantäne inechecks** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e87d2-110">The **EnableQuarantineChecks** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e87d2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e87d2-111">Requirements</span></span>



| <span data-ttu-id="e87d2-112">Role</span><span class="sxs-lookup"><span data-stu-id="e87d2-112">Role</span></span> | <span data-ttu-id="e87d2-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="e87d2-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="e87d2-114">Client</span><span class="sxs-lookup"><span data-stu-id="e87d2-114">Client</span></span><br/> | <span data-ttu-id="e87d2-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e87d2-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e87d2-116">Server</span><span class="sxs-lookup"><span data-stu-id="e87d2-116">Server</span></span><br/> | <span data-ttu-id="e87d2-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e87d2-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e87d2-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e87d2-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e87d2-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="e87d2-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e87d2-120">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="e87d2-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="e87d2-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="e87d2-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e87d2-122">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="e87d2-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="e87d2-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e87d2-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="e87d2-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="e87d2-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="e87d2-125">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="e87d2-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="e87d2-126">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="e87d2-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





