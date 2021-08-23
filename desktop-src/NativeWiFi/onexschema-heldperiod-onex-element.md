---
description: Gibt die Zeitdauer in Sekunden an, in der ein Client nach einem fehlgeschlagenen Authentifizierungsversuch nicht erneut versucht, die Authentifizierung zu versuchen.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: heldPeriod-Element (OneX)
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
ms.openlocfilehash: 5a2009ac8518d114353e3323b97c4ea57c54fc801447c375641b8f6bbd1b2bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684851"
---
# <a name="heldperiod-onex-element"></a>heldPeriod-Element (OneX)

Das heldPeriod (OneX)-Element gibt die Zeitdauer in Sekunden an, in der ein Client nach einem fehlgeschlagenen Authentifizierungsversuch nicht erneut versucht, die Authentifizierung zu versuchen.

Dieses Element ist optional. Wenn heldPeriod nicht in einem Profil angegeben ist, wird ein Wert von 1 Sekunde verwendet.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

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

Das **heldPeriod-Element** wird durch das [**OneX-Element**](onexschema-onex-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




