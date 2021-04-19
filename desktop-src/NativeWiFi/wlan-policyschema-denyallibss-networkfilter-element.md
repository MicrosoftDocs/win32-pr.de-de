---
description: Gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: denyallibss-Element (NetworkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350409"
---
# <a name="denyallibss-networkfilter-element"></a><span data-ttu-id="f46ba-103">denyallibss-Element (NetworkFilter)</span><span class="sxs-lookup"><span data-stu-id="f46ba-103">denyAllIBSS (networkFilter) Element</span></span>

<span data-ttu-id="f46ba-104">Das denyallibss (NetworkFilter)-Element gibt an, ob der Zugriff auf alle Ad-hoc-Netzwerke blockiert ist.</span><span class="sxs-lookup"><span data-stu-id="f46ba-104">The denyAllIBSS (networkFilter) element specifies if access to all ad-hoc networks is blocked.</span></span> <span data-ttu-id="f46ba-105">Wenn **denyallibss** den Wert true aufweist, können Computer keine Verbindung mit einem Ad-hoc-Netzwerk herstellen. Andernfalls können Computer eine Verbindung mit Ad-hoc-Netzwerken herstellen.</span><span class="sxs-lookup"><span data-stu-id="f46ba-105">When **denyAllIBSS** has a value of TRUE, machines cannot connect to an ad-hoc network; otherwise, machines may connect to ad-hoc networks.</span></span>

<span data-ttu-id="f46ba-106">Der Standardwert für dieses Element ist false.</span><span class="sxs-lookup"><span data-stu-id="f46ba-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="f46ba-107">Wenn **denyallibss** nicht in einem Profil angegeben ist, können Computer standardmäßig eine Verbindung mit Ad-hoc-Netzwerken herstellen.</span><span class="sxs-lookup"><span data-stu-id="f46ba-107">If **denyAllIBSS** is not specified in a profile, then by default machines may connect to ad-hoc networks.</span></span>

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

<span data-ttu-id="f46ba-108">Das **denyallibss** -Element wird durch das [**NetworkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="f46ba-108">The **denyAllIBSS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f46ba-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f46ba-109">Requirements</span></span>



| <span data-ttu-id="f46ba-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f46ba-110">Requirement</span></span> | <span data-ttu-id="f46ba-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f46ba-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f46ba-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f46ba-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f46ba-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f46ba-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f46ba-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f46ba-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f46ba-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f46ba-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f46ba-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f46ba-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="f46ba-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="f46ba-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f46ba-118">**Network Filter**</span><span class="sxs-lookup"><span data-stu-id="f46ba-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="f46ba-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="f46ba-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f46ba-120">**Network Filter (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="f46ba-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




