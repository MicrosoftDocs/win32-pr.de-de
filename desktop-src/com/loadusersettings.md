---
title: LoadUserSettings
description: Bestimmt, ob COM das Benutzerprofil für COM-Server lädt, die als startende Benutzeranwendungsidentität ausgeführt werden.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- LoadUserSettings-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b82bd89015baa4c73c9200013e49c76523951218dfde62bbe39300eefdfe0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731040"
---
# <a name="loadusersettings"></a>LoadUserSettings

Bestimmt, ob COM das Benutzerprofil für COM-Server lädt, die als startende Benutzeranwendungsidentität ausgeführt werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.** Wenn *der Wert* ungleich 0 (null) ist, lädt COM das Profil des Benutzerkontos, mit dem der COM-Server gestartet wird. Wenn *der Wert* 0 (null) oder nicht vorhanden ist, lädt COM nicht das Profil des Benutzerkontos, mit dem der COM-Server gestartet wird.

Diese Einstellung wird ignoriert, wenn ein [**RunAs-Eintrag**](runas.md) vorhanden ist.

 

 




