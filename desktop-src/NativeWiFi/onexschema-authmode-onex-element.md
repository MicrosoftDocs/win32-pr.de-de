---
description: Gibt den Typ der für die Authentifizierung verwendeten Anmelde Informationen an.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: authmode-Element (Onex)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356708"
---
# <a name="authmode-onex-element"></a>authmode-Element (Onex)

Das authmode (Onex)-Element gibt den Typ der Anmelde Informationen an, die für die Authentifizierung verwendet werden. In der folgenden Tabelle sind die möglichen Werte beschrieben.



| Wert         | BESCHREIBUNG                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| machineoruser | Verwenden Sie Computer-oder Benutzer Anmelde Informationen. Wenn ein Benutzer angemeldet ist, werden die Anmelde Informationen des Benutzers zur Authentifizierung verwendet. Wenn kein Benutzer angemeldet ist, werden Computer Anmelde Informationen verwendet. |
| Computer       | Verwenden Sie nur Computer Anmelde Informationen.                                                                                                                                           |
| user          | Nur Benutzer Anmelde Informationen verwenden.                                                                                                                                              |
| guest         | Nur Gast Anmelde Informationen (leer) verwenden.                                                                                                                                     |



 

Dieses Element ist optional. Wenn authmode nicht in einem Profil angegeben ist, wird der Wert `machineOrUser` verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das **authmode** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.

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

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 
