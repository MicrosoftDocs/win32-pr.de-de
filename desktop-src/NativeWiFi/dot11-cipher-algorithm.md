---
description: Definiert einen Verschlüsselungsalgorithmus für die Verschlüsselung und Entschlüsselung von Daten.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: DOT11_CIPHER_ALGORITHM-Enumeration (wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349297"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>DOT11 \_ Chiffre \_ Algorithmus-Enumeration

Der Enumerationstyp **DOT11 \_ Verschlüsselungs \_ Algorithmus** definiert einen Verschlüsselungsalgorithmus für die Verschlüsselung und Entschlüsselung von Daten.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ Cipher \_ algo \_ None**
</dt> <dd>

Gibt an, dass kein Verschlüsselungsalgorithmus aktiviert oder unterstützt wird.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ Cipher \_ algo \_ WEP40**
</dt> <dd>

Gibt einen drahtlosen WEP-Algorithmus (Wired Equivalent Privacy) an, bei dem es sich um den RC4-basierten Algorithmus handelt, der im 802.11-1999-Standard angegeben ist. Dieser Enumerator gibt den WEP-Verschlüsselungsalgorithmus mit einem 40-Bit-Chiffre Schlüssel an.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11 \_ Cipher \_ algo \_ TKIP**
</dt> <dd>

Gibt einen TKIP-Algorithmus (Temporal Key Integrity Protocol) an, bei dem es sich um die RC4-basierte Verschlüsselungs Sammlung handelt, die auf den in der WPA-Spezifikation definierten Algorithmen und dem IEEE 802.11 i-2004-Standard basiert. Diese Chiffre verwendet auch den "Michael Message Integrity Code (MIC)"-Algorithmus für den Fälschungsschutz.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ Cipher \_ algo \_ CCMP**
</dt> <dd>

Gibt einen AES-CCMP-Algorithmus an, wie im IEEE 802.11 i-2004-Standard und in RFC 3610 angegeben. Advanced Encryption Standard (AES) ist der Verschlüsselungsalgorithmus, der in der "fps pub 197" definiert ist.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ Cipher \_ algo \_ WEP104**
</dt> <dd>

Gibt einen WEP-Verschlüsselungsalgorithmus mit einem 104-Bit-Chiffre Schlüssel an.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ Cipher \_ algo \_ WPA \_ - \_ Gruppe verwenden**
</dt> <dd>

Gibt einen Wi-Fi geschützten Zugriff (WPA) Gruppenschlüssel Verschlüsselungs Sammlung verwenden. Weitere Informationen zur Verwendung von Group Key Verschlüsselungs Suite finden Sie Unterklausel 7.3.2.25.1 of the IEEE 802.11 i-2004 Standard.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ Cipher \_ algo- \_ RSN- \_ Verwendungs \_ Gruppe**
</dt> <dd>

Gibt ein stabiles Sicherheitsnetzwerk (RSN) mit Gruppenschlüssel Verschlüsselungs Sammlung an. Weitere Informationen zur Verwendung von Group Key Verschlüsselungs Suite finden Sie Unterklausel 7.3.2.25.1 of the IEEE 802.11 i-2004 Standard.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ Cipher \_ algo \_ WEP**
</dt> <dd>

Gibt einen WEP-Chiffre Algorithmus mit einem Verschlüsselungsschlüssel beliebiger Länge an.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ Cipher \_ algo \_ IHV \_ starten**
</dt> <dd>

Gibt den Anfang des Bereichs an, der verwendet wird, um proprietäre Verschlüsselungsalgorithmen zu definieren, die von einem unabhängigen Hardwarehersteller (IHV) entwickelt werden.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ Cipher \_ algo \_ IHV \_ Ende**
</dt> <dd>

Gibt das Ende des Bereichs an, der verwendet wird, um proprietäre Verschlüsselungsalgorithmen zu definieren, die von einem IHV entwickelt werden.

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

 

 




