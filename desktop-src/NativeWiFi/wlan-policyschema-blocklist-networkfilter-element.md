---
description: Gibt die Liste der Drahtlos-LAN-Netzwerke an, mit denen ein Computer keine Verbindung herstellen darf.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: blocklist-Element (NetworkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958679"
---
# <a name="blocklist-networkfilter-element"></a><span data-ttu-id="6a006-103">blocklist-Element (NetworkFilter)</span><span class="sxs-lookup"><span data-stu-id="6a006-103">blockList (networkFilter) Element</span></span>

<span data-ttu-id="6a006-104">Das blocklist-Element (NetworkFilter) gibt die Liste der Drahtlos-LAN-Netzwerke an, mit denen ein Computer keine Verbindung herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="6a006-104">The blockList (networkFilter) element specifies the list of wireless LAN networks to which a machine must not connect.</span></span>

``` syntax
<xs:element name="blockList">
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

<span data-ttu-id="6a006-105">Das **Block List** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="6a006-105">The **blockList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6a006-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6a006-106">Child elements</span></span>



| <span data-ttu-id="6a006-107">Element</span><span class="sxs-lookup"><span data-stu-id="6a006-107">Element</span></span>                                                        | <span data-ttu-id="6a006-108">type</span><span class="sxs-lookup"><span data-stu-id="6a006-108">Type</span></span>                                                                     | <span data-ttu-id="6a006-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a006-109">Description</span></span>                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="6a006-110">**Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="6a006-110">**network**</span></span>](wlan-policyschema-network-blocklist-element.md) | [<span data-ttu-id="6a006-111">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="6a006-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="6a006-112">Das blockierte Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6a006-112">The blocked network.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="6a006-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a006-113">Requirements</span></span>



| <span data-ttu-id="6a006-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a006-114">Requirement</span></span> | <span data-ttu-id="6a006-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6a006-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a006-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a006-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a006-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a006-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a006-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a006-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a006-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a006-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a006-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a006-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a006-121">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="6a006-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6a006-122">**Network Filter**</span><span class="sxs-lookup"><span data-stu-id="6a006-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="6a006-123">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="6a006-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6a006-124">**Network Filter (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="6a006-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




