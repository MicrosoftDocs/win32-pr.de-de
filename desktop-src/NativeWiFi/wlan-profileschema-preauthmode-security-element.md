---
description: Gibt an, ob die Vorauthentifizierung vom Client verwendet wird.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: preAuthMode (security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dd8fad733b66337572b428ad9b15bbf8e24fb96444a646100a331f7ec9ce460a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797788"
---
# <a name="preauthmode-security-element"></a>preAuthMode (security)-Element

Das preAuthMode -Element (Sicherheit) gibt an, ob die Vorauthentifizierung vom Client verwendet wird. Die Vorauthentifizierung ist für sicheres schnelles Roaming mit WPA2 erforderlich. Dieses Element ist nur für WPA2-definierte Netzwerke gültig, für die [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) auf "enabled" festgelegt ist. Wenn **PMKCacheMode** aktiviert ist und dieses Element nicht vorhanden ist, lautet der Standardwert "disabled".

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="preAuthMode"
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Sicherheit**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Sicherheit (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




