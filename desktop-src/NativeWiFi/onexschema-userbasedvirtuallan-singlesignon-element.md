---
description: Gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: userbasedvirtuallan (SingleSignOn)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129732"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>userbasedvirtuallan (SingleSignOn)-Element

Das userbasedvirtuallan (SingleSignOn)-Element gibt an, ob das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmelde Informationen des Benutzers geändert wird. Einige Netzwerk Zugriffs Server-Geräte (NAS) ändern das VLAN, nachdem sich ein Benutzer authentifiziert hat. Wenn userbasedvirtuallan den Wert true hat, kann der NAS das VLAN eines Geräts ändern, nachdem sich ein Benutzer authentifiziert hat.

Dieses Element ist optional. Wenn userbasedvirtuallan nicht in einem Profil angegeben ist, wird der Wert false verwendet.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

Das **userbasedvirtuallan** -Element wird durch das [**SingleSignOn**](onexschema-singlesignon-onex-element.md) -Element definiert.

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

 

 
