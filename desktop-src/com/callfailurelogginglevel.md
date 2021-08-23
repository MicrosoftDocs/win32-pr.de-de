---
title: CallFailureLoggingLevel
description: Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu fehlgeschlagenen Aufrufen von Komponenten fest.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- CallFailureLoggingLevel-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819d132a8cd0f1741eb3b825a17f02387b200e80f2dba6913821e77f9a0913cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793820"
---
# <a name="callfailurelogginglevel"></a>CallFailureLoggingLevel

Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu fehlgeschlagenen Aufrufen von Komponenten fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert | BESCHREIBUNG                                                                            |
|-------|----------------------------------------------------------------------------------------|
| 1     | Protokollieren Sie Fehler immer während eines Aufrufs im COM-Serverprozess.                           |
| 2     | Protokollieren Sie während eines Aufrufs im COM-Serverprozess niemals Fehler. Dies ist der Standardwert. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




