---
description: Gibt an, ob die Vorauthentifizierung vom Client verwendet wird.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: preauthmode (Security)-Element
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
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345685"
---
# <a name="preauthmode-security-element"></a>preauthmode (Security)-Element

Das preauthmode (Security)-Element gibt an, ob die Vorauthentifizierung vom Client verwendet wird. Die Vorauthentifizierung ist für das sichere schnelle Roaming von WPA2 erforderlich. Dieses Element gilt nur für WPA2-definierte Netzwerke, bei denen [**pmkcachemode**](wlan-profileschema-pmkcachemode-security-element.md) auf "aktiviert" festgelegt ist. Wenn **pmkcachemode** aktiviert ist und dieses Element nicht vorhanden ist, ist der Standardwert "deaktiviert".

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

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

 

 




