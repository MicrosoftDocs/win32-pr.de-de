---
description: Gibt einen Netzwerktyp an.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: NetworkType (networkitemtype)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352272"
---
# <a name="networktype-networkitemtype-element"></a><span data-ttu-id="495a7-103">NetworkType (networkitemtype)-Element</span><span class="sxs-lookup"><span data-stu-id="495a7-103">networkType (networkItemType) Element</span></span>

<span data-ttu-id="495a7-104">Das NetworkType (networkitemtype)-Element gibt einen Netzwerktyp an.</span><span class="sxs-lookup"><span data-stu-id="495a7-104">The networkType (networkItemType) element specifies a network type.</span></span> <span data-ttu-id="495a7-105">Es gibt zwei Arten von Netzwerken: Infrastruktur Netzwerke (ESS) und Ad-hoc-Netzwerke (IBSS).</span><span class="sxs-lookup"><span data-stu-id="495a7-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

<span data-ttu-id="495a7-106">Das **NetworkType** -Element wird durch den komplexen Typ [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="495a7-106">The **networkType** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="495a7-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="495a7-107">Requirements</span></span>



| <span data-ttu-id="495a7-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495a7-108">Requirement</span></span> | <span data-ttu-id="495a7-109">Wert</span><span class="sxs-lookup"><span data-stu-id="495a7-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="495a7-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="495a7-110">Minimum supported client</span></span><br/> | <span data-ttu-id="495a7-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="495a7-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="495a7-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="495a7-112">Minimum supported server</span></span><br/> | <span data-ttu-id="495a7-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="495a7-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="495a7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="495a7-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="495a7-115">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="495a7-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="495a7-116">**networkitemtype**</span><span class="sxs-lookup"><span data-stu-id="495a7-116">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="495a7-117">**Mögliche direkt übergeordnete Elemente in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="495a7-117">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="495a7-118">**Netzwerk (AllowList)**</span><span class="sxs-lookup"><span data-stu-id="495a7-118">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="495a7-119">**Netzwerk (blocklist)**</span><span class="sxs-lookup"><span data-stu-id="495a7-119">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




