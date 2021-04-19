---
description: Definiert ein zulässiges Netzwerk.
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: Network (AllowList)-Element
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
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373323"
---
# <a name="network-allowlist-element"></a><span data-ttu-id="91821-103">Network (AllowList)-Element</span><span class="sxs-lookup"><span data-stu-id="91821-103">network (allowList) Element</span></span>

<span data-ttu-id="91821-104">Das Network (AllowList)-Element definiert ein zulässiges Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="91821-104">The network (allowList) element defines an allowed network.</span></span> <span data-ttu-id="91821-105">Ein Computer muss eine Verbindung mit einem zulässigen Netzwerk herstellen können.</span><span class="sxs-lookup"><span data-stu-id="91821-105">A machine must be allowed to connect to an allowed network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="91821-106">Das **Network** -Element wird durch das [**AllowList**](wlan-policyschema-allowlist-networkfilter-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="91821-106">The **network** element is defined by the [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="91821-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91821-107">Requirements</span></span>



| <span data-ttu-id="91821-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91821-108">Requirement</span></span> | <span data-ttu-id="91821-109">Wert</span><span class="sxs-lookup"><span data-stu-id="91821-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91821-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91821-110">Minimum supported client</span></span><br/> | <span data-ttu-id="91821-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91821-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91821-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91821-112">Minimum supported server</span></span><br/> | <span data-ttu-id="91821-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91821-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91821-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91821-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="91821-115">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="91821-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="91821-116">**Zulassungs**</span><span class="sxs-lookup"><span data-stu-id="91821-116">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="91821-117">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="91821-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="91821-118">**AllowList (NetworkFilter)**</span><span class="sxs-lookup"><span data-stu-id="91821-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




