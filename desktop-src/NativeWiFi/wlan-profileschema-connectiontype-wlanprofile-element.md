---
description: Gibt den Betriebsmodus des Netzwerks an.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: connectionType (wlanprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1e7b456260c656ebb3d64b6a3732fe97ca3ca488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863348"
---
# <a name="connectiontype-wlanprofile-element"></a><span data-ttu-id="d6a37-103">connectionType (wlanprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="d6a37-103">connectionType (WLANProfile) Element</span></span>

<span data-ttu-id="d6a37-104">Das connectionType (wlanprofile)-Element gibt den Betriebsmodus des Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="d6a37-104">The connectionType (WLANProfile) element indicates the operating mode of the network.</span></span>

<span data-ttu-id="d6a37-105">Der Wert **ESS** gibt ein Infrastrukturnetzwerk an, während **IBSS** ein Ad-hoc-Netzwerk angibt.</span><span class="sxs-lookup"><span data-stu-id="d6a37-105">A value of **ESS** indicates an infrastructure network, while **IBSS** indicates an ad-hoc network.</span></span>

``` syntax
<xs:element name="connectionType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="IBSS"
             />
            <xs:enumeration
                value="ESS"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="d6a37-106">Das **connectionType** -Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="d6a37-106">The **connectionType** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d6a37-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6a37-107">Examples</span></span>

<span data-ttu-id="d6a37-108">Beispiel Profile, die das **connectionType** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d6a37-108">To view sample profiles that use the **connectionType** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6a37-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6a37-109">Requirements</span></span>



| <span data-ttu-id="d6a37-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6a37-110">Requirement</span></span> | <span data-ttu-id="d6a37-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d6a37-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d6a37-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6a37-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a37-113">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6a37-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6a37-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6a37-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a37-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6a37-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d6a37-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d6a37-116">Redistributable</span></span><br/>          | <span data-ttu-id="d6a37-117">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="d6a37-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d6a37-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6a37-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6a37-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d6a37-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d6a37-120">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d6a37-120">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d6a37-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="d6a37-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d6a37-122">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d6a37-122">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




