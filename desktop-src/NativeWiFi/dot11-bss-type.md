---
description: Definiert einen BSS-Netzwerktyp (Basic Service Set).
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: DOT11_BSS_TYPE-Enumeration (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356228"
---
# <a name="dot11_bss_type-enumeration"></a><span data-ttu-id="cf994-103">DOT11 \_ BSS- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="cf994-103">DOT11\_BSS\_TYPE enumeration</span></span>

<span data-ttu-id="cf994-104">Der enumerierte Typ **DOT11 \_ BSS \_** definiert einen grundlegenden Service Set (BSS)-Netzwerktyp.</span><span class="sxs-lookup"><span data-stu-id="cf994-104">The **DOT11\_BSS\_TYPE** enumerated type defines a basic service set (BSS) network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf994-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf994-105">Syntax</span></span>


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="cf994-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="cf994-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cf994-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**Dot11 \_ BSS \_ - \_ typinfrastruktur**</span><span class="sxs-lookup"><span data-stu-id="cf994-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11\_BSS\_type\_infrastructure**</span></span>
</dt> <dd>

<span data-ttu-id="cf994-108">Gibt ein Infrastruktur-BSS-Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="cf994-108">Specifies an infrastructure BSS network.</span></span>

</dd> <dt>

<span data-ttu-id="cf994-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**Dot11 \_ BSS- \_ Typ \_ unabhängig**</span><span class="sxs-lookup"><span data-stu-id="cf994-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11\_BSS\_type\_independent**</span></span>
</dt> <dd>

<span data-ttu-id="cf994-110">Gibt ein unabhängiges BSS (IBSS)-Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="cf994-110">Specifies an independent BSS (IBSS) network.</span></span>

</dd> <dt>

<span data-ttu-id="cf994-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**Dot11 \_ BSS- \_ Typ \_ beliebig**</span><span class="sxs-lookup"><span data-stu-id="cf994-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11\_BSS\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="cf994-112">Gibt entweder eine Infrastruktur oder ein IBSS-Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="cf994-112">Specifies either infrastructure or IBSS network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf994-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf994-113">Requirements</span></span>



| <span data-ttu-id="cf994-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf994-114">Requirement</span></span> | <span data-ttu-id="cf994-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cf994-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf994-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf994-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf994-117">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf994-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cf994-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf994-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf994-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf994-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="cf994-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cf994-120">Redistributable</span></span><br/>          | <span data-ttu-id="cf994-121">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="cf994-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="cf994-122">Header</span><span class="sxs-lookup"><span data-stu-id="cf994-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf994-123"><dt>Wlantypes. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf994-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf994-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf994-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf994-125">**WLAN- \_ BSS- \_ Eintrag**</span><span class="sxs-lookup"><span data-stu-id="cf994-125">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[<span data-ttu-id="cf994-126">**WLAN- \_ Verbindungs \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="cf994-126">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="cf994-127">**Wlangetnetworkbsslist**</span><span class="sxs-lookup"><span data-stu-id="cf994-127">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




