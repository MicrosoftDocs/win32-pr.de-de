---
description: Der System Event Notification Service (Sens) definiert die Sens-Co-Klasse als Teil der Sens-Typbibliothek.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Sens-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356971"
---
# <a name="sens-object"></a>Sens-Objekt

Der System Event Notification Service (Sens) definiert die Sens-Co-Klasse als Teil der Sens-Typbibliothek.

## <a name="implementation"></a>Implementierung

Die Sens-Objekt Implementierung wird vom Betriebssystem bereitgestellt.

## <a name="creationaccess-functions"></a>Erstellungs-/Zugriffs Funktionen



| Funktion                                      | BESCHREIBUNG                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Erstellt eine Instanz des Sens-Objekts unter Verwendung der zugehörigen CLSID. |



 

## <a name="interfaces"></a>Schnittstellen



| Schnittstelle                            | BESCHREIBUNG                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Isensnetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Standard. Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert                   |
| [**Isennow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert                            |
| [**Isenslogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Ausgehende Schnittstelle, die vom Sink-Objekt in der Abonnenten Anwendung implementiert Verfügbar in Windows XP. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Isenslogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**Isensnetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**Isennow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[Informationen zum System Ereignis Benachrichtigungsdienst](about-system-event-notification-service.md)
</dt> </dl>

 

 
