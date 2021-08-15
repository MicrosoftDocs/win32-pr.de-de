---
title: Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe
description: Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe
ms.assetid: 3c8145a8-e56a-449d-ad45-2ae016f79697
keywords:
- Keyboard Instrument Digital Interface (KEYBOARD), gepufferte Wiedergabe
- KEYBOARD (Keyboard Instrument Digital Interface), gepufferte Wiedergabe
- Wiedergeben vonSCHALT-Dateien, gepufferte Wiedergabe
- Gepufferte Wiedergabe
- MM_MOM_CLOSE Nachricht
- MM_MOM_DONE-Nachricht
- MM_MOM_OPEN-Nachricht
- Instruments Instrument Digital Interface (KEYBOARD), Senden von Nachrichten
- KEYBOARD (Instruments Instrument Digital Interface), Senden von Nachrichten
- Wiedergeben von DANN-Dateien, Senden von Nachrichten
- Senden von SIGNAL-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc0acb39090a640d60539542a439111287faef246adf64aef7ee12ced3ae09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801254"
---
# <a name="using-a-window-or-thread-to-manage-buffered-playback"></a>Verwenden eines Fensters oder Threads zum Verwalten der gepufferten Wiedergabe

Die folgenden Meldungen können an ein Fenster oder einen Thread gesendet werden, um die Wiedergabe von SYSTEM-exklusiven NACHRICHTEN oder Streampuffern zu verwalten.



| Wert                                  | Bedeutung                                                                                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MOM \_ CLOSE**](mm-mom-close.md) | Wird gesendet, wenn das Gerät mithilfe der [**Funktion "keyboardOutClose" geschlossen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) wird.                                                                               |
| [**MM \_ MOM \_ DONE**](mm-mom-done.md)   | Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig gestellt wird, der mithilfe der [**Funktion "blocksOutLongMsg"**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) oder [**"streamStreamOut" gesendet**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) wird. |
| [**MM \_ MOM \_ OPEN**](mm-mom-open.md)   | Wird gesendet, wenn das Gerät geöffnet wird, indem [**die Funktion "befehlOutOpen" verwendet**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) wird.                                                                                 |



 

Jeder dieser Meldungen sind ein *wParam-Parameter* und ein *lParam-Parameter* zugeordnet. Der *wParam-Parameter* gibt immer das Handle eines geöffnetenWERT-Geräts an. Für [**MM MOM DONE \_ \_ gibt**](mm-mom-done.md) *lParam* eine Adresse einer [**BLOCKSHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) an, die den abgeschlossenen Datenblock identifiziert. Der *lParam-Parameter* wird für [**MM MOM \_ \_ CLOSE**](mm-mom-close.md) und [**MM MOM OPEN nicht \_ \_ verwendet.**](mm-mom-open.md)

Die nützlichste Meldung ist wahrscheinlich MM \_ MOM \_ DONE. Wenn Sie keinen Arbeitsspeicher zuordnen oder Variablen initialisieren müssen, müssen Sie mm mom open und \_ MM MOM CLOSE wahrscheinlich nicht \_ \_ \_ verarbeiten. Wenn die Wiedergabe eines Datenblocks abgeschlossen ist, können Sie den Datenblock bereinigt und freigeben.

 

 