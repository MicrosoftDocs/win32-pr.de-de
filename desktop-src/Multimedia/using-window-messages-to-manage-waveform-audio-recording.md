---
title: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Aufzeichnung
description: Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Aufzeichnung
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- Wellenform-Audiodatei, Verwalten der Aufzeichnung mit Nachrichten
- Waveform-Audioschnittstelle, Verwalten der Aufzeichnung mit Nachrichten
- Aufzeichnen von Wellenform-Audiodaten, Verwalten der Aufzeichnung mit Nachrichten
- Wellenform-Audiodaten, Meldungen
- Waveform-Audioschnittstelle, Meldungen
- Aufzeichnen von Wellenform-Audiodaten, Nachrichten
- MM_WIM_CLOSE Meldung
- MM_WIM_DATA Meldung
- MM_WIM_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472836"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Verwenden von Fenster Meldungen zum Verwalten Waveform-Audio Aufzeichnung

Die folgenden Meldungen können an eine Fenster Prozedur Funktion zum Verwalten der Waveform-Audioaufzeichnung gesendet werden.



| `Message`                                | BESCHREIBUNG                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WIM \_ Schließen**](mm-wim-close.md) | Wird gesendet, wenn das Gerät mithilfe der [**waveinclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) -Funktion geschlossen wird.                                     |
| [**MM- \_ WIM- \_ Daten**](mm-wim-data.md)   | Wird gesendet, wenn der Gerätetreiber mit einem Puffer fertig ist, der mithilfe der [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) -Funktion gesendet wurde. |
| [**MM \_ WIM \_ geöffnet**](mm-wim-open.md)   | Wird gesendet, wenn das Gerät mithilfe der [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion geöffnet wird.                                       |



 

Der *LPARAM* -Parameter der [**mm-WIM- \_ \_ Daten**](mm-wim-data.md) gibt einen Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur an, die den Puffer identifiziert. Dieser Puffer ist möglicherweise nicht vollständig mit Waveform-Audiodaten gefüllt. Aufzeichnung kann angehalten werden, bevor der Puffer gefüllt wird. Verwenden Sie den **dwbytesrecorded** -Member der **wavehdr** -Struktur, um die Menge der gültigen Daten zu ermitteln, die im Puffer vorhanden sind.

Die nützlichste Meldung ist wahrscheinlich [**mm \_ WIM- \_ Daten**](mm-wim-data.md). Wenn die Anwendung mit dem vom Gerätetreiber gesendeten Datenblock abgeschlossen ist, können Sie den Datenblock bereinigen und freigeben. Wenn Sie Arbeitsspeicher nicht zuweisen oder Variablen initialisieren müssen, müssen Sie die mm-WIM-Nachrichten ( [**\_ WIM \_ Open**](mm-wim-open.md) und [**mm \_ \_**](mm-wim-close.md) ) wahrscheinlich nicht verwenden.

Die Rückruffunktion für Waveform-Audioeingabegeräte wird von der Anwendung bereitgestellt. Weitere Informationen zu dieser Rückruffunktion finden Sie unter der [**waveinproc**](/previous-versions//dd743849(v=vs.85)) -Funktion.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audiodaten](recording-waveform-audio.md)
</dt> </dl>

 

 