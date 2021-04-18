---
description: Enthält verschiedene Einstellungen für unabhängige Hardware Anbieter.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: IHV-Element (wlanprofile)
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
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347850"
---
# <a name="ihv-wlanprofile-element"></a>IHV-Element (wlanprofile)

Das IHV (wlanprofile)-Element enthält verschiedene Einstellungen für unabhängige Hardwarehersteller. Wenn ein Profil IHV-Sicherheitseinstellungen enthält, überschreiben Sie von Microsoft definierte Sicherheitseinstellungen.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

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

Das-Element wird durch das [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                             | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stech**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Enthält IHV-bezogene Konnektivitätseinstellungen.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**Ische**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Enthält eine hexbinär Datei mit 3 Bytes, die den IHV identifiziert.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Ouiheader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifiziert den IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**Sicherung**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Enthält IHV-spezifische Sicherheitseinstellungen. Die Sicherheitseinstellungen von Microsoft und die IHV-Sicherheitseinstellungen schließen sich gegenseitig aus. Das gesamte Profil ist ungültig, wenn beide Sicherheitseinstellungen vorhanden sind.<br/>                                                                                                                                                                                            |
| [**Sorte**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Enthält eine hexbinär Datei mit 1 Byte, die zur Unterscheidung von NICs durch denselben IHV verwendet wird.<br/>                                                                                                                                                                                                                                                                                                        |
| [**usemsonex**](wlan-profileschema-usemsonex-ihv-element.md)       | [boolean](/dotnet/api/system.boolean) | Gibt den Ursprung der 802.1 x-Sicherheitseinstellungen an, die von einer IHV-Sicherheitskomponente verwendet werden. Wenn [**usemsonex**](wlan-profileschema-usemsonex-ihv-element.md) auf true festgelegt ist, verwenden die IHV-Sicherheitskomponenten von Microsoft definierte 802.1 x-Einstellungen. Wenn **usemsonex** den Wert false hat, verwenden IHV-Sicherheitskomponenten vom Hersteller bereitgestellte 802.1 x-Einstellungen. Standardmäßig ist **usemsonex** false. Dieses Element ist optional.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
