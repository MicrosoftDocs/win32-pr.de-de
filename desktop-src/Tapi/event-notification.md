---
description: Die Ereignis Benachrichtigung ist das primäre Mittel, mit dem eine Anwendung Informationen von TAPI und den Dienstanbietern abruft.
ms.assetid: 02160f10-dc3f-484c-9cd3-bcfb07ded822
title: Ereignisbenachrichtigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aa232b0e712a76442c298ea04e24ec7671cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362219"
---
# <a name="event-notification"></a>Ereignisbenachrichtigung

Die Ereignis Benachrichtigung ist das primäre Mittel, mit dem eine Anwendung Informationen von TAPI und den Dienstanbietern abruft. Diese Informationen sind möglicherweise der Status eines asynchronen Vorgangs, der von der Anwendung ausgelöst wird, oder ein Prozess, der außerhalb der Anwendung gestartet wird, z. b. Benachrichtigungen über neue eingehende Anrufe.

**TAPI 2. x:** Anwendungen verarbeiten eine Benachrichtigung auf eine von drei Arten: ausgeblendetes Fenster, Ereignis handle oder Beendigungs Port. Weitere Informationen zu diesen Benachrichtigungsmechanismen finden Sie im Abschnitt "Hinweise" für [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Eine Anwendung gibt den Mechanismus an, indem der **dwOptions** -Member der [**lineinitializeexparameams**](/windows/win32/api/tapi/ns-tapi-lineinitializeexparams) -Struktur vor dem Aufrufen von [**lineinitializeex**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)festgelegt wird.

Die [**linesetstatusmessages**](/windows/win32/api/tapi/nf-tapi-linesetstatusmessages) -Funktion ermöglicht es einer Anwendung, anzugeben, welche Benachrichtigungs Meldungen für Ereignisse im Zusammenhang mit Statusänderungen für die angegebene Zeile oder eine Ihrer Adressen empfangen werden sollen.

**TAPI 3. x:** Anwendungen verarbeiten allgemeine Benachrichtigungen mithilfe von [Verbindungs fähigen](../com/events-in-com-and-connectable-objects.md)com-Standardobjekten. [**Ittapieventnotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) ist die ausgehende Schnittstelle, die mit dem-Container Objekt von TAPI registriert werden muss, und [**ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) ist die Methode TAPI-Aufrufe, um die Antwort der Anwendung zu bestimmen. Die [**ittapi::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) -Methode teilt TAPI mit, welche Ereignisse für die Anwendung von Interesse sind. Wenn kein Ereignis Filter eingegeben wird, empfängt die Anwendung keine Benachrichtigung über Ereignisse. Die [**ittapi:: registercallnotification**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) -Methode weist TAPI die Medientypen und-Adressen zu, für die die Anwendung eingehende Sitzungen behandelt. Weitere Informationen zur TAPI-3-Ereignis Behandlung finden Sie in der Übersicht über [Ereignisse](events.md) oder im Codebeispiel zum [Registrieren von Ereignissen](register-events.md) .

Telefoniedienstanbieter implementieren [**TSPI \_ linesetdefaultmediadetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) und [**TSPI \_ linesetstatus-Meldungen**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages). TAPI ruft diese Funktionen auf, um den Satz aller Zeilen-, Adress-und Medientyp Ereignisse anzugeben, die von Anwendungen angefordert werden.

 

 
