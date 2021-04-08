---
description: Gibt die maximale Verzögerung (in Sekunden) an, bevor der einmalige Anmelde Verbindungsversuch fehlschlägt.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: MaxDelay-Element (SingleSignOn)
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
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864812"
---
# <a name="maxdelay-singlesignon-element"></a>MaxDelay-Element (SingleSignOn)

Das MaxDelay-Element (SingleSignOn) gibt die maximale Verzögerung (in Sekunden) an, bevor der einmalige Anmelde Verbindungsversuch fehlschlägt.

Dieses Element ist optional. Wenn MaxDelay nicht in einem Profil angegeben ist, wird ein Wert von 10 Sekunden verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

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

Das **MaxDelay** -Element wird durch das [**SingleSignOn**](onexschema-singlesignon-onex-element.md) -Element definiert.

## <a name="remarks"></a>Bemerkungen

Dieser Parameter kann über die Befehlszeile mit dem **Netsh WLAN Set ProfileParameter** -Befehl festgelegt werden. Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

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

 

 
