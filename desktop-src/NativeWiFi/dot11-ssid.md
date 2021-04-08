---
description: Enthält die SSID einer Schnittstelle.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: DOT11_SSID Struktur (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866032"
---
# <a name="dot11_ssid-structure"></a><span data-ttu-id="372fb-103">DOT11 \_ -SSID-Struktur</span><span class="sxs-lookup"><span data-stu-id="372fb-103">DOT11\_SSID structure</span></span>

<span data-ttu-id="372fb-104">Eine **DOT11 \_ SSID** -Struktur enthält die SSID einer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="372fb-104">A **DOT11\_SSID** structure contains the SSID of an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="372fb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="372fb-105">Syntax</span></span>


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a><span data-ttu-id="372fb-106">Member</span><span class="sxs-lookup"><span data-stu-id="372fb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="372fb-107">**ussidlength**</span><span class="sxs-lookup"><span data-stu-id="372fb-107">**uSSIDLength**</span></span>
</dt> <dd>

<span data-ttu-id="372fb-108">Die Länge des **ucssid-** Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="372fb-108">The length, in bytes, of the **ucSSID** array.</span></span>

</dd> <dt>

<span data-ttu-id="372fb-109">**ucssid**</span><span class="sxs-lookup"><span data-stu-id="372fb-109">**ucSSID**</span></span>
</dt> <dd>

<span data-ttu-id="372fb-110">Die SSID.</span><span class="sxs-lookup"><span data-stu-id="372fb-110">The SSID.</span></span> <span data-ttu-id="372fb-111">\_ \_ Die maximale Länge von DOT11 SSID \_ ist auf 32 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="372fb-111">DOT11\_SSID\_MAX\_LENGTH is set to 32.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="372fb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="372fb-112">Remarks</span></span>

<span data-ttu-id="372fb-113">Die vom **ucssid-** Member angegebene SSID ist keine NULL-terminierte ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="372fb-113">The SSID that is specified by the **ucSSID** member is not a null-terminated ASCII string.</span></span> <span data-ttu-id="372fb-114">Die Länge der SSID wird durch das Element " **ussidlength** " bestimmt.</span><span class="sxs-lookup"><span data-stu-id="372fb-114">The length of the SSID is determined by the **uSSIDLength** member.</span></span>

<span data-ttu-id="372fb-115">Eine Platzhalter-SSID ist eine SSID, deren " **ussidlength** "-Member auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="372fb-115">A wildcard SSID is an SSID whose **uSSIDLength** member is set to zero.</span></span> <span data-ttu-id="372fb-116">Wenn die gewünschte SSID auf die Platzhalter-SSID festgelegt ist, kann die 802,11-Station eine Verbindung mit einem beliebigen Basic Service Set (BSS)-Netzwerk herstellen.</span><span class="sxs-lookup"><span data-stu-id="372fb-116">When the desired SSID is set to the wildcard SSID, the 802.11 station can connect to any basic service set (BSS) network.</span></span>

## <a name="requirements"></a><span data-ttu-id="372fb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="372fb-117">Requirements</span></span>



| <span data-ttu-id="372fb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="372fb-118">Requirement</span></span> | <span data-ttu-id="372fb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="372fb-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="372fb-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="372fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="372fb-121">Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="372fb-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="372fb-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="372fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="372fb-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="372fb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="372fb-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="372fb-124">Redistributable</span></span><br/>          | <span data-ttu-id="372fb-125">Drahtlose LAN-API für Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="372fb-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="372fb-126">Header</span><span class="sxs-lookup"><span data-stu-id="372fb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="372fb-127"><dt>Wlantypes. h (Include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="372fb-127"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="372fb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="372fb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="372fb-129">**WLAN- \_ Verbindungs \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="372fb-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="372fb-130">**Wlangetnetworkbsslist**</span><span class="sxs-lookup"><span data-stu-id="372fb-130">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[<span data-ttu-id="372fb-131">**Wlanscan**</span><span class="sxs-lookup"><span data-stu-id="372fb-131">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




