---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Bestimmt, ob RPCSS standardmäßig automatisch eine \_ ALL APPLICATION \_ PACKAGES-SID an COM-Einschränkungen anfügt.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1608d49d7e5bebc977ace8e59e4b31c5b13da8ab4f743e89095b9f31632453c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737006"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Bestimmt, ob RPCSS standardmäßig automatisch eine \_ ALL APPLICATION \_ PACKAGES-SID an COM-Einschränkungen anfügt.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert | BESCHREIBUNG                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Deaktiviert Windows Store Apps bei der Migration von Windows 7 zu Windows 8.                   |
| 1     | Fügt com-Einschränkungen nicht die SID ALL \_ APPLICATION \_ PACKAGES hinzu. Dies ist die Standardoption. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




