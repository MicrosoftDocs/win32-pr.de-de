---
title: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Wiedergabe
description: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Wiedergabe
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- Wellenform-Audiodatei, Verwalten der Wiedergabe mit Meldungen
- Waveform-Audioschnittstelle, Verwalten der Wiedergabe mit Nachrichten
- Wiedergabe von Waveform-Audiodateien, Verwalten der Wiedergabe mit Nachrichten
- Wellenform-Audiodaten, Meldungen
- Waveform-Audioschnittstelle, Meldungen
- Wiedergabe von Waveform-Audiodateien, Nachrichten
- MM_WOM_CLOSE Meldung
- MM_WOM_DONE Meldung
- MM_WOM_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314853"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Wiedergabe

Die folgenden Meldungen können an eine Fenster Prozedur Funktion zum Verwalten der Waveform-Audiowiedergabe gesendet werden.



| `Message`                                | BESCHREIBUNG                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WOM \_ Schließen**](mm-wom-close.md) | Wird gesendet, wenn das Gerät mit der [**waveoutclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) -Funktion geschlossen wird.                                 |
| [**MM \_ WOM \_ abgeschlossen**](mm-wom-done.md)   | Wird gesendet, wenn der Gerätetreiber mit einem Datenblock fertig ist, der mithilfe der [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) -Funktion gesendet wurde. |
| [**MM \_ WOM \_ geöffnet**](mm-wom-open.md)   | Wird gesendet, wenn das Gerät mithilfe der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion geöffnet wird.                                   |



 

Jedem dieser Nachrichten ist ein *wParam* -Parameter und ein *LPARAM* -Parameter zugeordnet. Der *wParam* -Parameter gibt immer ein Handle des geöffneten Waveform-Audiogeräts an. Bei der Meldung [**mm \_ WOM \_ done**](mm-wom-done.md) gibt *LPARAM* einen Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur an, die den abgeschlossenen Datenblock identifiziert. Der *LPARAM* -Parameter wird nicht für die geöffneten Meldungen [**mm \_ WOM \_ Close**](mm-wom-close.md) und [**mm \_ WOM \_**](mm-wom-open.md) verwendet.

Die nützlichste Meldung ist wahrscheinlich mm \_ WOM \_ . Wenn diese Meldung signalisiert, dass die Wiedergabe eines Datenblocks beendet ist, können Sie den Datenblock bereinigen und freigeben. Wenn Sie Arbeitsspeicher nicht zuweisen oder Variablen initialisieren müssen, müssen Sie die \_ Nachrichten von mm WOM \_ Öffnen und mm \_ WOM \_ Schließen wahrscheinlich nicht verarbeiten.

Die Rückruffunktion für Waveform-Audioausgabegeräte wird von der Anwendung bereitgestellt. Weitere Informationen zu dieser Rückruffunktion finden Sie unter der [**waveoutproc**](/previous-versions//dd743869(v=vs.85)) -Funktion.

 

 