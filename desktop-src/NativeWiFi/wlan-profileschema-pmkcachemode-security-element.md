---
description: Gibt an, ob die PMK-Zwischenspeicherung verwendet wird.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: PMKCacheMode (security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 23e32d7a658e41f80eb2a4d8d743afc2c96f7a5a1b4135e646374b98e6acac26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619256"
---
# <a name="pmkcachemode-security-element"></a>PMKCacheMode (security)-Element

Das PMKCacheMode -Element (Security) gibt an, ob pmk caching verwendet wird. Dieses Element ist nur für WPA2-definierte Netzwerke gültig. Die PMK-Zwischenspeicherung wird in der [Spezifikation 802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) beschrieben.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das -Element wird durch das [**-Sicherheitselement**](wlan-profileschema-security-msm-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Sicherheit**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Sicherheit (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




