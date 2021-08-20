---
description: Enthält verschiedene Sicherheitseinstellungen, die von unabhängigen Hardwareanbietern verwendet werden.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: security (IHV)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e4baeadc5e53dc53d0a526b62c4905da1a778a1015f58321ae8b96e4aa52dfcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912750"
---
# <a name="security-ihv-element"></a>security (IHV)-Element

Das Element Security (IHV) enthält verschiedene Sicherheitseinstellungen, die von unabhängigen Hardwareanbietern verwendet werden.

Microsoft-Sicherheitseinstellungen und IHV-Sicherheitseinstellungen schließen sich gegenseitig aus. Wenn beide Sicherheitseinstellungen im gleichen Profil vorhanden sind, ist das Profil ungültig.

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="security">
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

Das **Sicherheitselement** wird durch das [**IHV-Element**](wlan-profileschema-ihv-wlanprofile-element.md) definiert.

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

 

 




