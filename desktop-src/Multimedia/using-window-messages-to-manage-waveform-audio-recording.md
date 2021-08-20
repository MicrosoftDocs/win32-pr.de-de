---
title: Verwenden von Fenstermeldungen zum Verwalten Waveform-Audio Aufzeichnung
description: Verwenden von Fenstermeldungen zum Verwalten Waveform-Audio Aufzeichnung
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- Waveformaudio, Verwalten der Aufzeichnung mit Nachrichten
- Waveform-Audio-Schnittstelle,Verwalten der Aufzeichnung mit Nachrichten
- Aufzeichnen von Waveform-Audio, Verwalten der Aufzeichnung mit Nachrichten
- Waveform-Audio, Nachrichten
- Waveform-Audio-Schnittstelle, Nachrichten
- Aufzeichnen von Waveform-Audio, Nachrichten
- MM_WIM_CLOSE Meldung
- MM_WIM_DATA Meldung
- MM_WIM_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c709df27be25a8a3f4c5a9be6528e28b4e8bab9251b04b6c397a7ef3fc8efd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135652"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Verwenden von Fenstermeldungen zum Verwalten Waveform-Audio Aufzeichnung

Die folgenden Nachrichten können an eine Fensterprozedurfunktion zum Verwalten der Waveform-Audioaufzeichnung gesendet werden.



| `Message`                                | BESCHREIBUNG                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WIM \_ CLOSE**](mm-wim-close.md) | Wird gesendet, wenn das Gerät mithilfe der [**waveInClose-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) geschlossen wird.                                     |
| [**MM \_ WIM \_ DATA**](mm-wim-data.md)   | Wird gesendet, wenn der Gerätetreiber mit einem Puffer fertig ist, der mithilfe der [**waveInAddBuffer-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) gesendet wird. |
| [**MM \_ WIM \_ OPEN**](mm-wim-open.md)   | Wird gesendet, wenn das Gerät mithilfe der [**waveInOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) geöffnet wird.                                       |



 

Der *lParam-Parameter* von [**MM \_ WIM \_ DATA**](mm-wim-data.md) gibt einen Zeiger auf eine [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) an, die den Puffer identifiziert. Dieser Puffer ist möglicherweise nicht vollständig mit Waveform-Audiodaten gefüllt. Die Aufzeichnung kann beendet werden, bevor der Puffer gefüllt wird. Verwenden Sie den **dwBytesRecorded-Member** der **WAVEHDR-Struktur,** um die Menge gültiger Daten zu bestimmen, die im Puffer vorhanden sind.

Die nützlichste Meldung ist wahrscheinlich [**MM \_ WIM \_ DATA**](mm-wim-data.md). Wenn Ihre Anwendung den vom Gerätetreiber gesendeten Datenblock verwendet, können Sie den Datenblock bereinigen und freigeben. Sofern Sie keinen Arbeitsspeicher belegen oder Variablen initialisieren müssen, müssen Sie wahrscheinlich nicht die [**MM \_ WIM \_ OPEN-**](mm-wim-open.md) und [**MM \_ WIM \_ CLOSE-Meldungen**](mm-wim-close.md) verwenden.

Die Rückruffunktion für Waveform-Audio-Eingabegeräte wird von der Anwendung bereitgestellt. Informationen zu dieser Rückruffunktion finden Sie in der [**waveInProc-Funktion.**](/previous-versions//dd743849(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audio](recording-waveform-audio.md)
</dt> </dl>

 

 