---
title: Öffnen von EINGABEGERÄTEN
description: Öffnen von EINGABEGERÄTEN
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Instrument Digital Interface (KEYBOARD), Eingabegeräte
- KEYBOARD (Keyboard Instrument Digital Interface), Eingabegeräte
- Aufzeichnung von audio,input devices (Audioaufzeichnung, Eingabegeräte)
- INPUTS-Eingabegeräte
- Instrument Digital Interface (KEYBOARD), Öffnen von Eingabegeräten
- KEYBOARD (Keyboard Instrument Digital Interface), Öffnen von Eingabegeräten
- Aufzeichnung von audio,opening input devices (Audioaufzeichnung von AUDIO,Öffnen von Eingabegeräten)
- Öffnen von EINGABEEINGABE-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d260674194e7f066e5095e30a78c94b241a60b32304888aceb8db9ae06ccfea6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806270"
---
# <a name="opening-midi-input-devices"></a>Öffnen von EINGABEGERÄTEN

Verwenden Sie zum Öffnen eines FÜRT-Eingabegeräts für die Aufzeichnung [**die Funktion "formatInOpen".**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) Diese Funktion öffnet das Gerät, das der angegebenen Geräte-ID zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle an einen angegebenen Speicherort geschrieben wird.

Wenn Sie das FLAGGE IO STATUS-Flag mit \_ \_ **"keyboardInOpen"** verwenden, verwendet das System die [**MIM \_ MOREDATA-Nachricht,**](mim-moredata.md) um die Rückruffunktion Ihrer Anwendung zu warnen, wenn die VERARBEITUNG DER Daten nicht schnell genug erfolgt, um mit dem Eingabegerätetreiber mithalten zu können. (Die [**MELDUNG MM MIM \_ \_ MOREDATA**](mm-mim-moredata.md) führt den gleichen Auftrag mit Fensterrückrufen aus. Aus Leistungsgründen verwenden die meisten Anwendungen rückruffunktionen anstelle von Fensterrückrufen.) Wenn Ihre Anwendung DIE-Daten in einem separaten Thread verarbeitet, kann die Erhöhung der Threadpriorität erhebliche Auswirkungen auf die Fähigkeit der Anwendung haben, mit dem Datenfluss Schritt zu halten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von TONS-Audio](recording-midi-audio.md)
</dt> </dl>

 

 