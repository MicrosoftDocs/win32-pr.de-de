---
title: LaunchPermission
description: Beschreibt die Access Control -Liste (ACL) der Prinzipale, die neue Server für diese Klasse starten können. Dieser Wert kann unter jedem AppID-Schlüssel hinzugefügt werden, um die Aktivierung durch Remoteclients bestimmter Klassen zu beschränken.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- LaunchPermission-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5967ee63288b11edca017820b9a367dd4e6c017e993330616e633e7448a098b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756100"
---
# <a name="launchpermission"></a>LaunchPermission

Beschreibt die Access Control -Liste (ACL) der Prinzipale, die neue Server für diese Klasse starten können. Dieser Wert kann unter jedem [**AppID-Schlüssel hinzugefügt**](appid-key.md) werden, um die Aktivierung durch Remoteclients bestimmter Klassen zu beschränken.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ BINARY-Wert.** Beim Empfang einer lokalen oder Remoteanforderung zum Starten des Servers dieser Klasse wird die durch diesen Wert beschriebene ACL beim Identitätswechsel des Clients überprüft, und ihr Erfolg lässt entweder das Starten des Servers zu oder nicht zu. Wenn dieser Wert nicht vorhanden ist, wird [**der DefaultLaunchPermission-Wert**](defaultlaunchpermission.md) auf die gleiche Weise überprüft, um zu bestimmen, ob der Klassencode gestartet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




