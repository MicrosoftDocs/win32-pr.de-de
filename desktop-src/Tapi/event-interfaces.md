---
description: Mit den Ereignis Schnittstellen (Benachrichtigungs Schnittstellen) kann eine TAPI 3-Anwendung auf asynchrone Ereignisse reagieren.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Ereignis Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7b705c89988ff62d972e594ceb936bb01db78e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526318"
---
# <a name="event-interfaces"></a>Ereignis Schnittstellen

Mit den Ereignis Schnittstellen (Benachrichtigungs Schnittstellen) kann eine TAPI 3-Anwendung auf asynchrone Ereignisse reagieren.

Sie müssen die Ereignis [**\_ Filter-Methode ittapi::p UT**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) und eine Ereignis Filtermaske festlegen, um den Empfang von Anforderungs Ereignissen zu aktivieren. Wenn Sie **ittapi::p UT \_ EventFilter** nicht anrufen, empfängt Ihre Anwendung keine Ereignisse.

In der Übersicht über [Ereignisse](./asynchronous-spontaneous-events.md) finden Sie eine Beschreibung der Art und Weise, wie eine Anwendung den Empfang von Benachrichtigungen sicherstellt. Weitere Informationen zum Festlegen einer Filtermaske für einzelne Ereignis Typen finden Sie in den einzelnen Schnittstellen, die in der folgenden Tabelle aufgeführt sind.



| Schnittstelle                                                           | BESCHREIBUNG                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Itadressssevent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Ruft die Beschreibung der Adress Ereignisse ab.                                                                                                |
| [**Itasrterminalevent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Ruft die Beschreibung der automatischen sprechererkennungs-Terminal Ereignisse ab.                                                                  |
| [**Itcallhubevent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Ruft die Beschreibung von callhub-Ereignissen ab.                                                                                                |
| [**Itcallinfochangeevent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Ruft die Beschreibung der Änderungs Ereignisse für Ereignis Aufrufe ab.                                                                                |
| [**Itcallmediaevent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Ruft die Beschreibung der Ereignisse für das Abrufen von Medien ab.                                                                                             |
| [**Itcallnotificationevent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Ruft die Beschreibung der Ereignis Benachrichtigungs Ereignisse ab.                                                                                      |
| [**Itcallstateevent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Ruft die Beschreibung der Aufrufe von Zustands Ereignissen ab.                                                                                             |
| [**Itdigitdetectionevent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Ruft Informationen zu DTMF-Ziffern Ereignissen während eines-Aufrufes ab.                                                                                |
| [**Itdigitgenerationevent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Ruft Informationen zu Aufrufen ab, die die Generierung von DTMF-Ziffern erfordern.                                                               |
| [**Itdigiungsgatherede Vent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Ruft Daten ab, die sich auf die Anforderung zur Ziffern Erfassung einer Anwendung beziehen.                                                                         |
| [**Itfileterminalevent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Ruft die Beschreibung der Datei Terminal Ereignisse ab.                                                                                          |
| [**Itparticipvorgänger Vent**](./itparticipantevent.md)           | Ruft die Beschreibung der Konferenzteilnehmer Ereignisse ab.                                                                                 |
| [**Itphoneevent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Ruft die Beschreibung der Telefon Ereignisse ab.                                                                                                  |
| [**Itqoabvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Ruft die Beschreibung der QoS-Ereignisse (Quality of Service) ab.                                                                               |
| [**Itqueueevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Ruft die Beschreibung der Warteschlangen Ereignisse für die automatische aufrufsverteilung (ACD) ab.                                                                |
| [**Itrequestevent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Ruft die Beschreibung der unter [stützten telefonieanforderungsereignisse](./assisted-telephony-overview.md) ab.                                 |
| [**Ittapiobjectevent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Ruft die Beschreibung von TAPI-Objekt Ereignissen ab.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Erweitert [**ittapiobjectevent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); Ruft einen Zeiger auf das Telefon Objekt ab, das das TAPI-Objekt Ereignis verursacht hat. |
| [**Ittonedetectionevent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Ruft Informationen zu einem Tone-Erkennungs Ereignis ab.                                                                                         |
| [**Ittoneterminalevent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Ruft die Beschreibung der Tone-Terminal Ereignisse ab.                                                                                          |
| [**Itttsterminalevent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Ruft die Beschreibung der Terminal Ereignisse von Text-zu-Sprache (TTS) ab.                                                                          |



 



| Schnittstelle                                                                                             | BESCHREIBUNG                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Itpluggableterminaleventsink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Benachrichtigt Client Anwendungen über Änderungen in einem austauschbaren Terminal.                              |
| [**Itpluggableterminaleventsink Registration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Registriert eine Client Anwendung und hebt die Registrierung für Benachrichtigungen über austauschbare Terminal Ereignisse auf. |



 

 

 
