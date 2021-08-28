---
title: InvalidSecurityDescriptorLoggingLevel
description: Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu ungültigen Sicherheitsbeschreibungen für Komponentenstart- und Zugriffsberechtigungen fest.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- InvalidSecurityDescriptorLoggingLevel-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c2362b38c19acd8d895e5fa9640475fa401a7d5bd88c8016056df2d22c3a579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854340"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu ungültigen Sicherheitsbeschreibungen für Komponentenstart- und Zugriffsberechtigungen fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert | BESCHREIBUNG                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Protokollieren Sie Immer Fehler, wenn COM einen ungültigen Sicherheitsdeskriptor findet. Dies ist der Standardwert.                                                                                  |
| 2     | Protokollieren Sie niemals Fehler, wenn COM einen ungültigen Sicherheitsdeskriptor findet. Es wird nicht empfohlen, die Ereignisprotokollierung zu deaktivieren, da dies die Diagnose von Problemen erschweren kann. |



 

Wenn Sie Sicherheitsbeschreibungen für Start- und Zugriffsberechtigungen (häufig als ACLs bezeichnet) direkt festlegen, ist es möglich, einen Sicherheitsdeskriptor zu erstellen, dessen Bedeutung nicht eindeutig interpretiert werden kann. COM nimmt einen Ereignisprotokolleintrag vor, wenn ein solcher ungültiger Sicherheitsdeskriptor gefunden wird.

Beachten Sie, dass [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) und [**CallFailureLoggingLevel**](callfailurelogginglevel.md) keine Kontrolle über die Protokollierung ungültiger Sicherheitsbeschreibungsfehler haben. Verwenden Sie **InvalidSecurityDescriptorLoggingLevel, um** die vollständige Kontrolle über diese Funktionalität zu haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




