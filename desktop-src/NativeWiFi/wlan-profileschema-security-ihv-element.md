---
description: Enthält verschiedene Sicherheitseinstellungen, die von unabhängigen Hardwareanbietern verwendet werden.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Security (IHV)-Element
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
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373087"
---
# <a name="security-ihv-element"></a>Security (IHV)-Element

Das Sicherheitselement (IHV) enthält verschiedene Sicherheitseinstellungen, die von unabhängigen Hardwareanbietern verwendet werden.

Die Sicherheitseinstellungen von Microsoft und die IHV-Sicherheitseinstellungen schließen sich gegenseitig aus. Wenn beide Gruppen von Sicherheitseinstellungen im gleichen Profil vorhanden sind, ist das Profil ungültig.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

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

Das **Security** -Element wird durch das [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) -Element definiert.

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

 

 




