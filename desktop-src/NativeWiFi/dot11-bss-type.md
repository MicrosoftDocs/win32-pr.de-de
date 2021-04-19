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
# <a name="dot11_bss_type-enumeration"></a>DOT11 \_ BSS- \_ Typenumeration

Der enumerierte Typ **DOT11 \_ BSS \_** definiert einen grundlegenden Service Set (BSS)-Netzwerktyp.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**Dot11 \_ BSS \_ - \_ typinfrastruktur**
</dt> <dd>

Gibt ein Infrastruktur-BSS-Netzwerk an.

</dd> <dt>

<span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**Dot11 \_ BSS- \_ Typ \_ unabhängig**
</dt> <dd>

Gibt ein unabhängiges BSS (IBSS)-Netzwerk an.

</dd> <dt>

<span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**Dot11 \_ BSS- \_ Typ \_ beliebig**
</dt> <dd>

Gibt entweder eine Infrastruktur oder ein IBSS-Netzwerk an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                        |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes. h (Include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WLAN- \_ BSS- \_ Eintrag**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[**WLAN- \_ Verbindungs \_ Parameter**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**Wlangetnetworkbsslist**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




