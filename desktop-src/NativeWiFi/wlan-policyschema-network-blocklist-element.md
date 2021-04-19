---
description: Definiert ein blockiertes Netzwerk.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Network (blocklist)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352728"
---
# <a name="network-blocklist-element"></a><span data-ttu-id="bcf4b-103">Network (blocklist)-Element</span><span class="sxs-lookup"><span data-stu-id="bcf4b-103">network (blockList) Element</span></span>

<span data-ttu-id="bcf4b-104">Das Network (blocklist)-Element definiert ein blockiertes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="bcf4b-104">The network (blockList) element defines a blocked network.</span></span> <span data-ttu-id="bcf4b-105">Ein Computer kann keine Verbindung mit einem blockierten Netzwerk herstellen.</span><span class="sxs-lookup"><span data-stu-id="bcf4b-105">A machine cannot connect to a blocked network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="bcf4b-106">Das **Network** -Element wird durch das [**Block List**](wlan-policyschema-blocklist-networkfilter-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="bcf4b-106">The **network** element is defined by the [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf4b-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcf4b-107">Requirements</span></span>



| <span data-ttu-id="bcf4b-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcf4b-108">Requirement</span></span> | <span data-ttu-id="bcf4b-109">Wert</span><span class="sxs-lookup"><span data-stu-id="bcf4b-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bcf4b-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bcf4b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf4b-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcf4b-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bcf4b-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bcf4b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf4b-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcf4b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcf4b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcf4b-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="bcf4b-115">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="bcf4b-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bcf4b-116">**Blocklisten**</span><span class="sxs-lookup"><span data-stu-id="bcf4b-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="bcf4b-117">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="bcf4b-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bcf4b-118">**blocklist (NetworkFilter)**</span><span class="sxs-lookup"><span data-stu-id="bcf4b-118">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




