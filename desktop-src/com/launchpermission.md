---
title: Launchberechtigung
description: Beschreibt die Access Control Liste (ACL) der Prinzipale, die neue Server für diese Klasse starten können. Dieser Wert kann unter jedem AppID-Schlüssel hinzugefügt werden, um die Aktivierung durch Remote Clients bestimmter Klassen einzuschränken.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Launchberechtigungs-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037613"
---
# <a name="launchpermission"></a>Launchberechtigung

Beschreibt die Access Control Liste (ACL) der Prinzipale, die neue Server für diese Klasse starten können. Dieser Wert kann unter jedem [**AppID**](appid-key.md) -Schlüssel hinzugefügt werden, um die Aktivierung durch Remote Clients bestimmter Klassen einzuschränken.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg- \_ Binärwert** . Wenn eine lokale oder eine Remote Anforderung zum Starten des Servers dieser Klasse empfangen wird, wird die durch diesen Wert beschriebene ACL während der Identität des Clients aktiviert, und Ihr Erfolg erlaubt oder verweigert das Starten des Servers. Wenn dieser Wert nicht vorhanden ist, wird der [**defaultlaunchberechtigungswert**](defaultlaunchpermission.md) auf dieselbe Weise überprüft, um zu bestimmen, ob der Klassen Code gestartet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




