---
title: Beenden, Anhalten und Neustarten der Wiedergabe
description: Beenden, Anhalten und Neustarten der Wiedergabe
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- Waveform-Audio, Beenden der Wiedergabe
- Waveform-Audio-Schnittstelle, Beenden der Wiedergabe
- Wiedergabe von Waveform-Audiodateien, Beenden der Wiedergabe
- Waveform-Audio, Anhalten der Wiedergabe
- Waveform-Audio-Schnittstelle, Anhalten der Wiedergabe
- Wiedergabe von Waveform-Audiodateien, Anhalten der Wiedergabe
- Waveform-Audio, Neustarten der Wiedergabe
- Waveform-Audio-Schnittstelle, Neustarten der Wiedergabe
- Wiedergabe von Waveform-Audiodateien, Neustarten der Wiedergabe
- waveOutPause-Funktion
- waveOutReset-Funktion
- waveOutRestart-Funktion
- Beenden der Wiedergabe von Waveform-Audio
- Anhalten der Wiedergabe von Waveform-Audio
- Neustarten der Wiedergabe von Waveform-Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04491a676a104e288d274da7dd70eb759e363adc6476805b261a9651444bf1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688490"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Beenden, Anhalten und Neustarten der Wiedergabe

Sie können die Wiedergabe anhalten oder anhalten, während Waveform-Audio abspielt wird. Nachdem die Wiedergabe angehalten wurde, können Sie sie neu starten. Windows bietet die folgenden Funktionen zum Steuern der Wiedergabe von Waveform-Audio.



| Funktion                                 | Beschreibung                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Hält die Wiedergabe auf einem Waveform-Audio-Ausgabegerät an.                                          |
| [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Beendet die Wiedergabe auf einem Waveform-Audio-Ausgabegerät und markiert alle ausstehenden Datenblöcke als abgeschlossen. |
| [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Setzt die Wiedergabe auf einem angehaltenen Waveform-Audio-Ausgabegerät wieder auf.                                  |



 

Das Anhalten eines Waveform-Audiogeräts mit [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) ist möglicherweise nicht sofort möglich. Der Treiber kann die Wiedergabe des aktuellen Blocks beenden, bevor die Wiedergabe beendet wird.

Im Allgemeinen beginnt das Waveform-Audio-Gerät mit der Wiedergabe, sobald der erste Waveform-Audio-Datenblock mithilfe der [**waveOutWrite-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) gesendet wird. Wenn Sie nicht möchten, dass der Sound sofort abspielt, rufen Sie **waveOutPause** auf, bevor **Sie waveOutWrite aufrufen.** Wenn Sie dann mit der Wiedergabe von Waveform-Audiodaten beginnen möchten, rufen Sie [**waveOutRestart auf.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)

Sie können **waveOutRestart nicht verwenden,** um ein Gerät neu zu starten, das mit [**waveOutReset beendet wurde.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) Sie müssen **waveOutWrite verwenden,** um den ersten Datenblock zu senden, um die Wiedergabe auf dem Gerät wieder aufzunehmen.

 

 