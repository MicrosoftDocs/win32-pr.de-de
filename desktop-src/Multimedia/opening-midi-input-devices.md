---
title: Öffnen von MIDI-Eingabegeräten
description: Öffnen von MIDI-Eingabegeräten
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Digital Instrumentation Digital Interface (MIDI), Eingabegeräte
- MIDI (Digital Instrumentation Digital Interface), Eingabegeräte
- Aufzeichnen von MIDI-Audiodaten, Eingabegeräte
- MIDI-Eingabegeräte
- Digital Instrumentation Digital Interface (MIDI), Öffnen von Eingabegeräten
- MIDI (Digital Instrumentation Digital Interface), Öffnen von Eingabegeräten
- Aufzeichnen von MIDI-Audiodaten, Öffnen von Eingabegeräten
- Öffnen von MIDI-Eingabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4c1271cee1e6a47c35f8c555932d87d1055065
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726320"
---
# <a name="opening-midi-input-devices"></a>Öffnen von MIDI-Eingabegeräten

Verwenden Sie zum Öffnen eines MIDI-Eingabe Geräts für die Aufzeichnung die [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion. Diese Funktion öffnet das Gerät, das dem angegebenen Geräte Bezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle an einen angegebenen Speicherort geschrieben wird.

Wenn Sie das Integritäts Kennzeichen für das MIDI-e/a \_ \_ mit **midiinopen** verwenden, verwendet das System die [**MIM \_ MoreData**](mim-moredata.md) -Nachricht, um die Rückruffunktion Ihrer Anwendung zu benachrichtigen, wenn die Daten von MIDI nicht schnell genug verarbeitet werden, um mit dem Eingabegeräte Treiber Schritt zu halten. (Die [**mm \_ MIM \_ MoreData**](mm-mim-moredata.md) -Nachricht führt den gleichen Auftrag mit Fenster Rückrufen aus. Aus Leistungsgründen werden von den meisten Anwendungen jedoch Rückruf Funktionen anstelle von Fenster Rückrufen verwendet.) Wenn Ihre Anwendung die Daten von MIDI in einem separaten Thread verarbeitet, kann sich die Erhöhung der Thread Priorität erheblich auf die Fähigkeit der Anwendung auswirken, mit dem Datenfluss Schritt zu halten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von MIDI-Audiodateien](recording-midi-audio.md)
</dt> </dl>

 

 