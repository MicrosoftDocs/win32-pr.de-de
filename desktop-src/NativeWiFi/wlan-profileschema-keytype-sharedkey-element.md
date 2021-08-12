---
description: Gibt an, ob der freigegebene Schlüssel ein Netzwerkschlüssel oder ein Passphrase ist.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: keyType-Element (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 88c9a48d1c70cd156fa3d8f63bd3b70d69a99a1151a18c95ffd556b2503c9575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619283"
---
# <a name="keytype-sharedkey-element"></a>keyType-Element (sharedKey)

Das keyType -Element (sharedKey) gibt an, ob der gemeinsam verwendete Schlüssel ein Netzwerkschlüssel oder ein Passphrase ist.

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das -Element wird durch das [**sharedKey-Element**](wlan-profileschema-sharedkey-security-element.md) definiert.

## <a name="remarks"></a>Hinweise

Wenn das [**Verschlüsselungselement**](wlan-profileschema-encryption-authencryption-element.md) über den Wert WEP verfügt, muss **keyType** auf **networkKey** festgelegt werden.

## <a name="examples"></a>Beispiele

Beispielprofile, die das **keyType-Element** verwenden, finden Sie unter [Beispiel für Nicht-Broadcastprofil,](non-broadcast-profile-sample.md) [WPA-Personal Profile Sample](wpa-personal-profile-sample.md)und [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**sharedKey (Sicherheit)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




