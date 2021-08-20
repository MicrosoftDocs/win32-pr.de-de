---
description: Enthält IHV-bezogene Konnektivitätseinstellungen. Sie ist derzeit nicht implementiert.
ms.assetid: d943e82a-8660-4df7-8f5c-42ed83f17313
title: connectivity(IHV)-Element
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
ms.openlocfilehash: 393a07df451c0a9e79f74f369a84bed5310d5efc6eae2186fe8da4844d3bb806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797910"
---
# <a name="connectivity-ihv-element"></a>connectivity(IHV)-Element

Das Konnektivitätselement (IHV) enthält IHV-bezogene Konnektivitätseinstellungen. Sie ist derzeit nicht implementiert.

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

Das -Element wird durch das [**IHV-Element**](wlan-profileschema-ihv-wlanprofile-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Ihv**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




