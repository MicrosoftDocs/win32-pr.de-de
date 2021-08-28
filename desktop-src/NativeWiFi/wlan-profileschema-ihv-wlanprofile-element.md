---
description: Enthält verschiedene Einstellungen für unabhängige Hardwarehersteller.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: IHV-Element (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1cfcd9ee463ef91d04d0bebbeac800d48da32fdd777edc2a08ccf0051410160d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799920"
---
# <a name="ihv-wlanprofile-element"></a>IHV-Element (WLANProfile)

Das IHV-Element (WLANProfile) enthält verschiedene Einstellungen für unabhängige Hardwarehersteller. Wenn ein Profil IHV-Sicherheitseinstellungen enthält, setzen sie alle von Microsoft definierten Sicherheitseinstellungen außer Kraft.

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
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

Das -Element wird durch das [**WLANProfile-Element**](wlan-profileschema-wlanprofile-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | Typ                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verbindung**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Enthält IHV-bezogene Konnektivitätseinstellungen.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Enthält ein hexadezimalesBinary mit 3 Byte, das die IHV identifiziert.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifiziert die IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**Sicherheit**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Enthält IHV-spezifische Sicherheitseinstellungen. Microsoft-Sicherheitseinstellungen und IHV-Sicherheitseinstellungen schließen sich gegenseitig aus. Das gesamte Profil ist ungültig, wenn beide Sicherheitseinstellungen vorhanden sind.<br/>                                                                                                                                                                                            |
| [**Typ**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Enthält ein hexadezimalesBinary-1-Byte, das verwendet wird, um NICs durch dieselbe IHV zu unterscheiden.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Gibt den Ursprung der 802.1X-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden. Wenn [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) true ist, verwenden IHV-Sicherheitskomponenten von Microsoft definierte 802.1X-Einstellungen. Wenn **useMSOneX** false ist, verwenden IHV-Sicherheitskomponenten vom Anbieter bereitgestellte 802.1X-Einstellungen. Standardmäßig ist **useMSOneX** false. Dieses Element ist optional.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
