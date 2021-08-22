---
description: Ereignisbenachrichtigung ist das primäre Mittel, mit dem eine Anwendung Informationen von TAPI und den Dienstanbietern erhält.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Ereignisbenachrichtigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a83ed721ed22049baeaf3de15626ed8deecf2a7562d883658195eb1eb590f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003668"
---
# <a name="event-notification"></a>Ereignisbenachrichtigung

Ereignisbenachrichtigung ist das primäre Mittel, mit dem eine Anwendung Informationen von TAPI und den Dienstanbietern erhält. Bei diesen Informationen kann es sich um den Status eines asynchronen Vorgangs, der von der Anwendung gestartet wird, oder um einen Prozess, der außerhalb der Anwendung gestartet wurde, wie z. B. Benachrichtigungen über neue eingehende Aufrufe.

**TAPI 2.x:** Anwendungen verarbeiten Benachrichtigungen auf eine von drei Arten: ausgeblendetes Fenster, Ereignishand handle oder Abschlussport. Weitere Informationen zu diesen Benachrichtigungsmechanismen finden Sie im Abschnitt "Hinweise" für [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Eine Anwendung gibt den Mechanismus an, indem das **dwOptions-Element** der [**LINEINITIALIZEEXPARAMS-Struktur**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) vor dem Aufruf von [**lineInitializeEx festgelegt wird.**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)

Mit [**der lineSetStatusMessages-Funktion**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) kann eine Anwendung angeben, welche Benachrichtigungsmeldungen für Ereignisse im Zusammenhang mit Statusänderungen für die angegebene Zeile oder eine ihrer Adressen empfangen werden sollen.

**TAPI 3.x:** Anwendungen verarbeiten allgemeine Benachrichtigungen mithilfe von [COM-Standard-Verbindungsobjekten.](../com/events-in-com-and-connectable-objects.md) [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) ist die ausgehende Schnittstelle, die beim Containerobjekt von TAPI registriert werden muss, und [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) ist die TapI-Methode, um die Antwort der Anwendung zu bestimmen. Die [**Methode ITTAPI::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) teilt TAPI mit, welche Ereignisse für die Anwendung von Interesse sind. Wenn kein Ereignisfilter eingegeben wird, erhält die Anwendung keine Benachrichtigung über Ereignisse. Die [**ITTAPI::RegisterCallNotifications-Methode**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) teilt TAPI die Medientypen und Adressen mit, für die die Anwendung eingehende Sitzungen verarbeitet. Weitere Informationen zur TAPI 3-Ereignisbehandlung finden Sie in der Übersicht über Ereignisse oder im [Codebeispiel Zum Registrieren](register-events.md) von Ereignissen. [](events.md)

Telefoniedienstanbieter implementieren [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) und [**TSPI \_ lineSetStatusMessages.**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) TAPI ruft diese Funktionen auf, um den Satz aller Zeilen-, Adress- und Medientypereignisse anzugeben, die von Anwendungen angefordert werden.

 

 
