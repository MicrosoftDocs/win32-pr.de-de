---
title: Donotaddallapplicationpackagestorestrictions
description: Bestimmt, ob RPCSS standardmäßig automatisch eine \_ \_ sid für alle Anwendungspakete an com-Einschränkungen anfügt.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388035"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>Donotaddallapplicationpackagestorestrictions

Bestimmt, ob RPCSS standardmäßig automatisch eine \_ \_ sid für alle Anwendungspakete an com-Einschränkungen anfügt.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert | BESCHREIBUNG                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Deaktiviert Windows Store-Apps bei der Migration von Windows 7 zu Windows 8.                   |
| 1     | Die \_ sid für alle Anwendungspakete wird nicht \_ zu com-Einschränkungen hinzugefügt. Dies ist die Standardoption. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




