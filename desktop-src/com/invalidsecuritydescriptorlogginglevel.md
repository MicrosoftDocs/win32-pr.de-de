---
title: Invalidsecuritydescriptor LoggingLevel
description: Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen über ungültige Sicherheits Deskriptoren für die Start-und Zugriffsberechtigungen der Komponente fest.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Invalidsecuritydescriptor LoggingLevel-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309180"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>Invalidsecuritydescriptor LoggingLevel

Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen über ungültige Sicherheits Deskriptoren für die Start-und Zugriffsberechtigungen der Komponente fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert | BESCHREIBUNG                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Fehler immer protokollieren, wenn com einen ungültigen Sicherheits Deskriptor findet. Dies ist der Standardwert.                                                                                  |
| 2     | Fehler werden nie protokolliert, wenn com einen ungültigen Sicherheits Deskriptor findet. Es wird nicht empfohlen, die Ereignisprotokollierung zu deaktivieren, da dadurch die Diagnose von Problemen erschwert werden kann. |



 

Wenn Sie die Sicherheits Deskriptoren für die Start-und Zugriffsberechtigung (häufig als ACLs bezeichnet) direkt festlegen, ist es möglich, eine Sicherheits Beschreibung zu erstellen, deren Bedeutung nicht eindeutig interpretiert werden kann. COM führt einen Ereignisprotokoll Eintrag aus, wenn ein solcher Ungültiger Sicherheits Deskriptor auftritt.

Beachten Sie, dass [**activationfailurelogginglevel**](activationfailurelogginglevel.md) und [**CallFailureLoggingLevel**](callfailurelogginglevel.md) keine Kontrolle über die Protokollierung ungültiger Sicherheits deskriptorfehler haben. Verwenden Sie **invalidsecuritydescriptor LoggingLevel** , um die vollständige Kontrolle über diese Funktionalität zu haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




