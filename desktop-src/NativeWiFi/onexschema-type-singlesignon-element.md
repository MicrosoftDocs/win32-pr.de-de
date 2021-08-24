---
description: Gibt an, wann einmaliges Anmelden ausgeführt wird.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: type (singleSignOn)-Element
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
ms.openlocfilehash: a8a395a5cdbd21bd33012e624f069d9447204cc96ffd2996a138ebf5d65f7bb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800730"
---
# <a name="type-singlesignon-element"></a>type (singleSignOn)-Element

Das element type (singleSignOn) gibt an, wann einmaliges Anmelden ausgeführt wird. Wenn diese Einstellung auf festgelegt `preLogon` ist, wird einmaliges Anmelden ausgeführt, bevor sich der Benutzer anmeldet. Wenn diese Einstellung auf festgelegt `postLogon` ist, wird das einmalige Anmelden sofort nach der Anmeldung des Benutzers ausgeführt.

**Windows XP mit SP3 und Wlan-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

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

Das **type-Element** wird durch das [**singleSignOn-Element**](onexschema-singlesignon-onex-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




