---
description: Gibt den Wlan-Standard 802.11 an, der in einem WLAN verwendet wird.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: phyType-Element (Konnektivität)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f9af94923f9160d18a9787b61036d5cf4104aede6488e2219b18a84325da46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684020"
---
# <a name="phytype-connectivity-element"></a>phyType-Element (Konnektivität)

Das phyType-Element (Konnektivität) gibt den Funk-LAN-Standard 802.11 an, der in einem WLAN verwendet wird.

Sie können mehrere **phyType-s** angeben. Wenn kein **phyType** angegeben wird, kann das Profil verwendet werden, um eine Verbindung mit einem beliebigen **phyType herzustellen.** Der Wert "n" wird nur auf Windows Vista mit Service Pack 1 (SP1) und neueren Versionen des Betriebssystems unterstützt.

**Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
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
```

Das -Element wird durch das [**Konnektivitätselement**](wlan-profileschema-connectivity-msm-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Verbindung**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Konnektivität (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




