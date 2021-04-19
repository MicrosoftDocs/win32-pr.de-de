---
description: Gibt den 802,11 Wireless LAN-Standard an, der in einem Drahtlos Netzwerk verwendet wird.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: phytype (Connectivity)-Element
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
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353040"
---
# <a name="phytype-connectivity-element"></a>phytype (Connectivity)-Element

Das Element "phytype (Connectivity)" gibt den 802,11 Wireless LAN-Standard an, der in einem Drahtlos Netzwerk verwendet wird.

Sie können mehrere **phytype** s angeben. Wenn kein " **phytype** " angegeben ist, kann das Profil verwendet werden, um eine Verbindung mit einem beliebigen " **phytype**" herzustellen. Der Wert "n" wird nur unter Windows Vista mit Service Pack 1 (SP1) und höheren Versionen des Betriebssystems unterstützt.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

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

Das-Element wird durch das [**konnektivitätselement**](wlan-profileschema-connectivity-msm-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Stech**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Konnektivität (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




