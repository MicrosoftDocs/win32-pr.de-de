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
# <a name="dot11_ssid-structure"></a>DOT11 \_ -SSID-Struktur

Eine **DOT11 \_ SSID** -Struktur enthält die SSID einer Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a>Member

<dl> <dt>

**ussidlength**
</dt> <dd>

Die Länge des **ucssid-** Arrays in Bytes.

</dd> <dt>

**ucssid**
</dt> <dd>

Die SSID. \_ \_ Die maximale Länge von DOT11 SSID \_ ist auf 32 festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die vom **ucssid-** Member angegebene SSID ist keine NULL-terminierte ASCII-Zeichenfolge. Die Länge der SSID wird durch das Element " **ussidlength** " bestimmt.

Eine Platzhalter-SSID ist eine SSID, deren " **ussidlength** "-Member auf NULL festgelegt ist. Wenn die gewünschte SSID auf die Platzhalter-SSID festgelegt ist, kann die 802,11-Station eine Verbindung mit einem beliebigen Basic Service Set (BSS)-Netzwerk herstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                        |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes. h (Include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WLAN- \_ Verbindungs \_ Parameter**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**Wlangetnetworkbsslist**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[**Wlanscan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




