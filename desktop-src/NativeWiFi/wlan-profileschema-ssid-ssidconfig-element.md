---
description: Enthält eine SSID für ein drahtloses LAN.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID-Element (ssidconfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866031"
---
# <a name="ssid-ssidconfig-element"></a>SSID-Element (ssidconfig)

Das SSID-Element (ssidconfig) enthält eine SSID für ein drahtloses LAN.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Höchstens ein **SSID** -Element kann in einem Profil angezeigt werden.

``` syntax
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
```

Das **SSID** -Element wird vom [**ssidconfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                              | type | BESCHREIBUNG                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | Enthält die SSID eines Drahtlos-LANs im Hexadezimal Format.<br/> |
| [**Benennen**](wlan-profileschema-name-ssid-element.md) |      | Enthält die SSID für ein drahtloses LAN.<br/>                      |



## <a name="remarks"></a>Bemerkungen

Obwohl das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element optional sind, muss mindestens ein **Hex** -oder [**Name**](wlan-profileschema-name-ssid-element.md) -Element als untergeordnetes Element des **SSID** -Elements angezeigt werden.

Wenn Profilinformationen in eine SSID konvertiert werden, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element in die SSID (sofern vorhanden) konvertiert, und das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird ignoriert. Wenn das **Hex** -Element nicht vorhanden ist, wird das [**Name**](wlan-profileschema-name-ssid-element.md) -Element mithilfe der Unicode-in-ASCII-Konvertierung in eine SSID konvertiert.

Wenn eine SSID in einem Profil gespeichert wird, wird das [**Hex**](wlan-profileschema-hex-ssid-element.md) -Element immer generiert. Das [**Name**](wlan-profileschema-name-ssid-element.md) -Element wird nur generiert, wenn sowohl die ASCII-als auch die Unicode-Konvertierung der SSID und die Generierung des XML-Profils erfolgreich sind. Einige Informationen aus der ursprünglichen SSID können verloren gehen, wenn Sie in einen [**Namen**](wlan-profileschema-name-ssid-element.md)konvertiert werden.

## <a name="examples"></a>Beispiele

Beispiel Profile, die das **SSID** -Element verwenden, finden Sie unter [Beispiele für drahtlos profile](wireless-profile-samples.md).

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

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Ssidconfig (wlanprofile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




