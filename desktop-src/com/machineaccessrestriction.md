---
title: MachineAccessRestriction
description: Legt die Computer weite Einschränkungs Richtlinie für den Komponenten Zugriff fest.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Machineaccesseinschränkung-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342289"
---
# <a name="machineaccessrestriction"></a>MachineAccessRestriction

Legt die Computer weite Einschränkungs Richtlinie für den Komponenten Zugriff fest.

> [!Caution]  
> Wenn Sie diesen Wert ändern, wirkt sich dies auf alle com-Server Anwendungen aus und kann die ordnungsgemäße Ausführung verhindern. Wenn es com-Server Anwendungen gibt, die Einschränkungen aufweisen, die weniger streng sind als die Computer weiten Einschränkungen, können diese Anwendungen durch eine Reduzierung der Computer weiten Einschränkungen für unerwünschte Zugriffe zugänglich gemacht werden. Wenn Sie dagegen die Computer weiten Einschränkungen erhöhen, können einige com-Server Anwendungen nicht mehr durch das Aufrufen von Anwendungen aufgerufen werden.

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg- \_ Binärwert** .

Prinzipale, die hier nicht über Berechtigungen verfügen, können diese auch dann nicht abrufen, wenn die Berechtigungen durch den Registrierungs Wert [DefaultAccessPermission](defaultaccesspermission.md) oder durch die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion erteilt werden.

Standardmäßig können Mitglieder der Gruppe "jeder" Berechtigungen für den lokalen Zugriff und den Remote Zugriff erhalten, und anonyme Benutzer können lokale Zugriffsberechtigungen erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




