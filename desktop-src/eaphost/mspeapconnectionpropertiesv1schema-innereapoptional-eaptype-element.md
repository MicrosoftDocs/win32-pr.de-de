---
title: Innereapoptional (eaptype)-Element
description: Erfahren Sie mehr über das innereapoptional (eaptype)-Element. Dieses Element gibt an, ob Gast Zugriff durchgeführt werden soll.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Innereapoptional-Element EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102334"
---
# <a name="innereapoptional-eaptype-element"></a><span data-ttu-id="38c93-105">Innereapoptional (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="38c93-105">InnerEapOptional (EapType) Element</span></span>

<span data-ttu-id="38c93-106">Das **innereapoptional (eaptype)** -Element gibt an, ob Gast Zugriff durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38c93-106">The **InnerEapOptional (EapType)** element indicates whether to perform GUEST access.</span></span>

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

<span data-ttu-id="38c93-107">Das **innereapoptional** -Element wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="38c93-107">The **InnerEapOptional** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c93-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38c93-108">Remarks</span></span>

<span data-ttu-id="38c93-109">Wenn das **innereapoptional** -Element true ist, muss das [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) -Element vorhanden sein und die innere Methode und die Konfiguration beschreiben. Wenn der Wert false ist, führt der Peer-Agent den Gast Zugriff aus.</span><span class="sxs-lookup"><span data-stu-id="38c93-109">If the **InnerEapOptional** element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and it's configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="38c93-110">Das **innereapoptional** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="38c93-110">The **InnerEapOptional** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c93-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38c93-111">Requirements</span></span>



| <span data-ttu-id="38c93-112">Role</span><span class="sxs-lookup"><span data-stu-id="38c93-112">Role</span></span> | <span data-ttu-id="38c93-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="38c93-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="38c93-114">Client</span><span class="sxs-lookup"><span data-stu-id="38c93-114">Client</span></span><br/> | <span data-ttu-id="38c93-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38c93-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38c93-116">Server</span><span class="sxs-lookup"><span data-stu-id="38c93-116">Server</span></span><br/> | <span data-ttu-id="38c93-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38c93-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38c93-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38c93-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="38c93-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="38c93-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="38c93-120">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="38c93-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="38c93-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="38c93-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="38c93-122">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="38c93-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="38c93-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="38c93-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="38c93-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="38c93-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="38c93-125">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="38c93-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="38c93-126">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="38c93-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





