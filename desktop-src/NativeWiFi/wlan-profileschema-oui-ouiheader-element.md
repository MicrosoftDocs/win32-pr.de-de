---
description: Enthält eine hexbinär Datei mit 3 Bytes, die den IHV identifiziert.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: OUI (ouiheader)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 49a9cceffb308c64c8d1addf7c257b422751661f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343275"
---
# <a name="oui-ouiheader-element"></a>OUI (ouiheader)-Element

Das OUI (ouiheader)-Element enthält ein 3-Byte-hexBinary, das den IHV identifiziert.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird nicht unterstützt.

``` syntax
<xs:element name="OUI">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das-Element wird durch das [**ouiheader**](wlan-profileschema-ouiheader-ihv-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Ouiheader**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Ouiheader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




