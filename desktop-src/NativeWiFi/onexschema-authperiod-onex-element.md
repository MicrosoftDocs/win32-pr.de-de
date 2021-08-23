---
description: Gibt die maximale Zeitdauer in Sekunden an, in der ein Client auf eine Antwort vom Authentator wartet.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: authPeriod (OneX)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ccaef08f65baffa0d7b9a921afd9db78a6ac6c6dd1d0bf4fd8075454fe38be21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684859"
---
# <a name="authperiod-onex-element"></a>authPeriod (OneX)-Element

Das authPeriod (OneX)-Element gibt die maximale Zeitdauer in Sekunden an, in der ein Client auf eine Antwort vom Authentisierungsator wartet. Wenn innerhalb des angegebenen Zeitraums keine Antwort empfangen wird, geht der Client davon aus, dass im Netzwerk kein Authentator vorhanden ist.

Dieses Element ist optional. Wenn authPeriod nicht in einem Profil angegeben ist, wird ein Wert von 18 Sekunden verwendet.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="authPeriod">
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

Das **authPeriod-Element** wird durch das [**OneX-Element**](onexschema-onex-element.md) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




