---
title: Verwalten von MIDI-Thru
description: Verwalten von MIDI-Thru
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- Digital Instrumentation Digital Interface (MIDI), Thru-Treiber
- MIDI (Digital Interface Digital Interface), Thru-Treiber
- Aufzeichnen von MIDI-Audiodaten, Thru-Treiber
- MIDI-Thru-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948633"
---
# <a name="managing-midi-thru"></a>Verwalten von MIDI-Thru

Sie können ein MIDI-Eingabegerät direkt mit einem MIDI-Ausgabegerät verbinden, damit das System, wenn das Eingabegerät eine [**MIM- \_ Daten**](mim-data.md) Nachricht empfängt, eine Nachricht mit denselben Daten vom Typ "MIDI" an den Ausgabegeräte Treiber sendet. Verwenden Sie die [**midiconnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) -Funktion, um ein MIDI-Ausgabegerät mit einem MIDI-Eingabegerät zu verbinden.

Um die bestmögliche Leistung mit mehreren Ausgaben zu erzielen, kann eine Anwendung eine spezielle Form des Ausgabe Treibers von MIDI bereitstellen, die als " *Thru Driver*" bezeichnet wird. Obwohl das System zulässt, dass nur ein Paket mit einem MIDI-Ausgabegerät mit einem MIDI-Eingabegerät verbunden ist, können mehrere MIDI-Ausgabegeräte mit einem Thru-Treiber verbunden werden. Eine Anwendung auf einem solchen System kann das MIDI-Eingabegerät mit diesem Geräte-Gerät verbinden und das Gerät vom Typ "MIDI Thru" mit so vielen, bei Bedarf mit so vielen MIDI-Ausgabegeräten verbinden Weitere Informationen zu Thru-Treibern finden Sie in der Dokumentation zu Windows-Gerätetreibern.

## <a name="using-messages-to-manage-midi-recording"></a>Verwenden von Nachrichten zum Verwalten der MIDI-Aufzeichnung

Die folgenden Nachrichten können an ein Fenster oder eine Thread Rückruf Prozedur zum Verwalten der MIDI-Aufzeichnung gesendet werden.



| Wert                                          | Bedeutung                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ Schließen**](mm-mim-close.md)         | Wird gesendet, wenn ein MIDI-Eingabegerät mithilfe der [**midiinclose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) -Funktion geschlossen wird.                                      |
| [**MM \_ MIM- \_ Daten**](mm-mim-data.md)           | Wird gesendet, wenn eine komplette MIDI-Nachricht empfangen wird. (Diese Meldung wird für alle MIDI-Nachrichten mit Ausnahme von System exklusiven Nachrichten verwendet.)          |
| [**MM \_ MIM- \_ Fehler**](mm-mim-error.md)         | Wird gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird. (Diese Meldung wird für alle MIDI-Nachrichten mit Ausnahme von System exklusiven Nachrichten verwendet.)          |
| [**MM \_ MIM \_ longdata**](mm-mim-longdata.md)   | Wird gesendet, wenn entweder eine vollständige, vom System exklusive System exklusive Nachricht empfangen wird oder wenn ein Puffer mit System exklusiven Daten gefüllt wurde.     |
| [**MM \_ MIM \_ longerror**](mm-mim-longerror.md) | Wird gesendet, wenn eine ungültige, vom System exklusive System exklusive Nachricht empfangen wird.                                                                        |
| [**MM \_ MIM \_ MoreData**](mm-mim-moredata.md)   | Wird gesendet, wenn eine Anwendung [**MIM- \_ Daten**](mim-data.md) Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabegeräte Treiber Schritt zu halten. |
| [**MM \_ MIM \_ geöffnet**](mm-mim-open.md)           | Wird gesendet, wenn ein MIDI-Eingabegerät mithilfe der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion geöffnet wird.                                        |



 

Jedem dieser Nachrichten sind ein *wParam* -Parameter und ein *LPARAM* -Parameter zugeordnet. Der *wParam* -Parameter gibt immer das Handle eines geöffneten MIDI-Geräts an. Der *LPARAM* -Parameter wird für die von [**mm \_ MIM \_**](mm-mim-close.md) geöffneten Nachrichten Close und [**mm \_ MIM \_**](mm-mim-open.md) nicht verwendet.

Bei der [**mm \_ MIM \_ longdata**](mm-mim-longdata.md) -Nachricht gibt *lpmidihdr* eine Adresse einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur an, die den Puffer für System exklusive Meldungen identifiziert. Der Puffer kann nicht vollständig ausgefüllt werden, da die Größe der System exklusiven Nachrichten in der Regel nicht bekannt ist, bevor Sie aufgezeichnet wird, und dass Puffer, deren Gesamtgröße die größte erwartete Nachricht enthalten kann, zugeordnet werden müssen. Um die Menge der gültigen Daten im Puffer zu ermitteln, verwenden Sie den **dwbytesrecorded** -Member der **midihdr** -Struktur.

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Verwenden einer Rückruffunktion zum Verwalten der MIDI-Aufzeichnung

Sie können eine eigene Rückruffunktion definieren, um die Aufzeichnung für MIDI-Eingabegeräte zu verwalten. Die Rückruffunktion ist als [**midiinproc**](/previous-versions//dd798460(v=vs.85))dokumentiert.

Die folgenden Meldungen können an den *wmsg* -Parameter der **midiinproc** -Rückruffunktion gesendet werden.



| Wert                                   | Bedeutung                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MIM \_ Close**](mim-close.md)         | Wird gesendet, wenn das Gerät mit der [**midiinclose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) -Funktion geschlossen wird.                                               |
| [**MIM- \_ Daten**](mim-data.md)           | Wird gesendet, wenn eine vollständige MIDI-Nachricht empfangen wird (diese Nachricht wird für alle MIDI-Nachrichten mit Ausnahme von System exklusiven Nachrichten verwendet).           |
| [**MIM- \_ Fehler**](mim-error.md)         | Wird gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird (diese Nachricht wird für alle MIDI-Nachrichten mit Ausnahme von System exklusiven Nachrichten verwendet).           |
| [**MIM \_ longdata**](mim-longdata.md)   | Wird gesendet, wenn entweder eine vollständige, vom System exklusive System exklusive Nachricht empfangen wird oder wenn ein Puffer mit System exklusiven Daten gefüllt wurde.     |
| [**MIM \_ longerror**](mim-longerror.md) | Wird gesendet, wenn eine ungültige, vom System exklusive System exklusive Nachricht empfangen wird.                                                                        |
| [**MIM \_ MoreData**](mim-moredata.md)   | Wird gesendet, wenn eine Anwendung [**MIM- \_ Daten**](mim-data.md) Nachrichten nicht schnell genug verarbeitet, um mit dem Eingabegeräte Treiber Schritt zu halten. |
| [**MIM \_ geöffnet**](mim-open.md)           | Wird gesendet, wenn das MIDI-Eingabegerät mithilfe der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion geöffnet wird.                                      |



 

Diese Nachrichten ähneln denen, die an Fenster Prozedur Funktionen gesendet werden, die Parameter unterscheiden sich jedoch. Ein Handle des geöffneten MIDI-Geräts wird als Parameter an die Rückruffunktion übergeben, zusammen mit dem Doubleword der Instanzdaten, die mithilfe von **midiinopen** übergeben wurden.

Bei der [**MIM \_ longdata**](mim-longdata.md) -Nachricht gibt *lpmidihdr* eine Adresse einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur an, die den Puffer für System exklusive Meldungen identifiziert. Der Puffer ist möglicherweise nicht vollständig ausgefüllt. Um die Menge der gültigen Daten im Puffer zu ermitteln, verwenden Sie den **dwbytesrecorded** -Member der **midihdr** -Struktur.

Nachdem der Gerätetreiber mit einem Datenblock fertig ist, können Sie den Datenblock bereinigen und freigeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von MIDI-Audiodateien](recording-midi-audio.md)
</dt> </dl>

 

 