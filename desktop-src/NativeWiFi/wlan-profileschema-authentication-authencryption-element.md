---
description: Gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: authentication-Element (authencryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214995"
---
# <a name="authentication-authencryption-element"></a>authentication-Element (authencryption)

Das authentication-Element (authencryption) gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet wird.

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das-Element wird durch das [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die-Enumerationswerte beschrieben.



| Wert   | BESCHREIBUNG                            |
|---------|----------------------------------------|
| open    | Öffnen Sie 802,11-Authentifizierung.            |
| Freigegeben  | Shared 802,11-Authentifizierung.          |
| WPA     | WPA-Enterprise 802,11-Authentifizierung.  |
| WPAPSK  | WPA-Personal 802,11-Authentifizierung.    |
| WPA2    | WPA2-Enterprise 802,11-Authentifizierung. |
| WPA2PSK | WPA2-Personal 802,11-Authentifizierung.   |



 

Weitere Informationen zu 802,11-Authentifizierungsmethoden finden Sie in den Spezifikationen [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)und [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Beispiele

Beispiel Profile, die das- **Authentifizierungs** Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**authencryption (Sicherheit)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




