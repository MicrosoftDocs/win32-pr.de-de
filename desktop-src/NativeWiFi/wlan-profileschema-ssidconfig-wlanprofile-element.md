---
description: Enthält mindestens ein SSIDs für LANs für Funkverbindungen.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: SSIDConfig(WLANProfile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6df6edc3affa551d62473b616562257cd422fcc4a4021ea7e4ef05ba3c8af9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619041"
---
# <a name="ssidconfig-wlanprofile-element"></a>SSIDConfig(WLANProfile)-Element

Das SSIDConfig-Element (WLANProfile) enthält mindestens ein SSIDs-Element für LANs für Funkverbindungen.

``` syntax
<xs:element name="SSIDConfig"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="SSID"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="hex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="name"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:minLength
                                        value="1"
                                     />
                                    <xs:maxLength
                                        value="32"
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
            <xs:element name="nonBroadcast"
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

Das **SSIDConfig-Element** wird durch das [**WLANProfile-Element**](wlan-profileschema-wlanprofile-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | type                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Enthält die SSID eines WLAN im Hexadezimalformat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Namen**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Enthält den Namen der SSID eines Wlan-Lans (unter Schreibung der Schreibung).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**nonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [boolean](/dotnet/api/system.boolean) | Gibt an, ob das Netzwerk seine SSID überträgt.<br/> Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf ESS festgelegt ist, kann dieser Wert entweder **TRUE** oder **FALSE sein.** Der Standardwert ist **TRUE, wenn** dieses Element nicht vorhanden ist.<br/> Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf IBSS festgelegt ist, muss dieser Wert **FALSE sein.**<br/> **Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/> |
| [**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Enthält eine SSID für ein WLAN.<br/> **Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2:** In einem Profil kann nur ein [**SSID-Element**](wlan-profileschema-ssid-ssidconfig-element.md) angezeigt werden.<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Beispiele

Beispielprofile, die das **SSIDConfig-Element** verwenden, finden Sie unter [Beispiele für Funkprofile.](wireless-profile-samples.md)

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
