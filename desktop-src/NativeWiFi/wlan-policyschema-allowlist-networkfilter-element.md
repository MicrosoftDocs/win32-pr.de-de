---
description: Gibt die Liste der Drahtlos-LAN-Netzwerke an, denen jeder Computer eine Verbindung herstellen darf.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: AllowList-Element (NetworkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344855"
---
# <a name="allowlist-networkfilter-element"></a><span data-ttu-id="eef6d-103">AllowList-Element (NetworkFilter)</span><span class="sxs-lookup"><span data-stu-id="eef6d-103">allowList (networkFilter) Element</span></span>

<span data-ttu-id="eef6d-104">Das AllowList (NetworkFilter)-Element gibt die Liste der Drahtlos-LAN-Netzwerke an, denen jeder Computer eine Verbindung herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="eef6d-104">The allowList (networkFilter) element specifies the list of wireless LAN networks to which any machine must be allowed to connect.</span></span>

``` syntax
<xs:element name="allowList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="eef6d-105">Das **AllowList** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="eef6d-105">The **allowList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="eef6d-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eef6d-106">Child elements</span></span>



| <span data-ttu-id="eef6d-107">Element</span><span class="sxs-lookup"><span data-stu-id="eef6d-107">Element</span></span>                                                        | <span data-ttu-id="eef6d-108">type</span><span class="sxs-lookup"><span data-stu-id="eef6d-108">Type</span></span>                                                                     | <span data-ttu-id="eef6d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eef6d-109">Description</span></span>                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="eef6d-110">**Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="eef6d-110">**network**</span></span>](wlan-policyschema-network-allowlist-element.md) | [<span data-ttu-id="eef6d-111">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="eef6d-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="eef6d-112">Das Netzwerk, mit dem der Computer eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="eef6d-112">The network to which the machine can connect.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eef6d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eef6d-113">Requirements</span></span>



| <span data-ttu-id="eef6d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eef6d-114">Requirement</span></span> | <span data-ttu-id="eef6d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="eef6d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eef6d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eef6d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eef6d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eef6d-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eef6d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eef6d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eef6d-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eef6d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eef6d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eef6d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="eef6d-121">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="eef6d-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="eef6d-122">**Network Filter**</span><span class="sxs-lookup"><span data-stu-id="eef6d-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="eef6d-123">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="eef6d-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="eef6d-124">**Network Filter (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="eef6d-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




