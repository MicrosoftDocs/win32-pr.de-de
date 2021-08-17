---
description: Definiert einen Verschlüsselungsalgorithmus für die Datenverschlüsselung und -entschlüsselung.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: DOT11_CIPHER_ALGORITHM-Enumeration (Wlantypes.h)
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
ms.openlocfilehash: c99ef5b648c5503743de6f51ce7d035d75dbe1f3e5593d473a374813f4000566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780240"
---
# <a name="dot11_cipher_algorithm-enumeration"></a>DOT11 \_ CIPHER \_ ALGORITHM-Enumeration

Der **DOT11 \_ CIPHER ALGORITHM-Enumerationstyp \_** definiert einen Verschlüsselungsalgorithmus für die Datenverschlüsselung und -entschlüsselung.

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

<span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ CIPHER \_ ALGO \_ NONE**
</dt> <dd>

Gibt an, dass kein Verschlüsselungsalgorithmus aktiviert oder unterstützt wird.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP40**
</dt> <dd>

Gibt einen WEP-Algorithmus (Wired Equivalent Privacy) an, bei dem es sich um den RC4-basierten Algorithmus handelt, der im Standard 802.11-1999 angegeben ist. Dieser Enumerator gibt den WEP-Verschlüsselungsalgorithmus mit einem 40-Bit-Verschlüsselungsschlüssel an.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11 \_ CIPHER \_ ALGO \_ TKIP**
</dt> <dd>

Gibt einen TKIP-Algorithmus (Temporal Key Integrity Protocol) an, bei dem es sich um die RC4-basierte Verschlüsselungssammlung handelt, die auf den Algorithmen basiert, die in der WPA-Spezifikation und dem IEEE 802.11i-2004-Standard definiert sind. Diese Verschlüsselung verwendet auch den MIC-Algorithmus (Michael Message Integrity Code) zum Schutz vor Verfälschungen.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ CIPHER \_ ALGO \_ CCMP**
</dt> <dd>

Gibt einen AES-CCMP-Algorithmus an, wie im IEEE 802.11i-2004-Standard und RFC 3610 angegeben. Advanced Encryption Standard (AES) ist der in FIPS PUB 197 definierte Verschlüsselungsalgorithmus.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP104**
</dt> <dd>

Gibt einen WEP-Verschlüsselungsalgorithmus mit einem 104-Bit-Verschlüsselungsschlüssel an.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ WPA \_ USE \_ GROUP**
</dt> <dd>

Gibt eine Cipher Suite für den Wi-Fi geschützten Zugriff (WPA) Use Group Key an. Weitere Informationen zur Verschlüsselungssammlung "Gruppenschlüssel verwenden" finden Sie unter Klausel 7.3.2.25.1 des IEEE 802.11i-2004-Standards.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11 \_ CIPHER \_ ALGO \_ RSN \_ USE \_ GROUP**
</dt> <dd>

Gibt eine Rsn(Robust Security Network) Use Group Key Cipher Suite an. Weitere Informationen zur Verschlüsselungssammlung "Gruppenschlüssel verwenden" finden Sie unter Klausel 7.3.2.25.1 des IEEE 802.11i-2004-Standards.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11 \_ CIPHER \_ ALGO \_ WEP**
</dt> <dd>

Gibt einen WEP-Verschlüsselungsalgorithmus mit einem Verschlüsselungsschlüssel beliebiger Länge an.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ START**
</dt> <dd>

Gibt den Anfang des Bereichs an, der zum Definieren proprietärer Verschlüsselungsalgorithmen verwendet wird, die von einem unabhängigen Hardwareanbieter (IHV) entwickelt werden.

</dd> <dt>

<span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11 \_ CIPHER \_ ALGO \_ IHV \_ END**
</dt> <dd>

Gibt das Ende des Bereichs an, der zum Definieren proprietärer Verschlüsselungsalgorithmen verwendet wird, die von einer IHV entwickelt werden.

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

[**DOT11 \_ AUTH \_ CIPHER \_ PAIR**](dot11-auth-cipher-pair.md)
</dt> <dt>

[**\_VERFÜGBARES \_ WLAN-NETZWERK**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[**\_ \_ WLAN-SICHERHEITSATTRIBUTE**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




