---
title: Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe
description: Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Digital Instrumentation Digital Interface (MIDI), gepufferte Wiedergabe
- MIDI (Digital Instrumentation Digital Interface), gepufferte Wiedergabe
- Abspielen von MIDI-Dateien, gepufferte Wiedergabe
- gepufferte Wiedergabe
- MM_MOM_CLOSE Meldung
- MM_MOM_DONE Meldung
- MM_MOM_OPEN Meldung
- Digital Instrumentation Digital Interface (MIDI), Senden von Nachrichten
- MIDI (Digital Instrumentation Digital Interface), Senden von Nachrichten
- Abspielen von MIDI-Dateien, Senden von Nachrichten
- Senden von MIDI-Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c8c120504a4a25ddcf01474db341a367a2e9854
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315014"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe

Die folgenden Meldungen können an ein Fenster oder einen Thread gesendet werden, um die Wiedergabe von System exklusiven Systemnachrichten oder streampuffern zu verwalten.



| Wert                                  | Bedeutung                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schließen von mm \_ MOM \_**](mm-mom-close.md) | Wird gesendet, wenn das Gerät mit der [**midioutclose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) -Funktion geschlossen wird.                                                                               |
| [**MM- \_ MOM \_ abgeschlossen**](mm-mom-done.md)   | Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig ist, der mit der Funktion [**midioutlongmsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) oder [**midistreamout**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) gesendet wurde. |
| [**MM \_ MOM \_ geöffnet**](mm-mom-open.md)   | Wird gesendet, wenn das Gerät mit der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion geöffnet wird.                                                                                 |



 

Jedem dieser Nachrichten sind ein *wParam* -Parameter und ein *LPARAM* -Parameter zugeordnet. Der *wParam* -Parameter gibt immer das Handle eines geöffneten MIDI-Geräts an. Für [**mm \_ MOM \_**](mm-mom-done.md)gibt *LPARAM* eine Adresse einer [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur an, die den abgeschlossenen Datenblock identifiziert. Der *LPARAM* -Parameter wird für [**das \_ \_ Schließen von mm MOM**](mm-mom-close.md) und das [**Öffnen von mm \_ MOM \_**](mm-mom-open.md)nicht verwendet.

Die nützlichste Meldung ist wahrscheinlich, dass mm \_ MOM \_ abgeschlossen ist. Wenn Sie Arbeitsspeicher nicht zuweisen oder Variablen initialisieren müssen, ist es wahrscheinlich nicht erforderlich, dass Sie mm \_ MOM \_ Open und mm \_ MOM \_ Close verarbeiten. Wenn die Wiedergabe eines Datenblocks beendet ist, können Sie den Datenblock bereinigen und freigeben.

 

 