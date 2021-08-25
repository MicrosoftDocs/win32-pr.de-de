---
description: Das Installationsprogramm legt den Wert der UserSID-Eigenschaft auf die Zeichenfolgendarstellung der Sicherheits-ID (SID) des Benutzers fest, der die Installation ausführt. Weitere Informationen finden Sie unter Autorisierungsstrukturen.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26185c886117b39355241151ffef6d8615bd5f8d10a7f50bd5937a301f7b398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809160"
---
# <a name="usersid-property"></a>UserSID-Eigenschaft

Das Installationsprogramm legt den Wert der **UserSID-Eigenschaft** auf die Zeichenfolgendarstellung der Sicherheits-ID (SID) des Benutzers fest, der die Installation ausführt. Weitere Informationen finden Sie unter [Autorisierungsstrukturen.](../secauthz/authorization-structures.md)

## <a name="default-value"></a>Standardwert

Keine.

## <a name="remarks"></a>Hinweise

Der Windows Installer legt diese Eigenschaft auf Windows 2000, Windows XP und Windows Vista fest. Diese Eigenschaft ist nicht für alle anderen Betriebssysteme definiert.

Beachten Sie, dass diese Eigenschaft über das spezielle Attribut verfügt, das sie von einer verzögerten benutzerdefinierten Aktion abgerufen werden kann. Eine benutzerdefinierte Aktion, die mit erhöhten Rechten ausgeführt wird, kann weiterhin die SID des Benutzers in der **UserSID-Eigenschaft** zurückgeben. Weitere Informationen finden Sie unter [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
