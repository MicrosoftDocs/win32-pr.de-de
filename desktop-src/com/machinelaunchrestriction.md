---
title: MachineLaunchRestriction
description: Legt die Computer weite Einschränkungs Richtlinie für das Starten und Aktivieren von Komponenten fest.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Machinelauncheinschränkungs-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207263"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Legt die Computer weite Einschränkungs Richtlinie für das Starten und Aktivieren von Komponenten fest.

> [!Caution]  
> Wenn Sie diesen Wert ändern, wirkt sich dies auf alle com-Server Anwendungen aus und kann die ordnungsgemäße Ausführung verhindern. Wenn es com-Server Anwendungen gibt, die Einschränkungen aufweisen, die weniger streng sind als die Computer weiten Einschränkungen, können diese Anwendungen durch eine Reduzierung der Computer weiten Einschränkungen für unerwünschte Zugriffe zugänglich gemacht werden. Wenn Sie dagegen die Computer weiten Einschränkungen erhöhen, können einige com-Server Anwendungen nicht mehr durch das Aufrufen von Anwendungen aufgerufen werden.

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg- \_ Binärwert** .

Prinzipale, die hier nicht über Berechtigungen verfügen, können diese auch dann nicht abrufen, wenn die Berechtigungen durch den Registrierungs Wert [DefaultAccessPermission](defaultaccesspermission.md) oder durch die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion erteilt werden.

Standardmäßig können Administratoren lokale und Remote Start-und Aktivierungs Berechtigungen erhalten, und Mitglieder der Gruppe Jeder können lokale Aktivierungs-und Start Berechtigungen erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




