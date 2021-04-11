---
description: Gibt den Typ der Datenverschlüsselung an, die zum Herstellen einer Verbindung mit einem drahtlosen LAN verwendet werden soll.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Encryption-Element (authencryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129729"
---
# <a name="encryption-authencryption-element"></a>Encryption-Element (authencryption)

Das Encryption (authencryption)-Element gibt den Typ der Datenverschlüsselung an, die zum Herstellen einer Verbindung mit einem drahtlosen LAN verwendet werden soll.

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das-Element wird durch das [**authencryption**](wlan-profileschema-authencryption-security-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Wenn das **Verschlüsselungs** Element den Wert WEP hat, muss [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) auf **networkkey** festgelegt werden.

Die AES-Verschlüsselungsmethode ist gemäß den Spezifikationen [802.1 x](https://ieeexplore.ieee.org/document/1438730) und [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) angegeben.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das- **Verschlüsselungs** Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).

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

 

 




