---
description: Enthält Informationen zu gemeinsam genutzten Schlüsseln.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: sharedkey-Element (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363527"
---
# <a name="sharedkey-security-element"></a>sharedkey-Element (Security)

Das sharedkey-Element (Security) enthält Informationen zu gemeinsam genutzten Schlüsseln. Dieses Element ist nur erforderlich, wenn für das Authentifizierungs-und Verschlüsselungs paar WEP-oder PSK-Schlüssel erforderlich sind.

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                 | type                                                              | BESCHREIBUNG                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md) | [string](/dotnet/api/system.string)   | Enthält den Netzwerkschlüssel oder die Passphrase.<br/>                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | Der Schlüsseltyp.<br/>                                                                                                                                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)     | [boolean](/dotnet/api/system.boolean) | Gibt an, ob der Schlüssel verschlüsselt ist.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element muss den Wert false aufweisen.<br/> |



## <a name="remarks"></a>Bemerkungen

Für Windows Vista und Windows Server 2008 werden die dem **sharedkey** -Element zugeordneten Daten vor dem Speichern im Profil Speicher verschlüsselt.

Für Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2 werden die Daten nicht verschlüsselt.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **sharedkey** -Element verwenden, finden Sie unter Beispiel für [nicht-Broadcast profile](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md)und [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).

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

[**Sicherung**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Sicherheit (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
