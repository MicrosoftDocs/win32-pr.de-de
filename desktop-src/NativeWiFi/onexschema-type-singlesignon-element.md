---
description: Gibt an, wann einmaliges Anmelden ausgeführt wird.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Type (SingleSignOn)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 947c8801e5b2534f4c3b4e548a2a2f2c7a4250d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350471"
---
# <a name="type-singlesignon-element"></a>Type (SingleSignOn)-Element

Das Type (SingleSignOn)-Element gibt an, wann einmaliges Anmelden ausgeführt wird. Wenn die Einstellung auf festgelegt `preLogon` ist, wird einmaliges Anmelden ausgeführt, bevor sich der Benutzer anmeldet. Wenn der Wert auf festgelegt `postLogon` ist, wird das einmalige Anmelden sofort nach der Anmeldung des Benutzers ausgeführt.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **Type** -Element wird durch das [**SingleSignOn**](onexschema-singlesignon-onex-element.md) -Element definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**SingleSignOn (Onex)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




