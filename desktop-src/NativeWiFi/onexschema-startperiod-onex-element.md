---
description: Gibt die Zeitdauer in Sekunden an, die gewartet werden soll, bevor ein EAPOL-Start gesendet wird.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: startPeriod-Element (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2d21381939348ce8c37a9b23abb2283ab209e766bbce452c3802b8c5defe0872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800720"
---
# <a name="startperiod-onex-element"></a>startPeriod-Element (OneX)

Das startPeriod -Element (OneX) gibt die Wartezeit in Sekunden an, die gewartet werden soll, bevor EAPOL-Start gesendet wird. Eine EAPOL-Start wird gesendet, um den 802.1X-Authentifizierungsprozess zu starten.

Dieses Element ist optional. Wenn startPeriod nicht in einem Profil angegeben ist, wird ein Wert von 5 Sekunden verwendet.

**Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="startPeriod">
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

Das **startPeriod-Element** wird durch das [**OneX-Element**](onexschema-onex-element.md) definiert.

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

 

 




