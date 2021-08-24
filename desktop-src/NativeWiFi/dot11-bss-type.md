---
description: Definiert einen BSS-Netzwerktyp (Basic Service Set).
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: DOT11_BSS_TYPE-Enumeration (Wlantypes.h)
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
ms.openlocfilehash: 2d1c83ced842dbb876fea89271a160df2ca07fb9f02f415b13f8f1a46bc8dc79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780320"
---
# <a name="dot11_bss_type-enumeration"></a>DOT11 \_ BSS \_ TYPE-Enumeration

Der **dot11 \_ BSS TYPE-Enumerationstyp \_** definiert einen BSS-Netzwerktyp (Basic Service Set).

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

<span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11 \_ \_ BSS-Typinfrastruktur \_**
</dt> <dd>

Gibt ein BSS-Infrastrukturnetzwerk an.

</dd> <dt>

<span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11 \_ BSS \_ type \_ independent**
</dt> <dd>

Gibt ein unabhängiges BSS-Netzwerk (IBSS) an.

</dd> <dt>

<span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11 \_ BSS \_ type \_ any**
</dt> <dd>

Gibt entweder die Infrastruktur oder das IBSS-Netzwerk an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                        |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wlantypes.h (einschließlich Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_WLAN-BSS-EINTRAG \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[**\_ \_ WLAN-VERBINDUNGSPARAMETER**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[**WlanGetNetworkBssList**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




