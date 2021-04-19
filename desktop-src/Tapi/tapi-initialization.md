---
description: Die ordnungsgemäße Funktionsweise von TAPI-Komponenten erfordert das Einrichten der Kommunikationsumgebung auf einem Computer.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: TAPI-Initialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973d67931fb9f33751fedc638ab77021d3d3d34c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359481"
---
# <a name="tapi-initialization"></a>TAPI-Initialisierung

Die ordnungsgemäße Funktionsweise von TAPI-Komponenten erfordert das Einrichten der Kommunikationsumgebung auf einem Computer wie folgt:

-   Die [Installation](installation.md) wird ausgeführt, wenn dem Computer zuerst Software oder Hardware hinzugefügt wird. Ausführliche Verfahren richten sich nach dem Betriebssystem und der Software selbst.
-   Die [primäre Initialisierung](primary-initialization.md) erstellt die Objekte und die Kommunikations Pfade.
-   Mit der [Versions Aushandlung](version-negotiation.md) wird sichergestellt, dass TAPI-Komponenten Daten austauschen können.
-   [Ressourcen Inventur](resource-inventory.md) Ruft Informationen zu Geräten ab, die von einer TAPI-Anwendung verwendet werden können.
-   Die [Ereignis Benachrichtigung](event-notification.md) gibt an, wie TAPI und die Dienstanbieter asynchrone Vorgangs Ergebnisse und Zustands Änderungs Informationen an die Anwendung übergeben.

## <a name="summary-of-related-reference-pages"></a>Zusammenfassung verwandter Referenzseiten



| TAPI 2. x-Funktionen                                        | BESCHREIBUNG                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Richtet die Telefonieumgebung ein, gibt Anwendungs Handle und Geräte Anzahl zurück.                                                   |
| [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Ruft Gerätefunktionen ab, wie z. b. TAPI-Version oder Unterstützte Medientypen.                                                          |
| [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Ruft Adress Funktionen ab, z. b., ob callpark unterstützt wird.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Benachrichtigt TAPI, dass die Anwendung die-Zeile verwendet und auf welche Weise.                                                       |
| [**linegetmessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Gibt die nächste TAPI-Nachricht zurück, die für die Übermittlung an eine Anwendung in die Warteschlange gestellt wird, die den Benachrichtigungs Mechanismus für Ereignis Handles |



 



| TAPI 3. x-Schnittstellen oder-Methoden                                                | BESCHREIBUNG                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ittapi:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Richtet eine Telefonieumgebung ein.                                                                                                             |
| [**Ittapi:: enumerateadressen**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Listet aktuell verfügbare Adressen auf.                                                                                                  |
| [**Ittapi:: get- \_ Adressen**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Erstellt eine Sammlung von Adressen, die derzeit verfügbar sind. Wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. die in Visual Basic geschriebenen. |
| [**Ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Bestimmt die Antwort auf eine asynchrone Ereignis Benachrichtigung. Implementiert von der Anwendung, die von TAPI aufgerufen wird.                                |
| [**Ittapi::p UT- \_ Ereignis Filter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Legt die Ereignis Filtermaske fest, die TAPI benachrichtigt, welche Ereignisse für die Anwendung erforderlich sind.                                                     |
| [**Ittapi:: registercallbenachrichtigungen**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Weist TAPI an, die eingehenden Anwendungs Sitzungen für eine angegebene Adresse und einen Satz von Medientypen zu übergeben.                                   |
| [**Itmediasupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Ermöglicht es einer Anwendung, die Medien Unterstützungsfunktionen für eine Adresse zu ermitteln.                                                           |



 

 

 
