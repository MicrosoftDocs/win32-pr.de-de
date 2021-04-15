---
description: Gibt an, wie viele vorauthentifizierungs Versuche für benachbarte APS versucht werden.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: preauththrottle (Security)-Element
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
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525754"
---
# <a name="preauththrottle-security-element"></a>preauththrottle (Security)-Element

Das preauththrottle (Security)-Element gibt die Anzahl von vorauthentifizierungs versuchen für benachbarte APS an. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist. Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, wird für die Anzahl von versuchen standardmäßig der Wert 3 verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

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

Das-Element wird durch das [**Security**](wlan-profileschema-security-msm-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Sicherung**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Sicherheit (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




