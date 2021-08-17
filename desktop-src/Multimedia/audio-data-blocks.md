---
title: Audiodatenblöcke
description: Audiodatenblöcke
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- Multimediaaudio, Datenblöcke
- Audio,Datenblöcke
- Waveform-Audio, Datenblöcke
- Audiodatenblöcke,Informationen
- WAVEHDR-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a4a0c7236c52854911b51677cf792fa504371fb18900ac947e8fdf1391bd69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941754"
---
# <a name="audio-data-blocks"></a>Audiodatenblöcke

Die [**Funktionen waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) und [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) erfordern, dass Anwendungen Datenblöcke zuordnen, die zu Aufzeichnungs- oder Wiedergabezwecken an die Gerätetreiber übergeben werden. Beide Funktionen verwenden die [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) um ihren Datenblock zu beschreiben.

Bevor Sie eine dieser Funktionen verwenden, um einen Datenblock an einen Gerätetreiber zu übergeben, müssen Sie Arbeitsspeicher für den Datenblock und die Headerstruktur zuordnen, die den Datenblock beschreibt. Die Header können mithilfe der folgenden Funktionen vorbereitet und nicht vorbereitet werden.



| Funktion                                                 | Beschreibung                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Bereitet einen Waveform-Audio-Eingabedatenblock vor.                      |
| [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Bereinigt die Vorbereitung für einen Waveform-Audio-Eingabedatenblock.  |
| [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Bereitet einen Waveform-Audio-Ausgabedatenblock vor.                     |
| [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Bereinigt die Vorbereitung für einen Waveform-Audio-Ausgabedatenblock. |



 

Bevor Sie einen Audiodatenblock an einen Gerätetreiber übergeben, müssen Sie den Datenblock vorbereiten, indem Sie ihn entweder an [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) oder [**waveOutPrepareHeader übergeben.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) Wenn der Gerätetreiber mit dem Datenblock fertig ist und ihn zurückgibt, müssen Sie diese Vorbereitung bereinigt, indem Sie den Datenblock entweder [**an waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) oder [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) übergeben, bevor zugeordneter Arbeitsspeicher frei werden kann.

Sofern die Waveform-Audioeingabe- und -ausgabedaten nicht klein genug sind, um in einem einzelnen Datenblock enthalten zu sein, müssen Anwendungen dem Gerätetreiber kontinuierlich Datenblöcke zur Verfügung stellen, bis die Wiedergabe oder Aufzeichnung abgeschlossen ist.

Selbst wenn ein einzelner Datenblock verwendet wird, muss eine Anwendung in der Lage sein zu bestimmen, wann ein Gerätetreiber mit dem Datenblock fertig ist, damit die Anwendung den Speicher, der dem Datenblock und der Headerstruktur zugeordnet ist, frei geben kann. Es gibt mehrere Möglichkeiten, zu bestimmen, wann ein Gerätetreiber mit einem Datenblock fertig ist:

-   Durch Angeben einer Rückruffunktion zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn sie mit einem Datenblock abgeschlossen ist
-   Mithilfe eines Ereignisrückrufs
-   Durch Angeben eines Fensters oder Threads zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn er mit einem Datenblock fertig ist
-   Durch Abruf des WHDR \_ DONE-Bit im **dwFlags-Member** der [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) das mit jedem Datenblock gesendet wird

Wenn eine Anwendung bei Bedarf keinen Datenblock für den Gerätetreiber bekommt, kann es zu einer akustischen Lücke bei der Wiedergabe oder einem Verlust eingehender aufgezeichneter Informationen kommen. Dies erfordert mindestens ein Schema mit doppelter Pufferung– mindestens einen Datenblock vor dem Gerätetreiber.

In den folgenden Themen werden Möglichkeiten beschrieben, wie Sie bestimmen können, wann ein Gerätetreiber mit einem Datenblock fertig ist:

Verwenden einer Rückruffunktion zum Verarbeiten von Treibermeldungen

-   [Verwenden einer Rückruffunktion zum Verarbeiten von Treibermeldungen](using-a-callback-function-to-process-driver-messages.md)
-   [Verwenden eines Ereignisrückrufs zum Verarbeiten von Treibermeldungen](using-an-callback-to-process-driver-messages.md)
-   [Verwenden eines Fensters oder Threads zum Verarbeiten von Treibermeldungen](using-a-window-or-thread-to-process-driver-messages.md)
-   [Verwalten von Datenblöcken durch Abruf](managing-data-blocks-by-polling.md)

 

 