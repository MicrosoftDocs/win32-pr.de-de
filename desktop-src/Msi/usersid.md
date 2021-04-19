---
description: Das Installationsprogramm legt den Wert der UserSID-Eigenschaft auf die Zeichen folgen Darstellung der Sicherheits-ID (SID) des Benutzers fest, der die Installation durchführt. Weitere Informationen finden Sie unter Autorisierungs Strukturen.
ms.assetid: 94524636-c7f2-4de2-b35e-644c0c171193
title: UserSID-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fab01b3f87c654a306bfe3633adf0973ed58aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355899"
---
# <a name="usersid-property"></a>UserSID-Eigenschaft

Das Installationsprogramm legt den Wert der **UserSID** -Eigenschaft auf die Zeichen folgen Darstellung der Sicherheits-ID (SID) des Benutzers fest, der die Installation durchführt. Weitere Informationen finden Sie unter [Autorisierungs Strukturen](../secauthz/authorization-structures.md).

## <a name="default-value"></a>Standardwert

Keine.

## <a name="remarks"></a>Bemerkungen

Der Windows Installer diese Eigenschaft auf Windows 2000, Windows XP und Windows Vista festlegen. Diese Eigenschaft ist nicht für alle anderen Betriebssysteme definiert.

Beachten Sie, dass diese Eigenschaft über das spezielle Attribut verfügt, das Sie aus einer verzögerten benutzerdefinierten Aktion abrufen kann. Eine benutzerdefinierte Aktion, die mit erhöhten Rechten ausgeführt wird, kann weiterhin die SID des Benutzers in der **UserSID** -Eigenschaft zurückgeben. Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
