---
description: Der Systemereignisbenachrichtigungsdienst (SENS) definiert die SENS-Co-Klasse als Teil der SENS-Typbibliothek.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: SENS-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acdf70b5e2229051d569bd1f607ad8db5d3d567b4c0421464757f02bc6a8e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003948"
---
# <a name="sens-object"></a>SENS-Objekt

Der Systemereignisbenachrichtigungsdienst (SENS) definiert die SENS-Co-Klasse als Teil der SENS-Typbibliothek.

## <a name="implementation"></a>Implementierung

Die SENS-Objektimplementierung wird vom Betriebssystem bereitgestellt.

## <a name="creationaccess-functions"></a>Erstellungs-/Zugriffsfunktionen



| Funktion                                      | Beschreibung                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | Erstellt eine Instanz des SENS-Objekts mithilfe seiner CLSID. |



 

## <a name="interfaces"></a>Schnittstellen



| Schnittstelle                            | BESCHREIBUNG                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IsensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | Standard. Ausgehende Schnittstelle, die vom Senkenobjekt in der Abonnentenanwendung implementiert wird.                   |
| [**IsensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | Ausgehende Schnittstelle, die vom Senkenobjekt in der Abonnentenanwendung implementiert wird.                            |
| [**IsensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | Ausgehende Schnittstelle, die vom Senkenobjekt in der Abonnentenanwendung implementiert wird.                            |
| [**IsensLogon2**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | Ausgehende Schnittstelle, die vom Senkenobjekt in der Abonnentenanwendung implementiert wird. Verfügbar mit Windows XP. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[Informationen zum Systemereignisbenachrichtigungsdienst](about-system-event-notification-service.md)
</dt> </dl>

 

 
