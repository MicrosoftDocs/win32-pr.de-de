---
title: Audiodatenblöcke
description: Audiodatenblöcke
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- Multimedia-Audiodaten, Datenblöcke
- Audiodaten, Datenblöcke
- Wellenform-Audiodaten, Datenblöcke
- Audiodatenblöcke, Informationen zu
- Wavehdr-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948627"
---
# <a name="audio-data-blocks"></a>Audiodatenblöcke

Die Funktionen [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) und [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) erfordern, dass Anwendungen Datenblöcke zuordnen, die zu Aufzeichnungs-oder Wiedergabe Zwecken an die Gerätetreiber übergeben werden. Beide Funktionen verwenden die [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, um den zugehörigen Datenblock zu beschreiben.

Bevor Sie eine dieser Funktionen verwenden können, um einen Datenblock an einen Gerätetreiber zu übergeben, müssen Sie für den Datenblock und die Header Struktur, die den Datenblock beschreibt, Arbeitsspeicher zuweisen. Die Header können mithilfe der folgenden Funktionen vorbereitet und nicht vorbereitet werden.



| Funktion                                                 | BESCHREIBUNG                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**wavone prepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | Bereitet einen Eingabedaten Block mit Waveform-Audiodaten vor.                      |
| [**waveingeunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | Bereinigt die Vorbereitung auf einem Datenblock mit Waveform-Audioeingabe.  |
| [**waveoutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | Bereitet einen "Waveform-Audioausgabe"-Ausgabedaten Block vor.                     |
| [**waveoutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | Bereinigt die Vorbereitung für einen Waveform-audioausgabedatenblock. |



 

Bevor Sie einen audiodatenblock an einen Gerätetreiber übergeben, müssen Sie den Datenblock vorbereiten, indem Sie ihn entweder an [**waveingeprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) oder [**waveoutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)übergeben. Wenn der Gerätetreiber mit dem Datenblock fertig ist und ihn zurückgibt, müssen Sie diese Vorbereitung bereinigen, indem Sie den Datenblock entweder an [**waveinunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) oder [**waveoutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) übergeben, bevor zugeordneter Arbeitsspeicher freigegeben werden kann.

Wenn die Eingabe-und Ausgabedaten des Waveform-Audiodaten klein genug sind, um in einem einzelnen Datenblock enthalten zu sein, müssen Anwendungen den Gerätetreiber kontinuierlich mit Datenblöcken bereitstellen, bis die Wiedergabe oder Aufzeichnung abgeschlossen ist.

Selbst wenn ein einzelner Datenblock verwendet wird, muss eine Anwendung in der Lage sein, zu bestimmen, wann ein Gerätetreiber mit dem Datenblock fertig ist, damit die Anwendung den dem Datenblock und der Header Struktur zugeordneten Arbeitsspeicher freigeben kann. Es gibt mehrere Möglichkeiten, um zu bestimmen, wann ein Gerätetreiber mit einem Datenblock fertiggestellt ist:

-   Durch Angeben einer Rückruffunktion zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn er mit einem Datenblock fertig ist
-   Mithilfe eines Ereignis Rückrufs
-   Durch Angeben eines Fensters oder Threads zum Empfangen einer Nachricht, die vom Treiber gesendet wird, wenn er mit einem Datenblock fertig ist
-   Durch Abrufen des Bits "whdr \_ Done" im **dwFlags** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die mit jedem Datenblock gesendet wird

Wenn eine Anwendung bei Bedarf keinen Datenblock für den Gerätetreiber erhält, kann es eine akustische Lücke bei der Wiedergabe oder einen Verlust eingehender aufgezeichneter Informationen geben. Hierfür ist mindestens ein doppeltes Puffer Schema erforderlich – mindestens ein Datenblock vor dem Gerätetreiber.

In den folgenden Themen wird beschrieben, wie Sie bestimmen können, wann ein Gerätetreiber mit einem-Datenblock fertig ist:

Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten

-   [Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten](using-a-callback-function-to-process-driver-messages.md)
-   [Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten](using-an-callback-to-process-driver-messages.md)
-   [Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten](using-a-window-or-thread-to-process-driver-messages.md)
-   [Verwalten von Datenblöcken durch Abrufen](managing-data-blocks-by-polling.md)

 

 