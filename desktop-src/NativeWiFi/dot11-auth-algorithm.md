---
description: Definiert einen WLAN-Authentifizierungsalgorithmus.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: DOT11_AUTH_ALGORITHM -Enumeration (Wlantypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 774b2218a451f4cbaa85e6b77559c0d5761b0b132ebdf9d3f11c15ea6658e7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798470"
---
# <a name="dot11_auth_algorithm-enumeration"></a>DOT11 \_ AUTH \_ ALGORITHM-Enumeration

Der **aufzählte TYP DOT11 \_ AUTH \_ ALGORITHM** definiert einen WLAN-Authentifizierungsalgorithmus.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ OPEN**
</dt> <dd>

Gibt einen IEEE 802.11 Open System-Authentifizierungsalgorithmus an.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11 \_ AUTH \_ ALGO \_ 80211 \_ SHARED \_ KEY**
</dt> <dd>

Gibt einen 802.11-Authentifizierungsalgorithmus mit gemeinsam verwendeten Schlüsseln an, der die Verwendung eines vorinstallierten WEP-Schlüssels (Wired Equivalent Privacy) für die 802.11-Authentifizierung erfordert.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA**
</dt> <dd>

Gibt einen Wi-Fi WPA-Algorithmus (Protected Access) an. Die IEEE 802.1X-Portauthentifizierung wird vom Supplicant-, Authenticator- und Authentifizierungsserver ausgeführt. Verschlüsselungsschlüssel werden dynamisch durch den Authentifizierungsprozess abgeleitet.

Dieser Algorithmus ist nur für BSS-Typen der \_ Dot11-BSS-Typinfrastruktur \_ \_ gültig.

Wenn der WPA-Algorithmus aktiviert ist, wird die Station 802.11 nur einem Zugriffspunkt zuordnen, dessen Beacon- oder Testantworten die Authentifizierungssammlung vom Typ 1 (802.1X) innerhalb des WPA-Informationselements (IE) enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ PSK**
</dt> <dd>

Gibt einen WPA-Algorithmus an, der vorinstallierte Schlüssel (Preshared Keys, PSK) verwendet. Die IEEE 802.1X-Portauthentifizierung wird vom Supplicant und authenticator ausgeführt. Verschlüsselungsschlüssel werden dynamisch durch einen vorinstallierten Schlüssel abgeleitet, der sowohl für den Supplicant als auch für den Authentator verwendet wird.

Dieser Algorithmus ist nur für BSS-Typen der **Dot11-BSS-Typinfrastruktur \_ \_ \_ gültig.**

Wenn der WPA PSK-Algorithmus aktiviert ist, wird die Station 802.11 nur einem Zugriffspunkt zuordnen, dessen Beacon- oder Testantworten die Authentifizierungssammlung vom Typ 2 (vorinstallierte Schlüssel) innerhalb der WPA-IE enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ AUTH \_ ALGO \_ WPA \_ NONE**
</dt> <dd>

Dieser Wert wird nicht unterstützt.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA**
</dt> <dd>

Gibt einen RSNA-Algorithmus (802.11i Robust Security Network Association) an. WPA2 ist ein solcher Algorithmus. Die IEEE 802.1X-Portauthentifizierung wird vom Supplicant-, Authenticator- und Authentifizierungsserver ausgeführt. Verschlüsselungsschlüssel werden dynamisch durch den Authentifizierungsprozess abgeleitet.

Dieser Algorithmus ist nur für BSS-Typen der **Dot11-BSS-Typinfrastruktur \_ \_ \_ gültig.**

Wenn der RSNA-Algorithmus aktiviert ist, wird die Station 802.11 nur einem Zugriffspunkt zuordnen, dessen Beacon- oder Testantworten die Authentifizierungssammlung vom Typ 1 (802.1X) innerhalb der RSN-IE enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ AUTH \_ ALGO \_ RSNA \_ PSK**
</dt> <dd>

Gibt einen 802.11i RSNA-Algorithmus an, der PSK verwendet. Die IEEE 802.1X-Portauthentifizierung wird vom Supplicant und authenticator ausgeführt. Verschlüsselungsschlüssel werden dynamisch durch einen vorinstallierten Schlüssel abgeleitet, der sowohl für den Supplicant als auch für den Authentator verwendet wird.

Dieser Algorithmus ist nur für BSS-Typen der **Dot11-BSS-Typinfrastruktur \_ \_ \_ gültig.**

Wenn der RSNA PSK-Algorithmus aktiviert ist, wird die Station 802.11 nur einem Zugriffspunkt zuordnen, dessen Beacon- oder Testantworten die Authentifizierungssammlung des Typs 2 (vorinstallierte Schlüssel) innerhalb der RSN-IE enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ START**
</dt> <dd>

Gibt den Anfang des Bereichs an, der proprietäre Authentifizierungsalgorithmen angibt, die von einer IHV entwickelt werden.

Der **DOT11 \_ AUTH \_ ALGO \_ IHV START-Enumerator \_** ist nur gültig, wenn der Miniporttreiber im ExtSTA-Modus (Extensible Station) ausgeführt wird.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ AUTH \_ ALGO \_ IHV \_ END**
</dt> <dd>

Gibt das Ende des Bereichs an, der proprietäre Authentifizierungsalgorithmen angibt, die von einer IHV entwickelt werden.

Der **DOT11 \_ AUTH \_ ALGO \_ IHV END-Enumerator \_** ist nur gültig, wenn der Miniporttreiber im ExtSTA-Modus ausgeführt wird.

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

[**\_DOT11-AUTH-VERSCHLÜSSELUNGSPAAR \_ \_**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**VERFÜGBARES \_ \_ WLAN-NETZWERK**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**\_ \_ WLAN-SICHERHEITSATTRIBUTE**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




