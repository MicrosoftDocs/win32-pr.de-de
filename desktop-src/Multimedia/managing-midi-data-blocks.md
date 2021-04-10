---
title: Verwalten von MIDI-Datenblöcken
description: Verwalten von MIDI-Datenblöcken
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Digital Instrumentation Digital Interface (MIDI), Verwalten von Datenblöcken
- MIDI (Digital Instrumentation Digital Interface), Verwalten von Datenblöcken
- MIDI-Dienste, Verwalten von Datenblöcken
- Verwalten von MIDI-Datenblöcken
- Digital Instrumentation Digital Interface (MIDI), Verarbeitung von Treiber Meldungen
- MIDI (Digital Instrumentation Digital Interface), Verarbeiten von Treiber Meldungen
- MIDI-Dienste, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Digital Instrumentation Digital Interface (MIDI), Datenblöcke
- MIDI (Digital Interface Digital Interface), Datenblöcke
- MIDI-Dienste, Datenblöcke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948634"
---
# <a name="managing-midi-data-blocks"></a>Verwalten von MIDI-Datenblöcken

Anwendungen, die Datenblöcke zum Übergeben von System exklusiven Nachrichten (mit den Funktionen [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) und [**midiinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) und Streampuffer (mithilfe der [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) -Funktion) verwenden, müssen den Gerätetreiber kontinuierlich mit Datenblöcken bereitstellen, bis die Wiedergabe oder Aufzeichnung beendet ist.

Selbst wenn ein einzelner Datenblock verwendet wird, muss eine Anwendung in der Lage sein, zu bestimmen, wann ein Gerätetreiber mit dem Datenblock fertig ist, damit er den dem Datenblock und der Header Struktur zugeordneten Arbeitsspeicher freigeben kann. Es können drei Methoden verwendet werden, um zu bestimmen, wann ein Gerätetreiber mit einem Datenblock fertiggestellt wird:

-   Geben Sie eine Rückruffunktion an, um eine vom Treiber gesendete Nachricht zu empfangen, wenn Sie mit einem Datenblock fertig ist. Um die von einem Zeitstempel versehene Daten zu erhalten, müssen Sie eine Rückruffunktion verwenden.
-   Verwenden Sie einen Ereignis Rückruf (nur für die Ausgabe).
-   Verwenden eines Fenster-oder Thread Rückrufs zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn der Vorgang mit einem Datenblock abgeschlossen ist.

Wenn eine Anwendung bei Bedarf keinen Datenblock für den Gerätetreiber erhält, kann eine akustische Lücke bei der Wiedergabe oder ein Verlust eingehender erfasster Informationen auftreten. Eine Anwendung sollte zumindest ein doppeltes pufferungsschema verwenden, um mindestens einen Datenblock vor dem Gerätetreiber zu behalten.

## <a name="using-a-callback-function-to-process-driver-messages"></a>Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten

Sie können eine eigene Rückruffunktion schreiben, um Nachrichten zu verarbeiten, die vom Gerätetreiber gesendet werden. Um eine Rückruffunktion zu verwenden, geben Sie das Rückruf \_ funktionsflag im *dwFlags* -Parameter und die Adresse der Rückruffunktion im *dwcallback* -Parameter der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -oder [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion an.

An eine Rückruffunktion gesendete Nachrichten ähneln Nachrichten, die an ein Fenster gesendet werden, mit dem Unterschied, dass Sie zwei Double Word-Parameter anstelle eines ganzzahligen Parameters ohne Vorzeichen und einen Double Word-Parameter Weitere Informationen zu diesen Nachrichten finden Sie unter [Senden von System-Exclusive Nachrichten](sending-system-exclusive-messages.md) und [Verwalten der MIDI-Aufzeichnung](managing-midi-recording.md).

Verwenden Sie eine der folgenden Verfahren, um Instanzdaten von einer Anwendung an eine Rückruffunktion zu übergeben:

-   Verwenden Sie den *dwcallbackinstance* -Parameter der Funktion, die den Gerätetreiber öffnet.
-   Verwenden Sie den **DWUser** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, der einen Datenblock identifiziert, der an einen MIDI-Gerätetreiber gesendet wird.

Wenn Sie mehr als 32 Bits von Instanzdaten benötigen, übergeben Sie eine Adresse einer Struktur, die die zusätzlichen Informationen enthält.

## <a name="using-an-event-callback-to-process-driver-messages"></a>Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten

Um einen Ereignis Rückruf zu verwenden, verwenden Sie die Funktion " [-Funktion", um das Handle](/windows/win32/api/synchapi/nf-synchapi-createeventa) eines Ereignisses abzurufen und das Rückruf \_ Ereignis im Aufrufen der Funktion " [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) " anzugeben.

Ein Ereignis Rückruf wird durch alle Elemente festgelegt, die einen Funktions Rückruf verursachen könnten. Anders als Rückruf Funktionen und Fenster-oder Thread Rückrufe empfangen Ereignis Rückrufe keine speziellen Close-, done-oder Open-Benachrichtigungen. Daher muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den Sie wartet, nachdem das Ereignis aufgetreten ist.

Weitere Informationen über Ereignis Rückrufe finden Sie unter [Verwenden eines Ereignis Rückrufs zum Verwalten der gepufferten Wiedergabe](using-an-callback-to-manage-buffered-playback.md).

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>Verwenden eines Fenster-oder Thread Rückrufs zum Verarbeiten von Treiber Nachrichten

Um einen Fenster Rückruf zu verwenden, geben Sie das Rückruf \_ Fenster-Flag im *dwFlags* -Parameter und ein Fenster Handle im nieder wertigen Wort des *dwcallback* -Parameters der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -oder [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion an. Treiber Meldungen werden an die Fenster Prozedur Funktion für das Fenster gesendet, das durch das Handle in *dwcallback* identifiziert wird.

Um einen Thread Rückruf zu verwenden, geben Sie auf ähnliche Weise das Rückruf \_ -threadflag und einen Thread Bezeichner im-Befehl von **midiinopen** oder **midioutopen** an. In diesem Fall werden Nachrichten anstelle eines Fensters an den angegebenen Thread gesendet.

Nachrichten, die an einen Fenster-oder Thread Rückruf gesendet werden, sind spezifisch für das verwendete MIDI-Gerät. Weitere Informationen zu diesen Nachrichten finden Sie unter [Senden von System-Exclusive Nachrichten](sending-system-exclusive-messages.md) und [Verwalten der MIDI-Aufzeichnung](managing-midi-recording.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDI-Dienste](midi-services.md)
</dt> </dl>

 

 