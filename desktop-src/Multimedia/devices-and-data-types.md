---
title: Geräte und Datentypen
description: Geräte und Datentypen
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- Wellenform-Audiodatei, Öffnen von Ausgabegeräten
- Waveform-Audioschnittstelle, Öffnen von Ausgabegeräten
- Öffnen von Waveform-audioausgabegeräten
- Wellenform-Audiodaten, Abfragen von Ausgabegeräten
- Waveform-Audioschnittstelle, Abfragen von Ausgabegeräten
- Abfragen von Waveform-audioausgabegeräten
- Wellenform-Audiodatei, Geräte Handles
- Waveform-Audioschnittstelle, Geräte Handles
- Wellenform-Audiodatei, Geräte Bezeichner
- Waveform-Audioschnittstelle, Geräte Bezeichner
- Wellenform-Audiodatei, Ausgabe Datentypen
- Waveform-Audioschnittstelle, Ausgabe Datentypen
- Wellenform-Audiodaten, Datenformate
- Waveform-Audioschnittstelle, Datenformate
- Schreiben von Waveform-Audiodaten
- Wellenform-Audiodaten, Schreiben von Daten
- Waveform-Audioschnittstelle, Schreiben von Daten
- PCM Waveform-Audiodaten
- Wellenform-Audiodaten, PCM-Daten
- Waveform-Audioschnittstelle, PCM-Daten
- Wellenform-Audiodatei, schließen von Ausgabegeräten
- Waveform-Audioschnittstelle, schließen von Ausgabegeräten
- Schließen von Waveform-audioausgabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29561a74695fb8bde950e2e75a430803a1a0351b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340905"
---
# <a name="devices-and-data-types"></a>Geräte und Datentypen

In diesem Abschnitt wird das Arbeiten mit Waveform-Audiogeräten beschrieben. es enthält auch Informationen zum Öffnen, schließen und Abfragen der Funktionen. Außerdem wird beschrieben, wie die Geräte in einem System mithilfe von Geräte Handles und Geräte bezeichfern nachverfolgt werden.

## <a name="opening-waveform-audio-output-devices"></a>Öffnen Waveform-Audio Ausgabegeräte

Verwenden Sie die Funktion [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) , um ein Waveform-Audioausgabegerät für die Wiedergabe zu öffnen. Diese Funktion öffnet das Gerät, das dem angegebenen Geräte Bezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle eines angegebenen Speicher Orts geschrieben wird.

Einige Multimedia-Computer verfügen über mehrere Waveform-Audioausgabegeräte. Wenn Sie ein bestimmtes Waveform-Audioausgabegerät nicht in einem System öffnen möchten, sollten Sie das Wave- \_ Mapper-Flag für den Geräte Bezeichner verwenden, wenn Sie ein Gerät öffnen. Die **WaveOutOpen** -Funktion wählt das Gerät im System aus, das das angegebene Datenformat am besten wiedergeben kann.

## <a name="querying-audio-devices"></a>Abfragen von Audiogeräten

Windows stellt die folgenden Funktionen bereit, um zu bestimmen, wie viele Geräte eines bestimmten Typs in einem System verfügbar sind.



| Funktion                                       | BESCHREIBUNG                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**"auxgetnumentvs"**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Ruft die Anzahl der zusätzlichen Ausgabegeräte ab, die im System vorhanden sind.      |
| [**waveingegetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Ruft die Anzahl der Waveform-Audioeingabegeräte ab, die im System vorhanden sind.  |
| [**waveoutgetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Ruft die Anzahl der Waveform-Audioausgabegeräte ab, die im System vorhanden sind. |



 

Audiogeräte werden anhand eines Geräte Bezeichners identifiziert. Der Geräte Bezeichner wird implizit von der Anzahl der in einem System vorhandenen Geräte bestimmt. Geräte Bezeichner reichen von Null bis zu einer geringeren Anzahl von Geräten. Wenn z. b. zwei Waveform-Audioausgabegeräte in einem System vorhanden sind, sind gültige Geräte Bezeichner 0 und 1.

Nachdem Sie festgelegt haben, wie viele Geräte eines bestimmten Typs in einem System vorhanden sind, können Sie eine der folgenden Funktionen verwenden, um die Funktionen der einzelnen Geräte abzufragen.



| Funktion                                       | BESCHREIBUNG                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**"auxgetdevcaps"**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Ruft die Funktionen eines angegebenen zusätzlichen Ausgabegeräts ab.      |
| [**waveingegetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Ruft die Funktionen eines angegebenen Waveform-Audioeingabegeräts ab.  |
| [**waveoutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Ruft die Funktionen eines angegebenen Waveform-Audioausgabegeräts ab. |



 

Jede dieser Funktionen füllt eine Struktur mit Informationen zu den Funktionen eines bestimmten Geräts. In der folgenden Tabelle werden die-Strukturen aufgelistet, die den einzelnen Funktionen entsprechen.



|                                                |                                    |
|------------------------------------------------|------------------------------------|
| Funktion                                       | Struktur                          |
| [**"auxgetdevcaps"**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**Zugriffs enden**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveingegetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**Wavin Caps**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveoutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**Waveoutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Standard Formate werden im **dwformats** -Member der **waveoutcaps** -Struktur aufgeführt. Waveform: Audiogeräte können nicht dem Standard entsprechende Formate unterstützen. Um festzustellen, ob ein bestimmtes Format (Standard oder nicht Standard) von einem Gerät unterstützt wird, können Sie die [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion mit dem Query-Flag "Wave Format" aufzurufen \_ \_ . Dieses Flag öffnet das Gerät nicht. Sie geben das betreffende Format in der [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur an, auf die der an **WaveOutOpen** übergebenen *pwfx* -Parameter verweist.

Waveform-Audioausgabegeräte variieren in den von Ihnen unterstützten Funktionen. Der **dwsupport** -Member der [**waveoutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) -Struktur gibt an, ob ein Gerät solche Funktionen wie Volumen-und Speicherplatz Änderungen unterstützt.

## <a name="device-handles-and-device-identifiers"></a>Geräte Handles und Geräte Bezeichner

Jede Funktion, die ein Audiogerät öffnet, gibt einen Geräte Bezeichner, einen Zeiger auf einen Speicherort und einige Parameter an, die für die einzelnen Gerätetypen eindeutig sind. Der Speicherort wird mit einem Geräte handle gefüllt. Verwenden Sie dieses Geräte handle, um das geöffnete Audiogerät zu identifizieren, wenn andere Audiofunktionen aufgerufen werden.

Der Unterschied zwischen bezeichgern und Handles für Audiogeräte ist nur geringfügige, aber wichtig:

-   Geräte Bezeichner werden implizit von der Anzahl von Geräten, die in einem System vorhanden sind, bestimmt. Diese Zahl wird [**mithilfe der Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)"" von "" "" [](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)"" "" "" "" " [](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) " "" "" "" "" "" "" "" ""
-   Geräte Handles werden zurückgegeben, wenn Gerätetreiber mithilfe der [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion oder der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion geöffnet werden.

Es sind keine Funktionen vorhanden, mit denen zusätzliche Audiogeräte geöffnet oder geschlossen werden. Zusätzliche Audiogeräte müssen nicht wie Waveform-Audiogeräte geöffnet und geschlossen werden, da Ihnen keine fortlaufende Datenübertragung zugeordnet ist. Alle zusätzlichen Audiofunktionen verwenden Geräte Bezeichner zur Identifizierung von Geräten.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio Ausgabe Datentypen

Die folgenden Datentypen werden für die Waveform-audioausgabefunktionen definiert.



| type                                 | BESCHREIBUNG                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hwaveout**                         | Handle für ein offenes Waveform-Audioausgabegerät.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | -Struktur, die die von einem bestimmten Waveform-Audioeingabegerät unterstützten Datenformate angibt. Diese Struktur ist auch für Waveform-Audioeingabegeräte geeignet. |
| [**Wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struktur, die als Header für einen Block von Waveform-audioeingabedaten verwendet wird. Diese Struktur wird auch für Waveform-Audioeingabegeräte verwendet.                            |
| [**Waveoutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | -Struktur, die verwendet wird, um die Funktionen eines bestimmten Waveform-Audioausgabegeräts abzufragen.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Angeben von Waveform-Audio Datenformaten

Wenn Sie die [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion aufrufen, um einen Gerätetreiber für die Wiedergabe zu öffnen oder abzufragen, ob der Treiber ein bestimmtes Datenformat unterstützt, verwenden Sie den *pwfx* -Parameter, um einen Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur anzugeben, die das angeforderte Waveform-Audiodatenformat enthält. **WaveFormatEx** ersetzt die [**wellenformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) -und [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) -Strukturen.

Für Audiodaten, die in mehr als zwei Kanäle getrennt sind oder eine Stichprobengröße haben, die kein Vielfaches von 8 ist, sollten Sie [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)verwenden. Diese Struktur konfiguriert einfach die zusätzlichen bytes, auf die der **CBSIZE** -Member von **WaveFormatEx** zeigt, um zusätzliche Informationen über das Format zu senden. **WAVEFORMATEXTENSIBLE** kann als **WaveFormatEx** umgewandelt werden.

Es gibt auch zwei Zwischenablage Formate, die Sie verwenden können, um Audiodaten darzustellen: CF \_ Wave und CF \_ Riff. Verwenden Sie das CF- \_ Wave-Format, um Daten in einem der Standardformate (z. b. 11 kHz oder 22-kHz-PCM) darzustellen. Verwenden Sie das CF- \_ Riff Format, um komplexere Datenformate darzustellen, die nicht als standardmäßige Waveform-Audiodateien dargestellt werden können.

## <a name="writing-waveform-audio-data"></a>Schreiben von Waveform-Audio Daten

Nachdem Sie einen Waveform-Audio-Ausgabegeräte Treiber erfolgreich geöffnet haben, können Sie mit der Wiedergabe eines Sounds beginnen. Windows stellt die [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) -Funktion zum Senden von Datenblöcken an Waveform-Audioausgabegeräte bereit.

Verwenden Sie die Struktur [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , um den mit **waveOutWrite** gesendeten Waveform-audiodatenblock anzugeben. Diese Struktur enthält einen Zeiger auf einen gesperrten Datenblock, die Länge des Datenblocks und einige Flags. Dieser Datenblock muss vorbereitet werden, bevor er verwendet werden kann. Weitere Informationen zum Vorbereiten eines Datenblocks finden Sie unter [Audiodatenblöcke](audio-data-blocks.md).

Nachdem Sie einen Datenblock mithilfe von **waveOutWrite** an ein Ausgabegerät gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn freigeben. Wenn Sie mehrere Datenblöcke senden, müssen Sie den Abschluss der Datenblöcke überwachen, um zu erfahren, wann zusätzliche Blöcke gesendet werden müssen. Weitere Informationen zu Datenblöcken finden Sie unter [Audiodatenblöcke](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>PCM-Waveform-Audio Daten Format

Der **lpdata** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur weist auf die Daten Beispiele für Waveform-Audiodaten hin. Bei 8-Bit-PCM-Daten wird jedes Beispiel durch ein einzelnes nicht signiertes Daten Byte dargestellt. Für 16-Bit-PCM-Daten wird jedes Beispiel durch einen 16-Bit-Wert mit Vorzeichen dargestellt. In der folgenden Tabelle werden die maximalen, minimalen und Mittelpunkt Werte für PCM-Wellenform-Audiodaten zusammengefasst.



|             |                 |                  |                |
|-------------|-----------------|------------------|----------------|
| Datenformat | Maximalwert   | Minimalwert    | Mittelpunkt Wert |
| 8-Bit-PCM   | 255 (0xFF)      | 0                | 128 (0x80)     |
| 16-Bit-PCM  | 32.767 (0x7FFF) | – 32.768 (0X8000) | 0              |



 

## <a name="pcm-data-packing"></a>PCM-Daten Verpackung

Die Reihenfolge der Daten Bytes variiert zwischen 8-Bit-und 16-Bit-Formaten und zwischen Mono-und Stereo-Formaten. In der folgenden Liste wird das Verpacken von Daten für die unterschiedlichen PCM-Datenformate für Waveform-Audiodateien beschrieben.



| PCM-Waveform-Audioformat | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8-Bit-Mono                | Jede Stichprobe ist 1 Byte, das einem einzelnen Audiokanal entspricht. In Beispiel 1 werden die Beispiele 2, 3, 4 usw. befolgt.                                                                                                                                                                                                                           |
| 8-Bit-Stereo              | Jede Stichprobe ist 2 Bytes. In Beispiel 1 werden die Beispiele 2, 3, 4 usw. befolgt. Für jedes Beispiel ist das erste Byte Channel 0 (der linke Kanal) und das zweite Byte Channel 1 (der Rechte Kanal).                                                                                                                                               |
| 16-Bit-Mono               | Jede Stichprobe ist 2 Bytes. In Beispiel 1 werden die Beispiele 2, 3, 4 usw. befolgt. Für jedes Beispiel ist das erste Byte das nieder wertige Byte von Channel 0 und das zweite Byte das hochwertige Byte von Channel 0.                                                                                                                                         |
| 16-Bit-Stereo             | Jede Stichprobe beträgt 4 Bytes. In Beispiel 1 werden die Beispiele 2, 3, 4 usw. befolgt. Für jede Stichprobe ist das erste Byte das nieder wertige Byte von Channel 0 (linker Kanal). Das zweite Byte ist das hochwertige Byte von Channel 0. Das dritte Byte ist das nieder wertige Byte von Channel 1 (Right Channel); und das vierte Byte ist das hochwertige Byte von Channel 1. |
| Sonstige                    | Jede Stichprobe ist in einem Block enthalten, der ein Vielfaches von 4 Bytes ist, aber die Beispiele sind möglicherweise nicht Byte bündig. Die Anordnung von Kanälen wird durch eine Maske angegeben. Weitere Informationen finden Sie unter [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Schließen von Waveform-Audio Ausgabegeräte

Nachdem Waveform-Audiowiedergabe abgeschlossen ist, wenden Sie [**waveoutclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) an, um das Ausgabegerät zu schließen. Wenn **waveoutclose** aufgerufen wird, während eine Waveform-Audiodatei abgespielt wird, schlägt der Close-Vorgang fehl, und die Funktion gibt einen Fehlercode zurück, der angibt, dass das Gerät nicht geschlossen wurde. Wenn Sie nicht warten möchten, bis die Wiedergabe beendet ist, bevor Sie das Gerät schließen, können Sie vor dem schließen die [**Wave-Set**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) -Funktion aufzurufen. Dies beendet die Wiedergabe und ermöglicht das Schließen des Geräts. Stellen Sie sicher, dass Sie die [**waveoutunprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) -Funktion verwenden, um die Vorbereitung für alle Datenblöcke vor dem Schließen des Geräts zu bereinigen.

 

 