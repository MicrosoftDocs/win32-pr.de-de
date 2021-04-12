---
description: Enthält einen Netzwerkschlüssel oder eine Passphrase.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Keymaterial (sharedkey)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216221"
---
# <a name="keymaterial-sharedkey-element"></a>Keymaterial (sharedkey)-Element

Das Keymaterial (sharedkey)-Element enthält einen Netzwerkschlüssel oder eine Passphrase. Wenn das [**geschützte**](wlan-profileschema-protected-sharedkey-element.md) Element den Wert true aufweist, wird dieses Schlüsselmaterial verschlüsselt. Andernfalls ist das Schlüsselmaterial unverschlüsselt. Verschlüsseltes Schlüsselmaterial wird in hexadezimaler Form ausgedrückt.

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

Das-Element wird durch das [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Der Bereich gültiger Werte für das Keymaterial-Element variiert je nach Art der Authentifizierung und Verschlüsselung, die von den [**Authentifizierungs**](wlan-profileschema-authentication-authencryption-element.md) -und [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Elementen angegeben wird. Sie variiert auch je nach [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md).

In der folgenden Tabelle sind gültige **keymaterialwerte** für einige Authentifizierungs-und Verschlüsselungs Paare aufgeführt.



| [**Authentifizierungs**](wlan-profileschema-authentication-authencryption-element.md) Wert | [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Wert | [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) -Wert | Gültige **keymaterialwerte**                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Open oder Shared                                                                           | WEP                                                                              | Network Key                                                            | Dieses Element enthält einen WEP-Schlüssel mit 5 oder 13 ANSI-Zeichen oder 10 oder 26 hexadezimal Zeichen.                                                                                             |
| WPAPSK oder WPA2PSK                                                                        | TKIP oder AES                                                                      | passPhrase                                                            | Dieses Element enthält eine Passphrase von 8 bis 63 ASCII-Zeichen, d. h. 8 bis 63 ANSI-Zeichen im Bereich zwischen 32 und 126. Schlüsselwerte müssen den in 802.11 i angegebenen Anforderungen entsprechen. |
| WPAPSK oder WPA2PSK                                                                        | TKIP oder AES                                                                      | Network Key                                                            | Dieses Element enthält einen Schlüssel mit 64 hexadezimalen Zeichen.                                                                                                                                      |



 

Unicode-Zeichen können eingegeben werden, wenn oben ANSI-oder ASCII-Zeichen angegeben sind. Wenn die angegebenen Unicode-Zeichen jedoch nicht ANSI-oder ASCII-Zeichen zugeordnet werden können, wird das angegebene Schlüsselmaterial abgelehnt.

Das von [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) zurückgegebene Schlüsselmaterial ist immer verschlüsselt. Wenn nicht verschlüsseltes Schlüsselmaterial an [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)übermittelt wird, wird das Schlüsselmaterial auch automatisch verschlüsselt, bevor es im Profil Speicher gespeichert wird.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Das Schlüsselmaterial wird nie verschlüsselt.

Wenn Ihr Prozess im Kontext des Kontos "LocalSystem" ausgeführt wird, können Sie das Schlüsselmaterial durch den Aufruf von [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)entschlüsseln.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **Keymaterial** -Element verwenden, finden Sie unter Beispiel für [nicht-Broadcast profile](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md)und [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**sharedkey (Sicherheit)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
