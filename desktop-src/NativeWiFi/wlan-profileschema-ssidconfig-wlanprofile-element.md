---
description: Enthält mindestens eine SSIDs für drahtlose LANs.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Ssidconfig (wlanprofile)-Element
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
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865739"
---
# <a name="ssidconfig-wlanprofile-element"></a>Ssidconfig (wlanprofile)-Element

Das ssidconfig (wlanprofile)-Element enthält mindestens eine SSIDs für drahtlose LANs.

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

Das **ssidconfig** -Element wird vom [**wlanprofile**](wlan-profileschema-wlanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                    | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Enthält die SSID eines Drahtlos-LANs im Hexadezimal Format.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Benennen**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Enthält den Namen (Groß-/Kleinschreibung) der SSID eines drahtlosen LANs.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**nicht Broadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [boolean](/dotnet/api/system.boolean) | Gibt an, ob das Netzwerk seine SSID überträgt.<br/> Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf ESS festgelegt ist, kann dieser Wert entweder **true** oder **false** sein. Der Standardwert ist **true** , wenn dieses Element nicht vorhanden ist.<br/> Wenn [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) auf IBSS festgelegt ist, muss dieser Wert **false** lauten.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.<br/> |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Enthält eine SSID für ein drahtloses LAN.<br/> **Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Höchstens ein [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) -Element kann in einem Profil angezeigt werden.<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Beispiele

Beispiel Profile, die das **ssidconfig** -Element verwenden, finden Sie unter [Beispiele für Funk profile](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
