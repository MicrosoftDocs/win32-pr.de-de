---
description: Die ordnungsgemäße Funktionsweise von TAPI-Komponenten erfordert das Einrichten der Kommunikationsumgebung auf einem Computer.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: TAPI-Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f9062f8440cdec6597d21a2141a24b12f69bc9e940e189965d9e73880c54c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659900"
---
# <a name="tapi-initialization"></a>TAPI-Initialisierung

Für die ordnungsgemäße Funktionsweise von TAPI-Komponenten muss die Kommunikationsumgebung wie folgt auf einem Computer eingerichtet werden:

-   [Die Installation](installation.md) wird ausgeführt, wenn dem Computer zum ersten Mal Software oder Hardware hinzugefügt wird. Ausführliche Verfahren hängen vom Betriebssystem und der Software selbst ab.
-   [Die primäre Initialisierung](primary-initialization.md) erstellt die Objekte und Kommunikationspfade.
-   [Die Versionsaushandlung](version-negotiation.md) stellt sicher, dass TAPI-Komponenten Daten austauschen können.
-   [Die Ressourceninventur](resource-inventory.md) ruft Informationen zu Geräten ab, die von einer TAPI-Anwendung verwendet werden können.
-   [Ereignisbenachrichtigung](event-notification.md) gibt an, wie TAPI und die Dienstanbieter asynchrone Vorgangsergebnisse und Zustandsänderungsinformationen an die Anwendung übergeben.

## <a name="summary-of-related-reference-pages"></a>Zusammenfassung verwandter Referenzseiten



| TAPI 2.x-Funktionen                                        | Beschreibung                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Richtet die Telefonieumgebung ein, gibt das Anwendungshand handle und die Geräteanzahl zurück.                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Ruft Gerätefunktionen ab, z. B. die TAPI-Version oder unterstützte Medientypen.                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Ruft Adressfunktionen ab, z. B. ob Callpark unterstützt wird.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Benachrichtigt TAPI darüber, dass die Anwendung die Zeile und in welcher Weise verwendet.                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Gibt die nächste TAPI-Nachricht zurück, die für die Übermittlung an eine Anwendung in der Warteschlange steht, die den Benachrichtigungsmechanismus ereignishandpunkt verwendet. |



 



| TAPI 3.x-Schnittstellen oder -Methoden                                                | Beschreibung                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Richtet eine Telefonieumgebung ein.                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Hier werden die derzeit verfügbaren Adressen aufzählt.                                                                                                  |
| [**ITTAPI::get \_ Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Erstellt eine Auflistung der derzeit verfügbaren Adressen. Wird für Automation-Clientanwendungen bereitgestellt, z. B. solche, die in Visual Basic. |
| [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Bestimmt die Antwort auf eine asynchrone Ereignisbenachrichtigung. Wird von der Anwendung implementiert, die von TAPI aufgerufen wird.                                |
| [**ITTAPI::put \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Legt die Ereignisfiltermaske fest, die TAPI benachrichtigt, welche Ereignisse für die Anwendung erforderlich sind.                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Weist TAPI an, die eingehenden Anwendungssitzungen für eine angegebene Adresse und einen Satz von Medientypen zu übergeben.                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Ermöglicht einer Anwendung, die Medienunterstützungsfunktionen für eine Adresse zu entdecken.                                                           |



 

 

 
