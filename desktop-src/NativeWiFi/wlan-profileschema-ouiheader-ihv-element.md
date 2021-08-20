---
description: Identifiziert die IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: OUIHeader-Element (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5293a6e69c1384922572764674cbadd9980702c49f8945518ff9b0c56beee2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797920"
---
# <a name="ouiheader-ihv-element"></a>OUIHeader-Element (IHV)

Das OUIHeader-Element (IHV) identifiziert die IHV.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
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
```

Das -Element wird durch das [**IHV-Element**](wlan-profileschema-ihv-wlanprofile-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | type | Beschreibung                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)   |      | Enthält eine hexadezimalbinäre 3-Byte-Datei, die die IHV identifiziert.<br/>                            |
| [**Typ**](wlan-profileschema-type-ouiheader-element.md) |      | Enthält eine hexadezimalbinäre 1-Byte-Datei, die verwendet wird, um NICs durch dieselbe IHV zu unterscheiden.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Ihv**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




