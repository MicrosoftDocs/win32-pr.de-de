---
description: Gibt die maximale Anzahl von EAPOL-Start gesendeten Nachrichten an.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: maxstart (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350204"
---
# <a name="maxstart-onex-element"></a>maxstart (Onex)-Element

Das maxstart (Onex)-Element gibt die maximale Anzahl von EAPOL-Start gesendeten Nachrichten an. Nachdem die maximale Anzahl von EAPOL-Start-Nachrichten gesendet wurde, nimmt der Client an, dass im Netzwerk kein Authentifikator vorhanden ist.

Dieses Element ist optional. Wenn maxstart nicht in einem Profil angegeben ist, wird der Wert 3 Nachrichten verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **maxstart** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




