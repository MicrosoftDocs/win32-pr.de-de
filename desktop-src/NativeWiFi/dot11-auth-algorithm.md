---
description: Definiert einen Algorithmus für die drahtlose LAN-Authentifizierung.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: DOT11_AUTH_ALGORITHM-Enumeration (wlantypes. h)
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
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349921"
---
# <a name="dot11_auth_algorithm-enumeration"></a>DOT11 \_ auth- \_ algorithmusenumeration

Der enumerierte Typ des **DOT11 \_ auth- \_ Algorithmus** definiert einen drahtlosen LAN-Authentifizierungsalgorithmus.

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

<span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ auth \_ algo \_ 80211 \_ geöffnet**
</dt> <dd>

Gibt einen IEEE 802,11-Algorithmus für die Open-System Authentifizierung an.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11 \_ auth \_ algo \_ 80211 \_ gemeinsam verwendeter \_ Schlüssel**
</dt> <dd>

Gibt einen 802,11-Algorithmus für die gemeinsame Schlüssel Authentifizierung an, der die Verwendung eines vorinstallierten WEP-Schlüssels (Wired Equivalent Privacy) für die 802,11-Authentifizierung erfordert.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11 \_ auth \_ algo \_ WPA**
</dt> <dd>

Gibt einen WPA (Wi-Fi Protected Access)-Algorithmus an. Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant-, Authenticator-und Authentifizierungsserver. Verschlüsselungsschlüssel werden dynamisch durch den Authentifizierungsprozess abgeleitet.

Dieser Algorithmus ist nur für BSS-Typen der Dot11 \_ BSS \_ - \_ typanfrastruktur gültig.

Wenn der WPA-Algorithmus aktiviert ist, wird die 802,11-Station nur mit einem Zugriffspunkt verknüpft, dessen Leucht-oder Test Antworten die Authentifizierungs Suite vom Typ 1 (802.1 x) im WPA Information-Element (IE) enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ auth \_ algo \_ WPA \_ PSK**
</dt> <dd>

Gibt einen WPA-Algorithmus an, der vorinstallierten Keys (PSK) verwendet. Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant und Authentifikator. Verschlüsselungsschlüssel werden dynamisch über einen vorinstallierten Schlüssel abgeleitet, der sowohl für den Supplicant als auch für den Authentifikator verwendet wird.

Dieser Algorithmus ist nur für BSS-Typen der **Dot11 \_ BSS \_ - \_ typanfrastruktur** gültig.

Wenn der WPA-PSK-Algorithmus aktiviert ist, ordnet die 802,11-Station nur einem Zugriffspunkt zu, dessen Kenn Wort-oder Test Antworten die Authentifizierungs Suite vom Typ 2 (vorinstallierter Schlüssel) innerhalb der WPA-IE enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ auth \_ algo \_ WPA \_ None**
</dt> <dd>

Dieser Wert wird nicht unterstützt.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11 \_ auth \_ algo- \_ RSNA**
</dt> <dd>

Gibt einen robusten 802.11 i-RSNA (Security Network Association)-Algorithmus an. WPA2 ist ein solcher Algorithmus. Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant-, Authenticator-und Authentifizierungsserver. Verschlüsselungsschlüssel werden dynamisch durch den Authentifizierungsprozess abgeleitet.

Dieser Algorithmus ist nur für BSS-Typen der **Dot11 \_ BSS \_ - \_ typanfrastruktur** gültig.

Wenn der RSNA-Algorithmus aktiviert ist, wird die 802,11-Station nur mit einem Zugriffspunkt verknüpft, dessen Leucht-oder Test Antworten die Authentifizierungs Suite vom Typ 1 (802.1 x) in der RSN IE enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ auth \_ algo- \_ RSNA- \_ PSK**
</dt> <dd>

Gibt einen 802.11 i-RSNA-Algorithmus an, der PSK verwendet. Die IEEE 802.1 x-Port Authentifizierung erfolgt durch den Supplicant und Authentifikator. Verschlüsselungsschlüssel werden dynamisch über einen vorinstallierten Schlüssel abgeleitet, der sowohl für den Supplicant als auch für den Authentifikator verwendet wird.

Dieser Algorithmus ist nur für BSS-Typen der **Dot11 \_ BSS \_ - \_ typanfrastruktur** gültig.

Wenn der RSNA-PSK-Algorithmus aktiviert ist, wird die 802,11-Station nur mit einem Zugriffspunkt verknüpft, dessen Leucht Schlag-oder Test Antworten die Authentifizierungs Suite vom Typ 2 (vorinstaltzter Schlüssel) in der RSN IE enthalten.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11 \_ auth \_ algo \_ IHV \_ starten**
</dt> <dd>

Gibt den Anfang des Bereichs an, der proprietäre Authentifizierungs Algorithmen angibt, die von einem IHV entwickelt wurden.

Der **DOT11 \_ auth \_ algo \_ IHV- \_ Start** Enumerator ist nur gültig, wenn der Mini Port-Treiber im Extensible Station (extsta)-Modus betrieben wird.

</dd> <dt>

<span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11 \_ auth \_ algo \_ IHV \_ Ende**
</dt> <dd>

Gibt das Ende des Bereichs an, der proprietäre Authentifizierungs Algorithmen angibt, die von einem IHV entwickelt wurden.

Der **DOT11 \_ auth \_ algo \_ IHV \_ End** -Enumerator ist nur gültig, wenn der Mini Port-Treiber im extsta-Modus betrieben wird.

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

[**DOT11 \_ auth- \_ Chiffre \_ paar**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**\_verfügbares WLAN- \_ Netzwerk**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**WLAN- \_ Sicherheits \_ Attribute**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




