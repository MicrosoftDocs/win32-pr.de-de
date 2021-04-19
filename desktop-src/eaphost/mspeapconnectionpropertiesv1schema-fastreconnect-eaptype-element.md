---
title: Fastreconnect (eaptype)-Element
description: Erfahren Sie mehr über das fastreconnect (eaptype)-Element. Dieses Element gibt an, ob eine schnelle erneute Verbindungs Herstellung durchgeführt werden soll.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Fastreconnect-Element EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106342375"
---
# <a name="fastreconnect-eaptype-element"></a><span data-ttu-id="18916-105">Fastreconnect (eaptype)-Element</span><span class="sxs-lookup"><span data-stu-id="18916-105">FastReconnect (EapType) Element</span></span>

<span data-ttu-id="18916-106">Das **fastreconnect (eaptype)** -Element gibt an, ob eine schnelle erneute Verbindungs Herstellung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="18916-106">The **FastReconnect (EapType)** element indicates whether to perform a fast reconnect.</span></span>

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

<span data-ttu-id="18916-107">Das **fastreconnect** -Element wird durch das [**eaptype**](mspeapconnectionpropertiesv1schema-eaptype-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="18916-107">The **FastReconnect** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="18916-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18916-108">Remarks</span></span>

<span data-ttu-id="18916-109">Wenn das **fastreconnect** -Element "true" ist, versucht die Peer-APP, eine schnelle erneute Verbindungs Herstellung auszuführen. der Wert false gibt an, dass die vollständige Authentifizierung von Peer-App</span><span class="sxs-lookup"><span data-stu-id="18916-109">If the **FastReconnect** element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="18916-110">Das **fastreconnect** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="18916-110">The **FastReconnect** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="18916-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18916-111">Requirements</span></span>



| <span data-ttu-id="18916-112">Role</span><span class="sxs-lookup"><span data-stu-id="18916-112">Role</span></span> | <span data-ttu-id="18916-113">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="18916-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="18916-114">Client</span><span class="sxs-lookup"><span data-stu-id="18916-114">Client</span></span><br/> | <span data-ttu-id="18916-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18916-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18916-116">Server</span><span class="sxs-lookup"><span data-stu-id="18916-116">Server</span></span><br/> | <span data-ttu-id="18916-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18916-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18916-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18916-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="18916-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="18916-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="18916-120">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="18916-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="18916-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="18916-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="18916-122">**Eaptype**</span><span class="sxs-lookup"><span data-stu-id="18916-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="18916-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="18916-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="18916-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="18916-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="18916-125">mspeapconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="18916-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="18916-126">mspeapconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="18916-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





