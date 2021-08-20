---
title: Verwenden von Fenstermeldungen zum Verwalten Waveform-Audio Wiedergabe
description: Verwenden von Fenstermeldungen zum Verwalten Waveform-Audio Wiedergabe
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- Waveformaudio,Verwalten der Wiedergabe mit Nachrichten
- Waveform-Audio-Schnittstelle,Verwalten der Wiedergabe mit Nachrichten
- Wiedergeben von Waveform-Audiodateien, Verwalten der Wiedergabe mit Nachrichten
- Waveform-Audio, Nachrichten
- Waveform-Audio-Schnittstelle, Nachrichten
- Wiedergeben von Waveform-Audiodateien, Nachrichten
- MM_WOM_CLOSE Meldung
- MM_WOM_DONE Meldung
- MM_WOM_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31d8a88cb74953a1d38285a77b18ac25cd7495c3e29e71c5259551b5c2c3453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135885"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Verwenden von Fenstermeldungen zum Verwalten Waveform-Audio Wiedergabe

Die folgenden Nachrichten können an eine Fensterprozedurfunktion zum Verwalten der Wiedergabe von Waveform-Audio gesendet werden.



| `Message`                                | BESCHREIBUNG                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WOM \_ CLOSE**](mm-wom-close.md) | Wird gesendet, wenn das Gerät mithilfe der [**waveOutClose-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) geschlossen wird.                                 |
| [**MM \_ WOM \_ DONE**](mm-wom-done.md)   | Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig ist, der mithilfe der [**waveOutWrite-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) gesendet wird. |
| [**MM \_ WOM \_ OPEN**](mm-wom-open.md)   | Wird gesendet, wenn das Gerät mithilfe der [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) geöffnet wird.                                   |



 

Jeder dieser Nachrichten ist ein *wParam-* und *lParam-Parameter* zugeordnet. Der *wParam-Parameter* gibt immer ein Handle des geöffneten Waveform-Audiogeräts an. Für die [**MM \_ WOM \_ DONE-Nachricht**](mm-wom-done.md) gibt *lParam* einen Zeiger auf eine [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) an, die den abgeschlossenen Datenblock identifiziert. Der *lParam-Parameter* wird für die [**MM \_ WOM \_ CLOSE-**](mm-wom-close.md) und [**MM \_ WOM \_ OPEN-Meldungen**](mm-wom-open.md) nicht verwendet.

Die nützlichste Meldung ist wahrscheinlich MM \_ WOM \_ DONE. Wenn diese Meldung signalisiert, dass die Wiedergabe eines Datenblocks abgeschlossen ist, können Sie den Datenblock bereinigen und freigeben. Sofern Sie keinen Speicher belegen oder Variablen initialisieren müssen, müssen Sie die \_ MM WOM \_ OPEN- und MM \_ WOM CLOSE-Meldungen wahrscheinlich nicht \_ verarbeiten.

Die Rückruffunktion für Waveform-Audio-Ausgabegeräte wird von der Anwendung bereitgestellt. Informationen zu dieser Rückruffunktion finden Sie in der [**waveOutProc-Funktion.**](/previous-versions//dd743869(v=vs.85))

 

 