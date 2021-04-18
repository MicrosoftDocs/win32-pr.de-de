---
description: Identifiziert den IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Ouiheader (IHV)-Element
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
ms.openlocfilehash: a31feb123e31489c751b7844e06d5c344278778e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347140"
---
# <a name="ouiheader-ihv-element"></a>Ouiheader (IHV)-Element

Das ouiheader (IHV)-Element identifiziert den IHV.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

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

Das-Element wird durch das [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) -Element definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | type | BESCHREIBUNG                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [**Ische**](wlan-profileschema-oui-ouiheader-element.md)   |      | Enthält eine hexbinär Datei mit 3 Bytes, die den IHV identifiziert.<br/>                            |
| [**Sorte**](wlan-profileschema-type-ouiheader-element.md) |      | Enthält eine hexbinär Datei mit 1 Byte, die zur Unterscheidung von NICs durch denselben IHV verwendet wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**IHV (wlanprofile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




