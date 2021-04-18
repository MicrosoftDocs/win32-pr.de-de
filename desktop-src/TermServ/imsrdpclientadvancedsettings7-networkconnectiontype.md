---
title: IMsRdpClientAdvancedSettings7 networkconnectiontype (Eigenschaft)
description: Ruft den Typ der Netzwerkverbindung ab, die zwischen Client und Server verwendet wird, oder legt ihn fest. Die an den Server weiter gegebenen Informationen zum Netzwerk Verbindungstyp helfen dem Server beim Optimieren mehrerer Parameter basierend auf dem Netzwerk Verbindungstyp.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Networkconnectiontype-Eigenschaft Remotedesktopdienste
- Networkconnectiontype-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, networkconnectiontype-Eigenschaft
- Networkconnectiontype-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, networkconnectiontype-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338745"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a><span data-ttu-id="ba7dc-109">IMsRdpClientAdvancedSettings7:: networkconnectiontype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-109">IMsRdpClientAdvancedSettings7::NetworkConnectionType property</span></span>

<span data-ttu-id="ba7dc-110">Ruft den Typ der Netzwerkverbindung ab, die zwischen Client und Server verwendet wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="ba7dc-110">Gets or sets the type of network connection used between the client and server.</span></span> <span data-ttu-id="ba7dc-111">Die an den Server weiter gegebenen Informationen zum Netzwerk Verbindungstyp helfen dem Server beim Optimieren mehrerer Parameter basierend auf dem Netzwerk Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="ba7dc-111">The network connection type information passed on to the server helps the server tune several parameters based on the network connection type.</span></span>

<span data-ttu-id="ba7dc-112">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ba7dc-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7dc-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba7dc-113">Syntax</span></span>


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a><span data-ttu-id="ba7dc-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ba7dc-114">Property value</span></span>

<span data-ttu-id="ba7dc-115">Der Netzwerk Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="ba7dc-115">The network connection type.</span></span>

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span data-ttu-id="ba7dc-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Verbindung \_ \_Typmodem** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ba7dc-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION\_TYPE\_MODEM** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ba7dc-117">Modem (56 Kbit/s)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-117">Modem (56 Kbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span data-ttu-id="ba7dc-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Verbindung \_ Typ \_ Breitband \_ niedrig** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="ba7dc-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION\_TYPE\_BROADBAND\_LOW** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ba7dc-119">Breitband mit niedriger Geschwindigkeit (256 KBit/s bis 2 Mbit/s)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-119">Low-speed broadband (256 Kbps to 2 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span data-ttu-id="ba7dc-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Verbindung \_ \_Typsatellit** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="ba7dc-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION\_TYPE\_SATELLITE** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="ba7dc-121">Satellit (2 Mbit/s bis 16 Mbit/s mit hoher Latenz)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-121">Satellite (2 Mbps to 16 Mbps, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span data-ttu-id="ba7dc-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Verbindung \_ Typ \_ Breitband \_ hoch** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ba7dc-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION\_TYPE\_BROADBAND\_HIGH** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ba7dc-123">Hochgeschwindigkeitsbreitband (2 Mbit/s bis 10 Mbit/s)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-123">High-speed broadband (2 Mbps to 10 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span data-ttu-id="ba7dc-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Verbindung \_ Typ \_ WAN** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="ba7dc-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION\_TYPE\_WAN** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="ba7dc-125">WAN (Wide Area Network) (10 Mbit/s oder höher mit hoher Latenz)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-125">Wide area network (WAN) (10 Mbps or higher, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span data-ttu-id="ba7dc-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Verbindung \_ \_LAN-Typ** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="ba7dc-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION\_TYPE\_LAN** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="ba7dc-127">LAN (Local Area Network) (10 Mbit/s oder höher)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-127">Local area network (LAN) (10 Mbps or higher)</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba7dc-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba7dc-128">Requirements</span></span>



| <span data-ttu-id="ba7dc-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba7dc-129">Requirement</span></span> | <span data-ttu-id="ba7dc-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ba7dc-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7dc-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7dc-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ba7dc-132">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ba7dc-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba7dc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7dc-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ba7dc-134">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ba7dc-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ba7dc-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba7dc-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7dc-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba7dc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7dc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7dc-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7dc-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba7dc-139">IID</span><span class="sxs-lookup"><span data-stu-id="ba7dc-139">IID</span></span><br/>                      | <span data-ttu-id="ba7dc-140">IID \_ IMsRdpClientAdvancedSettings7 wird als 26036036-4010-4578-8091-0db9a1edf-C3 definiert.</span><span class="sxs-lookup"><span data-stu-id="ba7dc-140">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba7dc-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba7dc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7dc-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ba7dc-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ba7dc-143">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ba7dc-143">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





