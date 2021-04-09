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
# <a name="dot11_mac_address"></a>DOT11 \_ Mac- \_ Adresse

Die **\_ Mac- \_ Adresstypen DOT11** werden verwendet, um eine IEEE Media Access Control (Mac)-Adresse zu definieren.


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

**DOT11 \_ Mac- \_ Adresse \[ 6\]**
</dt> <dd>

Eine Mac-Adresse im Unicast-, Multicast-oder Broadcast-Format.

</dd> <dt>

**PDOT11 \_ Mac- \_ Adresse**
</dt> <dd>

Zeiger auf eine Mac-Adresse im Unicast-, Multicast-oder Broadcast-Format.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                       |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                                        |
| Header<br/>                   | <dl> <dt>Windot11. h (Include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_BSSID- \_ Liste DOT11**](dot11-bssid-list.md)
</dt> <dt>

[**WLAN-Zuordnungs \_ \_ Attribute**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**WLAN- \_ BSS- \_ Eintrag**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




