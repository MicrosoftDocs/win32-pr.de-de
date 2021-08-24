---
description: Die Ereignisschnittstellen (Benachrichtigungsschnittstellen) ermöglichen einer TAPI 3-Anwendung, auf asynchrone Ereignisse zu reagieren.
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: Ereignisschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a4ecf097d761e98b723b37d9de6adcfd7ebb60696ce5e389426965534d63f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660840"
---
# <a name="event-interfaces"></a>Ereignisschnittstellen

Die Ereignisschnittstellen (Benachrichtigungsschnittstellen) ermöglichen einer TAPI 3-Anwendung, auf asynchrone Ereignisse zu reagieren.

Sie müssen die [**Methode ITTAPI::p ut \_ EventFilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) aufrufen und eine Ereignisfiltermaske festlegen, um den Empfang von Anforderungsereignissen zu ermöglichen. Wenn Sie **ITTAPI::p ut \_ EventFilter** nicht aufrufen, erhält Ihre Anwendung keine Ereignisse.

Eine Beschreibung, [wie eine Anwendung](./asynchronous-spontaneous-events.md) den Empfang von Benachrichtigungen sicherstellt, finden Sie in der Übersicht über Ereignisse. Weitere Informationen zum Festlegen einer Filtermaske für einzelne Ereignistypen finden Sie in den einzelnen Schnittstellen, die in der folgenden Tabelle aufgeführt sind.



| Schnittstelle                                                           | BESCHREIBUNG                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | Ruft die Beschreibung von Adressereignissen ab.                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | Ruft die Beschreibung der Terminalereignisse der automatischen Spracherkennung ab.                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | Ruft die Beschreibung von CallHub-Ereignissen ab.                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | Ruft die Beschreibung von Änderungsereignissen für Aufrufinformationen ab.                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | Ruft die Beschreibung von Anrufmedienereignissen ab.                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | Ruft die Beschreibung von Anrufbenachrichtigungsereignissen ab.                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | Ruft die Beschreibung von Aufrufzustandsereignissen ab.                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | Ruft Während eines Aufrufs Informationen zu DEN DIGITF-Ziffernereignissen ab.                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | Ruft Informationen zu Aufrufen ab, die die Generierung von DIGITF-Ziffern erfordern.                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | Ruft Daten ab, die sich auf die Anforderung einer Anwendung zum Erfassen von Ziffern bezieht.                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | Ruft die Beschreibung von Dateiterminalereignissen ab.                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | Ruft die Beschreibung von Konferenzteilnehmerereignissen ab.                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | Ruft die Beschreibung von Telefonereignissen ab.                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | Ruft die Beschreibung von QOS-Ereignissen (Quality of Service) ab.                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | Ruft die Beschreibung der Warteschlangenereignisse der automatischen Anrufverteilung (Automatic Call Distribution, ACD) ab.                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | Ruft die Beschreibung der Unterstützten [Telefonieanforderungsereignisse](./assisted-telephony-overview.md) ab.                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | Ruft die Beschreibung von TAPI-Objektereignissen ab.                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | Erweitert [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent); ruft einen Zeiger auf das Phone-Objekt ab, das das TAPI-Objektereignis verursacht hat. |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | Ruft Informationen zu einem Tonerkennungsereignis ab.                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | Ruft die Beschreibung von Tonterminalereignissen ab.                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | Ruft die Beschreibung von TTS-Terminalereignissen (Text-to-Speech) ab.                                                                          |



 



| Schnittstelle                                                                                             | BESCHREIBUNG                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | Benachrichtigt Clientanwendungen über Änderungen in einem anschlussbaren Terminal.                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | Registriert und aufheben die Registrierung einer Clientanwendung für Benachrichtigungen zu pluggable-Terminalereignissen. |



 

 

 
