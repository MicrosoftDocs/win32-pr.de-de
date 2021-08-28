---
description: Enthält verschiedene Konnektivitätseinstellungen.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: Connectivity-Element (MSM)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8745671004799f96aecfe68b531c122c76122b5865678258fd241e9d8a07260a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799910"
---
# <a name="connectivity-msm-element"></a>Connectivity-Element (MSM)

Das Konnektivitätselement (MSM) enthält verschiedene Konnektivitätseinstellungen.

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
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

Das -Element wird durch das [**MSM-Element**](wlan-profileschema-msm-wlanprofile-element.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                            | Typ |
|--------------------------------------------------------------------|------|
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a>Beispiele

Beispielprofile, die das **Konnektivitätselement** verwenden, finden Sie unter [Beispiele für Funkprofile.](wireless-profile-samples.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP nur mit \[ SP3-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                |
| Verteilbare Komponente<br/>          | WLAN-API für Windows XP mit SP2<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Msm**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




