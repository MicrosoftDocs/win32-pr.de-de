---
description: Gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: denyalless (NetworkFilter)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214519"
---
# <a name="denyalless-networkfilter-element"></a><span data-ttu-id="bc39d-103">denyalless (NetworkFilter)-Element</span><span class="sxs-lookup"><span data-stu-id="bc39d-103">denyAllESS (networkFilter) Element</span></span>

<span data-ttu-id="bc39d-104">Das denyalless (NetworkFilter)-Element gibt an, ob der Zugriff auf alle Infrastruktur Netzwerke blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="bc39d-104">The denyAllESS (networkFilter) element specifies if access to all infrastructure networks is blocked.</span></span> <span data-ttu-id="bc39d-105">Wenn **denyalless** den Wert true aufweist, können Computer keine Verbindung mit einem Infrastrukturnetzwerk herstellen. Andernfalls können Computer Verbindungen mit Infrastruktur Netzwerken herstellen.</span><span class="sxs-lookup"><span data-stu-id="bc39d-105">When **denyAllESS** has a value of TRUE, machines cannot connect to an infrastructure network; otherwise, machines may connect to infrastructure networks.</span></span>

<span data-ttu-id="bc39d-106">Der Standardwert für dieses Element ist false.</span><span class="sxs-lookup"><span data-stu-id="bc39d-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="bc39d-107">Wenn **denyalless** nicht in einem Profil angegeben ist, können Computer standardmäßig eine Verbindung mit Infrastruktur Netzwerken herstellen.</span><span class="sxs-lookup"><span data-stu-id="bc39d-107">If **denyAllESS** is not specified in a profile, then by default machines may connect to infrastructure networks.</span></span>

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

<span data-ttu-id="bc39d-108">Das **denyalless** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="bc39d-108">The **denyAllESS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc39d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc39d-109">Requirements</span></span>



| <span data-ttu-id="bc39d-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc39d-110">Requirement</span></span> | <span data-ttu-id="bc39d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="bc39d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc39d-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc39d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="bc39d-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc39d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc39d-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc39d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="bc39d-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc39d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc39d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc39d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc39d-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="bc39d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bc39d-118">**Network Filter**</span><span class="sxs-lookup"><span data-stu-id="bc39d-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="bc39d-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="bc39d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bc39d-120">**Network Filter (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="bc39d-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




