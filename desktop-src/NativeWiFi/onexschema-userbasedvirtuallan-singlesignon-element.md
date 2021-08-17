---
description: Gibt an, ob sich das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmeldeinformationen des Benutzers ändert.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: userBasedVirtualLan -Element (singleSignOn)
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
ms.openlocfilehash: 9272f61e7efeaf90ba68b1577af9b0062e507984372f7f09ebdbfc15e4ac6fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064970"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a>userBasedVirtualLan -Element (singleSignOn)

Das userBasedVirtualLan-Element (singleSignOn) gibt an, ob sich das vom Gerät verwendete virtuelle LAN (VLAN) basierend auf den Anmeldeinformationen des Benutzers ändert. Einige NAS-Geräte (Network Access Server) ändern das VLAN, nachdem sich ein Benutzer authentifiziert hat. Wenn userBasedVirtualLan true ist, kann der NAS das VLAN eines Geräts ändern, nachdem sich ein Benutzer authentifiziert hat.

Dieses Element ist optional. Wenn userBasedVirtualLan nicht in einem Profil angegeben ist, wird der Wert FALSE verwendet.

**Windows XP mit SP3 und wlan-API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

Das **userBasedVirtualLan-Element** wird durch das [**singleSignOn-Element**](onexschema-singlesignon-onex-element.md) definiert.

## <a name="remarks"></a>Hinweise

Dieser Parameter kann über die Befehlszeile mit dem Befehl **netsh wlan set profileparameter festgelegt** werden. Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (wlan).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Definitionskontext des Elements im Schema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schemainstanz**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
