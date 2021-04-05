---
title: Loadusersettings
description: Bestimmt, ob com das Benutzerprofil für com-Server lädt, die als Anwendungs Identität des Anwendungs Starts ausgeführt werden.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- Loadusersettings-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947912"
---
# <a name="loadusersettings"></a>Loadusersettings

Bestimmt, ob com das Benutzerprofil für com-Server lädt, die als Anwendungs Identität des Anwendungs Starts ausgeführt werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert. Wenn *value* ungleich NULL ist, lädt com das Profil des Benutzerkontos, mit dem der com-Server gestartet wird. Wenn der *Wert* 0 (null) oder nicht vorhanden ist, lädt com das Profil des Benutzerkontos nicht, mit dem der com-Server gestartet wird.

Diese Einstellung wird ignoriert, wenn ein [**runas**](runas.md) -Eintrag vorhanden ist.

 

 




