---
description: Gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: authencryption (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345810"
---
# <a name="authencryption-security-element"></a>authencryption (Security)-Element

Das authencryption (Security)-Element gibt das Authentifizierungs-und Verschlüsselungs Paar an, das für dieses Profil verwendet werden soll.

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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



| Element                                                                            | type                                                              | BESCHREIBUNG                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Genehmigung**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Gibt die Authentifizierungsmethode an, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden muss.<br/> |
| [**Verschlüsselungs**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Legt die Datenverschlüsselung fest, die zum Herstellen einer Verbindung mit dem Drahtlos Netzwerk verwendet werden soll.<br/>                       |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Gibt an, ob 802.1 x verwendet wird.<br/>                                                     |



## <a name="remarks"></a>Bemerkungen

Das ""-Element kann als unter [**geordnetes Element des**](wlan-profileschema-fipsmode-authencryption-element.md) **authencryption** -Elements eingefügt werden.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **authencryption** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md). Ein Beispiel Profil, das das-Element in der-Datei verwendet, finden Sie unter Beispiel für das [**PPS**](wlan-profileschema-fipsmode-authencryption-element.md) - [Profil](fips-profile-sample.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beispiele für Funk profile](wireless-profile-samples.md)
</dt> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Sicherung**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Sicherheit (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
