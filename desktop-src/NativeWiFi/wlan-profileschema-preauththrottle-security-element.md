---
description: Gibt die Anzahl von Vorauthentifizierungsversuchen für benachbarte APs an.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: preAuthThrottle(security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8bc310d19126a0e4bc9a7e6abf2a6ae1d0eb917cb5f425796d10bee66ea6ebed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064600"
---
# <a name="preauththrottle-security-element"></a>preAuthThrottle(security)-Element

Das preAuthThrottle -Element (Sicherheit) gibt die Anzahl von Vorauthentifizierungsversuchen für benachbarte APs an. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, für die [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) auf "enabled" festgelegt ist. Wenn **PMKCacheMode** aktiviert ist und dieses Element nicht vorhanden ist, beträgt die Anzahl der Versuche standardmäßig 3.

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="preAuthThrottle"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="16"
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

 

 




