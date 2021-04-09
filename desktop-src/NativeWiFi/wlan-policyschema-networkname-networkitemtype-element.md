---
description: Gibt den Service Set Identifier (SSID) eines drahtlos Netzwerks an.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Network Name (networkitemtype)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867908"
---
# <a name="networkname-networkitemtype-element"></a><span data-ttu-id="ee74d-103">Network Name (networkitemtype)-Element</span><span class="sxs-lookup"><span data-stu-id="ee74d-103">networkName (networkItemType) Element</span></span>

<span data-ttu-id="ee74d-104">Das networkName (networkitemtype)-Element gibt den Service Set Identifier (SSID) eines drahtlos Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="ee74d-104">The networkName (networkItemType) element specifies the service set identifier (SSID) of a wireless network.</span></span>

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

<span data-ttu-id="ee74d-105">Das **networkName** -Element wird durch den komplexen Typ [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="ee74d-105">The **networkName** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee74d-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee74d-106">Requirements</span></span>



| <span data-ttu-id="ee74d-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee74d-107">Requirement</span></span> | <span data-ttu-id="ee74d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ee74d-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee74d-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee74d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="ee74d-110">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee74d-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee74d-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee74d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="ee74d-112">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee74d-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee74d-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee74d-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="ee74d-114">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="ee74d-114">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ee74d-115">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="ee74d-115">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="ee74d-116">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="ee74d-116">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ee74d-117">**Netzwerk (AllowList)**</span><span class="sxs-lookup"><span data-stu-id="ee74d-117">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="ee74d-118">**Netzwerk (blocklist)**</span><span class="sxs-lookup"><span data-stu-id="ee74d-118">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




