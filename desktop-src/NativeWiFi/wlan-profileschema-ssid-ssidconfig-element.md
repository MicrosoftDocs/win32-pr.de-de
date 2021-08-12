---
description: Enthält eine SSID für ein Drahtlos-LAN.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID-Element (SSIDConfig)
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
ms.openlocfilehash: 5d58ed866e79269e604fe49ad8afe65d557f27a90d0be03904b8d27da5ac5c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619057"
---
# <a name="ssid-ssidconfig-element"></a>SSID-Element (SSIDConfig)

Das SSID-Element (SSIDConfig) enthält eine SSID für ein Wlan.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Höchstens ein **SSID-Element** kann in einem Profil angezeigt werden.

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

Das **SSID-Element** wird durch das [**SSIDConfig-Element**](wlan-profileschema-ssidconfig-wlanprofile-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                              | type | Beschreibung                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**Hex**](wlan-profileschema-hex-ssid-element.md)   |      | Enthält die SSID eines Drahtlos-LAN im Hexadezimalformat.<br/> |
| [**Namen**](wlan-profileschema-name-ssid-element.md) |      | Enthält die SSID für ein Drahtlos-LAN.<br/>                      |



## <a name="remarks"></a>Hinweise

Obwohl die [**Hexadezimal-**](wlan-profileschema-hex-ssid-element.md) und [**Namenselemente**](wlan-profileschema-name-ssid-element.md) optional sind, muss mindestens ein **Hexadezimal-** oder [**Namenselement**](wlan-profileschema-name-ssid-element.md) als untergeordnetes Element des **SSID-Elements** angezeigt werden.

Wenn Profilinformationen in eine SSID konvertiert werden, wird das [**Hexadezimalelement**](wlan-profileschema-hex-ssid-element.md) in die SSID konvertiert (sofern vorhanden), und das [**Name-Element**](wlan-profileschema-name-ssid-element.md) wird ignoriert. Wenn das **Hexadezimalelement** nicht vorhanden ist, wird das [**Name-Element**](wlan-profileschema-name-ssid-element.md) mithilfe der Unicode- in ASCII-Konvertierung in eine SSID konvertiert.

Wenn eine SSID in einem Profil gespeichert wird, wird das [**Hexadezimalelement**](wlan-profileschema-hex-ssid-element.md) immer generiert. Das [**Name-Element**](wlan-profileschema-name-ssid-element.md) wird nur generiert, wenn sowohl die ASCII- in Unicode-Konvertierung der SSID als auch die XML-Profilgenerierung erfolgreich sind. Einige Informationen aus der ursprünglichen SSID verloren, wenn sie in einen [**Namen**](wlan-profileschema-name-ssid-element.md)konvertiert werden.

## <a name="examples"></a>Beispiele

Beispielprofile, die das **SSID-Element** verwenden, finden Sie unter [Beispiele für Funkprofile.](wireless-profile-samples.md)

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

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




