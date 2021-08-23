---
description: Gibt die maximale Verzögerung in Sekunden an, bevor der Verbindungsversuch für einmaliges Anmelden fehlschlägt.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: maxDelay-Element (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cd4e82e8031f57e9672dd11a066a9a1fb2e8f3540c93dc4e1898afa4f1cf6302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684840"
---
# <a name="maxdelay-singlesignon-element"></a>maxDelay-Element (singleSignOn)

Das maxDelay-Element (singleSignOn) gibt in Sekunden die maximale Verzögerung an, bevor der Verbindungsversuch für einmaliges Anmelden fehlschlägt.

Dieses Element ist optional. Wenn maxDelay nicht in einem Profil angegeben ist, wird ein Wert von 10 Sekunden verwendet.

**Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **maxDelay-Element** wird durch das [**singleSignOn-Element**](onexschema-singlesignon-onex-element.md) definiert.

## <a name="remarks"></a>Hinweise

Dieser Parameter kann über die Befehlszeile mit dem Befehl **netsh wlan set profileparameter festgelegt** werden. Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
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

 

 
