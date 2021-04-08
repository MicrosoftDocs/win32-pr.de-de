---
title: Beenden, anhalten und erneutes Starten der Wiedergabe
description: Beenden, anhalten und erneutes Starten der Wiedergabe
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- Wellenform-Audiodatei, Beenden der Wiedergabe
- Waveform-Audioschnittstelle, Beenden der Wiedergabe
- Wiedergabe von Waveform-Audiodateien, Beenden der Wiedergabe
- Wellenform-Audiodatei, Anhalten der Wiedergabe
- Waveform-Audioschnittstelle, Anhalten der Wiedergabe
- Wiedergabe von Waveform-Audiodateien, Anhalten der Wiedergabe
- Wellenform-Audiodatei, Wiedergabe neu starten
- Waveform-Audioschnittstelle, Neustarten der Wiedergabe
- Wiedergeben von Waveform-Audiodateien, erneutes Starten der Wiedergabe
- waveoutpause-Funktion
- Wave-Set-Funktion
- Wave-Start-Funktion
- Beenden der Waveform-Audiowiedergabe
- Anhalten der Waveform-Audiowiedergabe
- Neustarten der Waveform-Audiowiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101491"
---
# <a name="stopping-pausing-and-restarting-playback"></a>Beenden, anhalten und erneutes Starten der Wiedergabe

Sie können die Wiedergabe anhalten oder anhalten, während das Wellenform-Audioformat abgespielt wird. Nachdem die Wiedergabe angehalten wurde, können Sie Sie neu starten. Windows stellt die folgenden Funktionen zum Steuern der Waveform-Audiowiedergabe bereit.



| Funktion                                 | BESCHREIBUNG                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [**waveoutpause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | Hält die Wiedergabe auf einem Waveform-Audioausgabegerät an.                                          |
| [**waveeinset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | Beendet die Wiedergabe auf einem Waveform-Audioausgabegerät und markiert alle ausstehenden Datenblöcke als abgeschlossen. |
| [**wavestartstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | Nimmt die Wiedergabe auf einem angehaltenen Waveform-Audioausgabegerät wieder auf.                                  |



 

Das Anhalten eines Waveform-Audiogeräts mithilfe von [**waveoutpause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) ist möglicherweise nicht sofort. der Treiber kann das Abspielen des aktuellen Blocks beenden, bevor die Wiedergabe angehalten wird.

Im allgemeinen beginnt, sobald der erste Waveform-audiodatenblock mithilfe der [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) -Funktion gesendet wird, das Waveform-Audiogerät zu spielen. Wenn Sie nicht möchten, dass der Sound sofort abgespielt wird, rufen Sie **waveoutpause** auf, bevor Sie **waveOutWrite** aufrufen. Wenn Sie dann mit der Wiedergabe von Waveform-Audiodaten beginnen möchten, wenden Sie [**wavestartstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)an.

Sie können **wavestartstart** nicht verwenden, um ein Gerät neu zu starten, das mit [**waveeinset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)beendet wurde. Sie müssen " **waveOutWrite** " verwenden, um den ersten Datenblock zu senden, um die Wiedergabe auf dem Gerät wieder aufzunehmen.

 

 