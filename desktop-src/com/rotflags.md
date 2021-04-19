---
title: Rotflags
description: Steuert die Registrierung eines COM-Servers in der laufenden Objekttabelle (rot).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Rotflags-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342254"
---
# <a name="rotflags"></a>Rotflags

Steuert die Registrierung eines COM-Servers in der laufenden Objekttabelle (rot).

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Flagwert | Konstante                        |
|------------|---------------------------------|
| 0x1        | **rotregflags- \_ zustandsclient** |



 

### <a name="rotregflags_allowanyclient-description"></a>Rotregflags- \_ zustandsclientbeschreibung

Wenn ein com-Server in der rot registriert werden soll und jedem Client der Zugriff auf die Registrierung gestattet werden soll, muss das Flag " **rotflags \_ zugsclient** " verwendet werden. Der com-Server "aktivieren als Aktivator" kann " **rotflags \_ Zuordnungs Client** " nicht angeben, da der DCOM-Dienststeuerungs-Manager (dcomscm) eine spodüberprüfung für dieses Flag erzwingt. Daher fügt com in Windows Vista und höher Unterstützung für den **rotflags** -Registrierungs Eintrag hinzu, der es dem Server ermöglicht, festzulegen, dass seine rot-Registrierungen für jeden Client verfügbar gemacht werden.

Der Eintrag muss in der Hive des **\_ lokalen \_ HKEY** -Computers vorhanden sein. Dieser Eintrag bietet den Server "aktivieren als Aktivator" mit derselben Funktionalität, die von " **rotflags \_** " für einen runas-Server bereitstellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AppID-Schlüssel](appid-key.md)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




