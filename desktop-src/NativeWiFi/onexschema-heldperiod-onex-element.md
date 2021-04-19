---
description: Gibt die Zeitdauer in Sekunden an, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: heldperiod-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367920"
---
# <a name="heldperiod-onex-element"></a>heldperiod-Element (Onex)

Das heldperiod (Onex)-Element gibt die Zeitdauer in Sekunden an, in der ein Client die Authentifizierung nach einem fehlgeschlagenen Authentifizierungs Versuch nicht erneut versucht.

Dieses Element ist optional. Wenn heldperiod nicht in einem Profil angegeben ist, wird ein Wert von 1 Sekunde verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **heldperiod** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.

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

 

 




