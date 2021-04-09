---
description: Wird verwendet, um eine IEEE Media Access Control (Mac)-Adresse zu definieren.
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866040"
---
# <a name="dot11_mac_address"></a><span data-ttu-id="25e73-103">DOT11 \_ Mac- \_ Adresse</span><span class="sxs-lookup"><span data-stu-id="25e73-103">DOT11\_MAC\_ADDRESS</span></span>

<span data-ttu-id="25e73-104">Die **\_ Mac- \_ Adresstypen DOT11** werden verwendet, um eine IEEE Media Access Control (Mac)-Adresse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="25e73-104">The **DOT11\_MAC\_ADDRESS** types are used to define an IEEE media access control (MAC) address.</span></span>


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="25e73-105">**DOT11 \_ Mac- \_ Adresse \[ 6\]**</span><span class="sxs-lookup"><span data-stu-id="25e73-105">**DOT11\_MAC\_ADDRESS\[6\]**</span></span>
</dt> <dd>

<span data-ttu-id="25e73-106">Eine Mac-Adresse im Unicast-, Multicast-oder Broadcast-Format.</span><span class="sxs-lookup"><span data-stu-id="25e73-106">A MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> <dt>

<span data-ttu-id="25e73-107">**PDOT11 \_ Mac- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="25e73-107">**PDOT11\_MAC\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="25e73-108">Zeiger auf eine Mac-Adresse im Unicast-, Multicast-oder Broadcast-Format.</span><span class="sxs-lookup"><span data-stu-id="25e73-108">Pointer to a MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25e73-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25e73-109">Requirements</span></span>



| <span data-ttu-id="25e73-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25e73-110">Requirement</span></span> | <span data-ttu-id="25e73-111">Wert</span><span class="sxs-lookup"><span data-stu-id="25e73-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e73-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25e73-112">Minimum supported client</span></span><br/> | <span data-ttu-id="25e73-113">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25e73-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25e73-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25e73-114">Minimum supported server</span></span><br/> | <span data-ttu-id="25e73-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25e73-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="25e73-116">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="25e73-116">Redistributable</span></span><br/>          | <span data-ttu-id="25e73-117">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="25e73-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="25e73-118">Header</span><span class="sxs-lookup"><span data-stu-id="25e73-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e73-119"><dt>Windot11. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25e73-119"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e73-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25e73-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e73-121">**\_BSSID- \_ Liste DOT11**</span><span class="sxs-lookup"><span data-stu-id="25e73-121">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> <dt>

[<span data-ttu-id="25e73-122">**WLAN-Zuordnungs \_ \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="25e73-122">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="25e73-123">**WLAN- \_ BSS- \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="25e73-123">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




