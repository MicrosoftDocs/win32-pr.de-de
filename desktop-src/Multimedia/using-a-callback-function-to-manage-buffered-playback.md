---
title: Verwenden einer Rückruffunktion zum Verwalten der gepufferten Wiedergabe
description: Verwenden einer Rückruffunktion zum Verwalten der gepufferten Wiedergabe
ms.assetid: aaaf9c5f-c9b2-4e55-a4c1-28c99cc03945
keywords:
- Digital Instrumentation Digital Interface (MIDI), gepufferte Wiedergabe
- MIDI (Digital Instrumentation Digital Interface), gepufferte Wiedergabe
- Abspielen von MIDI-Dateien, gepufferte Wiedergabe
- gepufferte Wiedergabe
- MOM_CLOSE Meldung
- MOM_DONE Meldung
- MOM_OPEN Meldung
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
- Digital Instrumentation Digital Interface (MIDI), Rückruf Funktionen
- MIDI (Digital Instrumentation Digital Interface), Rückruf Funktionen
- Abspielen von MIDI-Dateien, Rückruf Funktionen
- Midioutproc-Rückruffunktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccccd8e5fb052b89e8ca1804b89de6da26cd5b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726296"
---
# <a name="using-a-callback-function-to-manage-buffered-playback"></a>Verwenden einer Rückruffunktion zum Verwalten der gepufferten Wiedergabe

Sie können eine eigene Rückruffunktion definieren, um die gepufferte Wiedergabe von MIDI-Ausgabegeräten zu verwalten. Die Rückruffunktion ist als [**midioutproc**](/previous-versions//dd798478(v=vs.85))dokumentiert.

Die folgenden Meldungen können an den *wmsg* -Parameter der **midioutproc** -Rückruffunktion gesendet werden.



| Wert                           | Bedeutung                                                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MOM \_ Schließen**](mom-close.md) | Wird gesendet, wenn das Gerät mit der [**midioutclose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) -Funktion geschlossen wird.                                                                               |
| [**MOM \_ abgeschlossen**](mom-done.md)   | Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig ist, der mit der Funktion [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) oder [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) gesendet wurde. |
| [**MOM \_ geöffnet**](mom-open.md)   | Wird gesendet, wenn das Gerät mit der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion geöffnet wird.                                                                                 |



 

Diese Nachrichten ähneln denen, die an Fenster Prozedur Funktionen gesendet werden, die Parameter unterscheiden sich jedoch. Ein Handle des geöffneten MIDI-Geräts wird als Parameter an die Rückruffunktion übergeben, zusammen mit dem Doubleword der mithilfe von **midioutopen** übergebenen Instanzdaten.

Nachdem der Treiber mit einem Datenblock fertig ist, können Sie den Datenblock bereinigen und freigeben. Aufgrund der empfohlenen Einschränkungen für Rückruf Funktionen ist es besser, dies nicht innerhalb der Rückruffunktion durchzuführen.

 

 