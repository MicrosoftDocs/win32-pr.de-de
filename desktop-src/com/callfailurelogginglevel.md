---
title: CallFailureLoggingLevel
description: Legt die Ausführlichkeit von Ereignisprotokoll Einträgen zu fehlgeschlagenen Aufrufen von-Komponenten fest.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- CallFailureLoggingLevel-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855887"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Legt die Ausführlichkeit von Ereignisprotokoll Einträgen zu fehlgeschlagenen Aufrufen von-Komponenten fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert | BESCHREIBUNG                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Fehler während eines Aufrufes im com-Server Prozess immer protokollieren.                           |
| 2     | Fehler während eines Aufrufes im com-Server Prozess nie protokollieren. Dies ist der Standardwert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




