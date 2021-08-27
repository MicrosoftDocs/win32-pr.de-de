---
title: Geräte und Datentypen
description: Geräte und Datentypen
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- Waveformaudio, Öffnen von Ausgabegeräten
- Waveform-Audio-Schnittstelle, Öffnen von Ausgabegeräten
- Öffnen von Waveform-Audioausgabegeräten
- Waveformaudio, Abfragen von Ausgabegeräten
- Waveform-Audio-Schnittstelle, Abfragen von Ausgabegeräten
- Abfragen von Waveform-Audio-Ausgabegeräten
- Waveformaudio, Gerätehandles
- Waveform-Audio-Schnittstelle, Gerätehandles
- Waveformaudio, Gerätebezeichner
- Waveform-Audio-Schnittstelle, Gerätebezeichner
- Waveformaudio, Ausgabedatentypen
- Waveform-Audio-Schnittstelle, Ausgabedatentypen
- Waveform-Audio, Datenformate
- Waveform-Audio-Schnittstelle, Datenformate
- Schreiben von Waveform-Audiodaten
- Waveformaudio, Schreiben von Daten
- Waveform-Audio-Schnittstelle, Schreiben von Daten
- PCM-Waveform-Audiodaten
- Waveform-Audio, PCM-Daten
- Waveform-Audio-Schnittstelle, PCM-Daten
- Waveformaudio, Schließen von Ausgabegeräten
- Waveform-Audio-Schnittstelle, Schließen von Ausgabegeräten
- Schließen von Waveform-Audioausgabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 165f740e260c4e1a25fbd40cac9b8efd66ccd401c3e166dd1119b92c7b9999f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941268"
---
# <a name="devices-and-data-types"></a>Geräte und Datentypen

Dieser Abschnitt beschreibt die Arbeit mit Waveform-Audio-Geräten und enthält Informationen zum Öffnen, Schließen und Abfragen ihrer Funktionen. Außerdem wird beschrieben, wie Die Geräte in einem System mithilfe von Gerätehandles und Gerätebezeichnern nachverfolgt werden.

## <a name="opening-waveform-audio-output-devices"></a>Öffnen Waveform-Audio Ausgabegeräte

Verwenden Sie die [**WaveOutOpen-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) um ein Waveform-Audio-Ausgabegerät für die Wiedergabe zu öffnen. Diese Funktion öffnet das Gerät, das dem angegebenen Gerätebezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle eines angegebenen Speicherorts geschrieben wird.

Einige Multimediacomputer verfügen über mehrere Waveform-Audioausgabegeräte. Wenn Sie kein bestimmtes Waveform-Audio-Ausgabegerät in einem System öffnen möchten, sollten Sie beim Öffnen eines Geräts das WAVE \_ MAPPER-Flag für den Gerätebezeichner verwenden. Die **waveOutOpen-Funktion** wählt das Gerät im System aus, das das angegebene Datenformat am besten wiedergeben kann.

## <a name="querying-audio-devices"></a>Abfragen von Audiogeräten

Windows stellt die folgenden Funktionen bereit, um zu bestimmen, wie viele Geräte eines bestimmten Typs in einem System verfügbar sind.



| Funktion                                       | Beschreibung                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Ruft die Anzahl der zusätzlichen Ausgabegeräte ab, die im System vorhanden sind.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Ruft die Anzahl der im System vorhandenen Waveform-Audio-Eingabegeräte ab.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Ruft die Anzahl der im System vorhandenen Waveform-Audio-Ausgabegeräte ab. |



 

Audiogeräte werden durch einen Gerätebezeichner identifiziert. Der Gerätebezeichner wird implizit anhand der Anzahl der in einem System vorhandenen Geräte bestimmt. Gerätebezeichner reichen von 0 bis 1 kleiner als die Anzahl der vorhandenen Geräte. Wenn beispielsweise zwei Waveform-Audio-Ausgabegeräte in einem System vorhanden sind, sind die gültigen Gerätebezeichner 0 und 1.

Nachdem Sie ermittelt haben, wie viele Geräte eines bestimmten Typs in einem System vorhanden sind, können Sie eine der folgenden Funktionen verwenden, um die Funktionen der einzelnen Geräte abzufragen.



| Funktion                                       | Beschreibung                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Ruft die Funktionen eines angegebenen Hilfsausgabegeräts ab.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Ruft die Funktionen eines angegebenen Waveform-Audio-Eingabegeräts ab.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Ruft die Funktionen eines angegebenen Waveform-Audio-Ausgabegeräts ab. |



 

Jede dieser Funktionen füllt eine -Struktur mit Informationen zu den Funktionen eines angegebenen Geräts. In der folgenden Tabelle sind die Strukturen aufgeführt, die den einzelnen Funktionen entsprechen.



|  Funktion                                              |  Struktur                                  |
|------------------------------------------------|------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Standardformate werden im **dwFormats-Member** der **WAVEOUTCAPS-Struktur** aufgeführt. Waveform-Audio-Geräte können nicht standardmäßige Formate unterstützen. Um zu bestimmen, ob ein bestimmtes Format (Standard oder Nichtstandard) von einem Gerät unterstützt wird, können Sie die [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) mit dem WAVE \_ FORMAT \_ QUERY-Flag aufrufen. Dieses Flag öffnet das Gerät nicht. Sie geben das betreffende Format in der [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) an, auf das der *pwfx-Parameter* zeigt, der an **waveOutOpen** übergeben wird.

Waveform-Audio-Ausgabegeräte variieren in den Funktionen, die sie unterstützen. Der **dwSupport-Member** der [**WAVEOUTCAPS-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) gibt an, ob ein Gerät Funktionen wie Volumen- und Tonhöhenänderungen unterstützt.

## <a name="device-handles-and-device-identifiers"></a>Gerätehandles und Gerätebezeichner

Jede Funktion, die ein Audiogerät öffnet, gibt einen Gerätebezeichner, einen Zeiger auf eine Speicherposition und einige Parameter an, die für jeden Gerätetyp eindeutig sind. Die Speicherposition wird mit einem Gerätehandle gefüllt. Verwenden Sie dieses Gerätehandle, um das geöffnete Audiogerät beim Aufrufen anderer Audiofunktionen zu identifizieren.

Der Unterschied zwischen Bezeichnern und Handles für Audiogeräte ist dezent, aber wichtig:

-   Gerätebezeichner werden implizit anhand der Anzahl der in einem System vorhandenen Geräte bestimmt. Diese Zahl wird mithilfe der [**Funktion auxGetNumDevs,**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)oder [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) abgerufen.
-   Gerätehandles werden zurückgegeben, wenn Gerätetreiber mithilfe der [**WaveInOpen-**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) oder [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) geöffnet werden.

Es gibt keine Funktionen, die zusätzliche Audiogeräte öffnen oder schließen. Zusätzliche Audiogeräte müssen nicht wie Waveform-Audiogeräte geöffnet und geschlossen werden, da ihnen keine kontinuierliche Datenübertragung zugeordnet ist. Alle zusätzlichen Audiofunktionen verwenden Gerätebezeichner, um Geräte zu identifizieren.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio-Ausgabedatentypen

Die folgenden Datentypen sind für Waveform-Audio-Ausgabefunktionen definiert.



| type                                 | Beschreibung                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Handle für ein geöffnetes Waveform-Audio-Ausgabegerät.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Struktur, die die Von einem bestimmten Waveform-Audio-Eingabegerät unterstützten Datenformate angibt. Diese Struktur wird auch für Waveform-Audio-Eingabegeräte verwendet. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struktur, die als Header für einen Block von Waveform-Audio-Eingabedaten verwendet wird. Diese Struktur wird auch für Waveform-Audio-Eingabegeräte verwendet.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Struktur zum Abfragen der Funktionen eines bestimmten Waveform-Audio-Ausgabegeräts.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Angeben Waveform-Audio Datenformate

Wenn Sie die [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) aufrufen, um einen Gerätetreiber für die Wiedergabe zu öffnen oder um zu abfragen, ob der Treiber ein bestimmtes Datenformat unterstützt, verwenden Sie den *pwfx-Parameter,* um einen Zeiger auf eine [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) anzugeben, die das angeforderte Waveform-Audio-Datenformat enthält. **WAVEFORMATEX** ersetzt die [**STRUKTUREN WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) und [**PCMWAVEFORMAT.**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)

Für Audiodaten, die in mehr als zwei Kanäle getrennt sind oder eine Stichprobengröße haben, die kein Vielfaches von 8 ist, sollten Sie [**WAVEFORMATEXTENSIBLE verwenden.**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) Diese Struktur konfiguriert einfach die zusätzlichen Bytes, auf die das **cbSize-Member** von **WAVEFORMATEX** verweist, um zusätzliche Informationen über das Format zu geben. **WAVEFORMATEXTENSIBLE** kann in **WAVEFORMATEX umgeformt werden.**

Es gibt auch zwei Formate für die Zwischenablage, die Sie zum Darstellen von Audiodaten verwenden können: CF \_ WAVE und \_ CFDATENÜBERTRAGUNG. Verwenden Sie das CF WAVE-Format, um Daten in einem der Standardformate wie \_ 11 kHz oder 22 kHz PCM zu darstellen. Verwenden Sie das \_ CF-FORMAT FÜR DIE Darstellung komplexerer Datenformate, die nicht als Standard-Waveform-Audiodateien dargestellt werden können.

## <a name="writing-waveform-audio-data"></a>Schreiben Waveform-Audio Daten

Nachdem Sie erfolgreich einen Waveform-Audio-Ausgabegerätetreiber geöffnet haben, können Sie mit der Wiedergabe eines Sounds beginnen. Windows stellt die [**waveOutWrite-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) zum Senden von Datenblöcken an Waveform-Audioausgabegeräte zur Verfügung.

Verwenden Sie [**die WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) um den Waveform-Audio-Datenblock anzugeben, den Sie mit **waveOutWrite senden.** Diese Struktur enthält einen Zeiger auf einen gesperrten Datenblock, die Länge des Datenblocks und einige Flags. Dieser Datenblock muss vorbereitet werden, bevor Sie ihn verwenden. Informationen zum Vorbereiten eines Datenblocks finden Sie unter [AudioDatenblöcke](audio-data-blocks.md).

Nachdem Sie einen Datenblock mit **waveOutWrite** an ein Ausgabegerät gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn wieder frei geben. Wenn Sie mehrere Datenblöcke senden, müssen Sie den Abschluss von Datenblöcken überwachen, um zu wissen, wann zusätzliche Blöcke gesendet werden sollen. Weitere Informationen zu Datenblöcken finden Sie unter [AudioDatenblöcke](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>PCMWaveform-Audio Datenformat

Der **lpData-Member** der [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) verweist auf die Waveform-Audio-Datenbeispiele. Bei 8-Bit-PCM-Daten wird jedes Beispiel durch ein einzelnes Daten byte ohne Vorzeichen dargestellt. Bei 16-Bit-PCM-Daten wird jedes Beispiel durch einen 16-Bit-Wert mit Vorsigniert dargestellt. In der folgenden Tabelle sind die Maximalen-, Minimal- und Mittelpunktwerte für PCM-Waveform-Audiodaten zusammengefasst.



| Datenformat | Maximalwert   | Minimalwert    | Mittelpunktwert |
|-------------|-----------------|------------------|----------------|
| 8-Bit-PCM   | 255 (0xFF)      | 0                | 128 (0x80)     |
| 16-Bit-PCM  | 32.767 (0x7FFF) | –32.768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>PCM-Datenpackung

Die Reihenfolge der Datenbytes variiert zwischen 8-Bit- und 16-Bit-Formaten sowie zwischen Mono- und Stereoformaten. Die folgende Liste beschreibt das Packen von Daten für die verschiedenen PCM-Waveform-Audio-Datenformate.



| PCM-Waveform-Audioformat | Beschreibung                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8-Bit-Mono                | Jedes Beispiel ist ein Byte, das einem einzelnen Audiokanal entspricht. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 und so weiter.                                                                                                                                                                                                                           |
| 8-Bit-Stereo              | Jedes Beispiel ist 2 Bytes. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 und so weiter. Für jedes Beispiel ist das erste Byte Kanal 0 (der linke Kanal), und das zweite Byte ist Kanal 1 (der rechte Kanal).                                                                                                                                               |
| 16-Bit-Mono               | Jedes Beispiel ist 2 Bytes. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 und so weiter. Für jede Stichprobe ist das erste Byte das niedrig geordnete Byte von Kanal 0, und das zweite Byte ist das obere Byte von Channel 0.                                                                                                                                         |
| 16-Bit-Stereo             | Jedes Beispiel ist 4 Bytes. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 und so weiter. Für jedes Beispiel ist das erste Byte das niedrig geordnete Byte von Kanal 0 (linker Kanal). Das zweite Byte ist das obere Byte von Channel 0. Das dritte Byte ist das niedrige Byte von Kanal 1 (rechter Kanal). und das vierte Byte ist das obere Byte von Channel 1. |
| Sonstige                    | Jedes Beispiel ist in einem -Block enthalten, der ein Vielfaches von 4 Bytes ist, aber die Stichproben können nicht bytebündig ausgerichtet sein. Die Anordnung von Kanälen wird durch eine Maske angegeben. Weitere Informationen finden Sie unter [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Schließen Waveform-Audio Ausgabegeräten

Nachdem die Wiedergabe von Waveform-Audio abgeschlossen ist, rufen Sie [**waveOutClose auf,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) um das Ausgabegerät zu schließen. Wenn **waveOutClose aufgerufen** wird, während eine Waveform-Audiodatei abspielt, schlägt der Schließvorgang fehl, und die Funktion gibt einen Fehlercode zurück, der angibt, dass das Gerät nicht geschlossen wurde. Wenn Sie nicht warten möchten, bis die Wiedergabe beendet ist, bevor Sie das Gerät schließen, rufen Sie die [**waveOutReset-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) vor dem Schließen auf. Dadurch wird die Wiedergabe beendet, und das Gerät kann geschlossen werden. Stellen Sie sicher, dass Sie die [**WaveOutUnprepareHeader-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) verwenden, um die Vorbereitung für alle Datenblöcke zu bereinige, bevor Sie das Gerät schließen.

 

 