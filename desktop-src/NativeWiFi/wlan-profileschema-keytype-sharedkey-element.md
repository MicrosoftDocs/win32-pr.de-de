---
description: Gibt an, ob der gemeinsam verwendete Schlüssel ein Netzwerkschlüssel oder eine Passphrase ist.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: KeyType (sharedkey)-Element
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
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351711"
---
# <a name="keytype-sharedkey-element"></a>KeyType (sharedkey)-Element

Das KeyType (sharedkey)-Element gibt an, ob der gemeinsam verwendete Schlüssel ein Netzwerkschlüssel oder eine Passphrase ist.

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

Das-Element wird durch das [**sharedkey**](wlan-profileschema-sharedkey-security-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn das [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md) Element den Wert WEP hat, muss **KeyType** auf **networkkey** festgelegt werden.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **KeyType** -Element verwenden, finden Sie unter Beispiel für [nicht-Broadcast profile](non-broadcast-profile-sample.md), [WPA-Personal Profile](wpa-personal-profile-sample.md)Sample und [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).

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

 

 




