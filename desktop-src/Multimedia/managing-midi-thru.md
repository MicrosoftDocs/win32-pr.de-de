---
title: Verwalten von DABEI
description: Verwalten von DABEI
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- Instrument Digital Interface (KEYBOARD), Thru-Treiber
- KEYBOARD (Keyboard Instrument Digital Interface), Thru-Treiber
- Aufzeichnung von audio,thru driver
- KEYBOARD-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c108ac13fbbfb80d1f7c41960984c904374db31e3a790f14c326cf9e7946dac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138943"
---
# <a name="managing-midi-thru"></a>Verwalten von DABEI

Sie können einBENACHRICHTIGUNG-Eingabegerät direkt mit einem OUTPUT-Ausgabegerät verbinden. Wenn das Eingabegerät eine [**MIM \_ DATA-Nachricht**](mim-data.md) empfängt, sendet das System eine Nachricht mit denselbenBENACHRICHTIGUNG-Ereignisdaten an den Ausgabegerätetreiber. Verwenden Sie zum Verbinden eines OUTPUT-Ausgabegeräts mit einem EINGABE-Eingabegerät [**die funktion "connect".**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)

Um die bestmögliche Leistung mit mehreren Ausgaben zu erzielen, kann eine Anwendung auswählen, dass eine spezielle Form des OUTPUT-Treibers namens *thru-Treiber zur Auswahl stehen soll.* Das System lässt zwar zu, dass nur ein EINZIGES-Ausgabegerät mit einem EINGABE-Eingabegerät verbunden ist, aber es können mehrere AUDIO-Ausgabegeräte mit einem Thru-Treiber verbunden werden. Eine Anwendung auf einem solchen System könnte das EINGABE-Eingabegerät mit diesem Gerät verbinden und das DABEI-Gerät bei Bedarf mit so vielen ANMELDUNG-Ausgabegeräten verbinden. Weitere Informationen zu Treibern finden Sie in der Windows device-driver-Dokumentation.

## <a name="using-messages-to-manage-midi-recording"></a>Verwenden von Nachrichten zum Verwalten der TONT-Aufzeichnung

Die folgenden Meldungen können an eine Fenster- oder Threadrückrufprozedur zum Verwalten derTEN-Aufzeichnung gesendet werden.



| Wert                                          | Bedeutung                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ CLOSE**](mm-mim-close.md)         | Wird gesendet, wenn ein SCHLIEßEN-Eingabegerät mithilfe der [**funktion "sollInClose" geschlossen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) wird.                                      |
| [**MM \_ MIM \_ DATA**](mm-mim-data.md)           | Wird gesendet, wenn eine vollständige FEHLERMELDUNG-Nachricht empfangen wird. (Diese Meldung wird für alle MESSAGE-Nachrichten mit Ausnahme von system-exklusiven Nachrichten verwendet.)          |
| [**\_MM-MIM FEHLER \_**](mm-mim-error.md)         | Wird gesendet, wenn eine ungültige FEHLERMELDUNG-Nachricht empfangen wird. (Diese Meldung wird für alle MESSAGE-Nachrichten mit Ausnahme von system-exklusiven Nachrichten verwendet.)          |
| [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)   | Wird gesendet, wenn entweder eine vollständige SYSTEM-exklusive NACHRICHT empfangen wird oder wenn ein Puffer mit system-exklusiven Daten gefüllt wurde.     |
| [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md) | Wird gesendet, wenn eine ungültige system-exklusive FEHLERMELDUNG empfangen wird.                                                                        |
| [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)   | Wird gesendet, wenn eine Anwendung MIM [**\_ DATENnachrichten**](mim-data.md) schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu können. |
| [**MM \_ MIM \_ OPEN**](mm-mim-open.md)           | Wird gesendet, wenn ein EINGABEGERÄT mithilfe der [**funktion "sollInOpen" geöffnet**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) wird.                                        |



 

Jeder dieser Meldungen sind ein *wParam-Parameter* und ein *lParam-Parameter* zugeordnet. Der *wParam-Parameter* gibt immer das Handle eines geöffnetenWERT-Geräts an. Der *lParam-Parameter* wird für die [**MM-MIM \_ \_ CLOSE-**](mm-mim-close.md) und [**MM-MIM \_ \_ OPEN-Meldungen nicht**](mm-mim-open.md) verwendet.

Für die [**MM \_ MIM \_ LONGDATA-Nachricht**](mm-mim-longdata.md) gibt *lpMidiHdr* eine Adresse einer [**FORMATHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) an, die den Puffer für system-exklusive Nachrichten identifiziert. Der Puffer wird möglicherweise nicht vollständig gefüllt, da die Größe der system-exklusiven Nachrichten in der Regel nicht bekannt ist, bevor sie aufgezeichnet werden, und weil Puffer, deren Gesamtgröße die größte erwartete Nachricht enthalten kann, zugeordnet werden müssen. Um die Menge der gültigen Daten im Puffer zu bestimmen, verwenden Sie den **dwBytesRecorded-Member** der **FORMATHDR-Struktur.**

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Verwenden einer Rückruffunktion zum Verwalten der DANN-Aufzeichnung

Sie können eine eigene Rückruffunktion definieren, um die Aufzeichnung für EINGABE-Eingabegeräte zu verwalten. Die Rückruffunktion ist als [**"ProgrammInProc" dokumentiert.**](/previous-versions//dd798460(v=vs.85))

Die folgenden Nachrichten können an den *wMsg-Parameter* der **Rückruffunktion "SollenInProc"** gesendet werden.



| Wert                                   | Bedeutung                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_MIM Schließen**](mim-close.md)         | Wird gesendet, wenn das Gerät geschlossen wird, indem die [**funktion "formatInClose" verwendet**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) wird.                                               |
| [**\_MIM Daten**](mim-data.md)           | Wird gesendet, wenn eine vollständige DANN-Nachricht empfangen wird (diese Meldung wird für alle MESSAGE-Nachrichten mit Ausnahme von system exklusiven Nachrichten verwendet).           |
| [**\_MIM Fehler**](mim-error.md)         | Wird gesendet, wenn eine ungültige FEHLERMELDUNG-Nachricht empfangen wird (diese Meldung wird für alle MESSAGE-Nachrichten mit Ausnahme von system-exklusiven Nachrichten verwendet).           |
| [**\_MIM LONGDATA**](mim-longdata.md)   | Wird gesendet, wenn entweder eine vollständige SYSTEM-exklusive NACHRICHT empfangen wird oder wenn ein Puffer mit system-exklusiven Daten gefüllt wurde.     |
| [**\_MIM LONGERROR**](mim-longerror.md) | Wird gesendet, wenn eine ungültige system-exklusive FEHLERMELDUNG empfangen wird.                                                                        |
| [**\_MIM MOREDATA**](mim-moredata.md)   | Wird gesendet, wenn eine Anwendung MIM [**\_ DATENnachrichten**](mim-data.md) schnell genug verarbeitet, um mit dem Eingabegerätetreiber mithalten zu können. |
| [**\_MIM Öffnen**](mim-open.md)           | Wird gesendet, wenn dasEINGABE-Eingabegerät mithilfe der [**funktion "formatInOpen" geöffnet**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) wird.                                      |



 

Diese Meldungen ähneln denen, die an Fensterprozedurfunktionen gesendet werden, aber die Parameter unterscheiden sich. Ein Handle des geöffnetenWERT-Geräts wird als Parameter an die Rückruffunktion übergeben, zusammen mit dem Doubleword der Instanzdaten, die **mithilfe von "mussInOpen" übergeben wurden.**

Für die [**MIM \_ LONGDATA-Nachricht**](mim-longdata.md) gibt *lpMidiHdr* eine Adresse einer [**FORMATHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) an, die den Puffer für system-exklusive Nachrichten identifiziert. Der Puffer ist möglicherweise nicht vollständig gefüllt. Um die Menge der gültigen Daten im Puffer zu bestimmen, verwenden Sie den **dwBytesRecorded-Member** der **FORMATHDR-Struktur.**

Nachdem der Gerätetreiber mit einem Datenblock fertig ist, können Sie den Datenblock bereinigt und frei geben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von TONS-Audio](recording-midi-audio.md)
</dt> </dl>

 

 