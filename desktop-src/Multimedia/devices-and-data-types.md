---
title: Geräte und Datentypen
description: Geräte und Datentypen
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- Waveform-Audio, Öffnen von Ausgabegeräten
- Waveform-Audioschnittstelle, Öffnen von Ausgabegeräten
- Öffnen von Waveform-Audio-Ausgabegeräten
- Waveform-Audio, Abfragen von Ausgabegeräten
- Waveform-Audio-Schnittstelle, Abfragen von Ausgabegeräten
- Abfragen von Waveform-Audio-Ausgabegeräten
- Waveform-Audio, Gerätehandles
- Waveform-Audio-Schnittstelle, Gerätehandles
- Waveform-Audio, Gerätebezeichner
- Waveform-Audio-Schnittstelle, Gerätebezeichner
- Waveform-Audio, Ausgabedatentypen
- Waveform-Audio-Schnittstelle, Ausgabedatentypen
- Waveform-Audio, Datenformate
- Waveform-Audio-Schnittstelle,Datenformate
- Schreiben von Waveform-Audiodaten
- Waveform-Audio, Schreiben von Daten
- Waveform-Audio-Schnittstelle, Schreiben von Daten
- PCM-Waveform-Audiodaten
- Waveform-Audio, PCM-Daten
- Waveform-Audio-Schnittstelle, PCM-Daten
- Waveform-Audio, Schließen von Ausgabegeräten
- Waveform-Audio-Schnittstelle, Schließen von Ausgabegeräten
- Schließen von Waveform-Audio-Ausgabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abe0c2c20c52f4498316fb619885d41f85e41d6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120245"
---
# <a name="devices-and-data-types"></a>Geräte und Datentypen

Dieser Abschnitt beschreibt die Arbeit mit Waveform-Audiogeräten und enthält Informationen zum Öffnen, Schließen und Abfragen ihrer Funktionen. Außerdem wird beschrieben, wie Die Geräte in einem System mithilfe von Gerätehandles und Gerätebezeichnern nachverfolgt werden.

## <a name="opening-waveform-audio-output-devices"></a>Öffnen Waveform-Audio Ausgabegeräten

Verwenden Sie die [**waveOutOpen-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) um ein Waveform-Audio-Ausgabegerät für die Wiedergabe zu öffnen. Diese Funktion öffnet das Gerät, das der angegebenen Geräte-ID zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle eines angegebenen Speicherorts geschrieben wird.

Einige Multimediacomputer verfügen über mehrere Waveform-Audio-Ausgabegeräte. Wenn Sie kein bestimmtes Waveform-Audio-Ausgabegerät in einem System öffnen möchten, sollten Sie das WAVE MAPPER-Flag für die Geräte-ID verwenden, wenn Sie \_ ein Gerät öffnen. Die **waveOutOpen-Funktion** wählt das Gerät im System aus, das das angegebene Datenformat am besten wiedererkennen kann.

## <a name="querying-audio-devices"></a>Abfragen von Audiogeräten

Windows stellt die folgenden Funktionen bereit, um zu bestimmen, wie viele Geräte eines bestimmten Typs in einem System verfügbar sind.



| Funktion                                       | Beschreibung                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Ruft die Anzahl der zusätzlichen Ausgabegeräte ab, die im System vorhanden sind.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Ruft die Anzahl der waveform-audio-Eingabegeräte ab, die im System vorhanden sind.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Ruft die Anzahl der waveform-audio-Ausgabegeräte ab, die im System vorhanden sind. |



 

Audiogeräte werden durch eine Geräte-ID identifiziert. Der Gerätebezeichner wird implizit anhand der Anzahl von Geräten bestimmt, die in einem System vorhanden sind. Gerätebezeichner reichen von 0 bis 1 kleiner als die Anzahl vorhandener Geräte. Wenn beispielsweise zwei Waveform-Audio-Ausgabegeräte in einem System enthalten sind, sind die gültigen Gerätebezeichner 0 und 1.

Nachdem Sie ermittelt haben, wie viele Geräte eines bestimmten Typs in einem System vorhanden sind, können Sie eine der folgenden Funktionen verwenden, um die Funktionen der einzelnen Geräte abfragt.



| Funktion                                       | Beschreibung                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Ruft die Funktionen eines angegebenen Hilfsausgabegeräts ab.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Ruft die Funktionen eines angegebenen Waveform-Audio-Eingabegeräts ab.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Ruft die Funktionen eines angegebenen Waveform-Audio-Ausgabegeräts ab. |



 

Jede dieser Funktionen füllt eine -Struktur mit Informationen über die Funktionen eines angegebenen Geräts. In der folgenden Tabelle sind die Strukturen aufgeführt, die den einzelnen Funktionen entsprechen.



|  Funktion                                              |  Struktur                                  |
|------------------------------------------------|------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

Standardformate werden im **dwFormats-Member** der **WAVEOUTCAPS-Struktur** aufgeführt. Waveform-Audio-Geräte können nicht standardmäßige Formate unterstützen. Um zu bestimmen, ob ein bestimmtes Format (Standard oder Nichtstandard) von einem Gerät unterstützt wird, können Sie die [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) mit dem WAVE \_ FORMAT \_ QUERY-Flag aufrufen. Dieses Flag öffnet das Gerät nicht. Sie geben das in Frage stellende Format in der [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) an, auf die durch den *pwfx-Parameter* verwiesen wird, der an **waveOutOpen übergeben wird.**

Waveform-Audio-Ausgabegeräte unterscheiden sich in den unterstützten Funktionen. Das **dwSupport-Member** der [**WAVEOUTCAPS-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) gibt an, ob ein Gerät Funktionen wie Volumen- und Tonhöhenänderungen unterstützt.

## <a name="device-handles-and-device-identifiers"></a>Gerätehandles und Gerätebezeichner

Jede Funktion, die ein Audiogerät öffnet, gibt einen Gerätebezeichner, einen Zeiger auf einen Speicherort und einige Parameter an, die für jeden Gerätetyp eindeutig sind. Der Speicherort wird mit einem Gerätehandpunkt gefüllt. Verwenden Sie dieses Gerätehand handle, um das geöffnete Audiogerät beim Aufrufen anderer Audiofunktionen zu identifizieren.

Der Unterschied zwischen Bezeichnern und Handles für Audiogeräte ist dezent, aber wichtig:

-   Gerätebezeichner werden implizit anhand der Anzahl der geräte in einem System bestimmt. Diese Zahl wird mithilfe der [**Funktion auxGetNumDevs,**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)oder [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) ermittelt.
-   Gerätehandles werden zurückgegeben, wenn Gerätetreiber mithilfe der [**WaveInOpen-**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) oder [**waveOutOpen-Funktion geöffnet**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) werden.

Es gibt keine Funktionen, die zusätzliche Audiogeräte öffnen oder schließen. Zusätzliche Audiogeräte müssen nicht wie Waveform-Audiogeräte geöffnet und geschlossen werden, da ihnen keine kontinuierliche Datenübertragung zugeordnet ist. Alle zusätzlichen Audiofunktionen verwenden Gerätebezeichner, um Geräte zu identifizieren.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio Ausgabedatentypen

Die folgenden Datentypen sind für Waveform-Audio-Ausgabefunktionen definiert.



| Typ                                 | Beschreibung                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Handle für ein offenes Waveform-Audio-Ausgabegerät.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Struktur, die die Datenformate angibt, die von einem bestimmten Waveform-Audio-Eingabegerät unterstützt werden. Diese Struktur wird auch für Waveform-Audioeingabegeräte verwendet. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struktur, die als Header für einen Block von Wellenform-Audio-Eingabedaten verwendet wird. Diese Struktur wird auch für Waveform-Audioeingabegeräte verwendet.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Struktur, die zum Abfragen der Funktionen eines bestimmten Waveform-Audioausgabegeräts verwendet wird.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Angeben Waveform-Audio Datenformate

Wenn Sie die [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) aufrufen, um einen Gerätetreiber für die Wiedergabe zu öffnen oder abzufragen, ob der Treiber ein bestimmtes Datenformat unterstützt, verwenden Sie den *pwfx-Parameter,* um einen Zeiger auf eine [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) anzugeben, die das angeforderte Waveform-Audio-Datenformat enthält. **WAVEFORMATEX** ersetzt die [**WAVEFORMAT-**](/windows/win32/api/mmreg/ns-mmreg-waveformat) und [**PCMWAVEFORMAT-Strukturen.**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)

Für Audiodaten, die in mehr als zwei Kanäle unterteilt sind oder eine Stichprobengröße haben, die kein Vielfaches von 8 ist, sollten Sie [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible)verwenden. Diese Struktur konfiguriert einfach die zusätzlichen Bytes, auf die der **cbSize-Member** von **WAVEFORMATEX** zeigt, um zusätzliche Informationen zum Format zu erhalten. **WAVEFORMATEXTENSIBLE** kann in **WAVEFORMATEX** umgecastet werden.

Es gibt auch zwei Zwischenablageformate, die Sie zur Darstellung von Audiodaten verwenden können: CF \_ WAVE und CF \_ DATEIFORMAT. Verwenden Sie das CF \_ WAVE-Format, um Daten in einem der Standardformate darzustellen, z. B. 11 kHz oder 22 kHz PCM. Verwenden Sie das CF \_ DATEIFORMAT-Format, um komplexere Datenformate darzustellen, die nicht als Standard-Waveform-Audiodateien dargestellt werden können.

## <a name="writing-waveform-audio-data"></a>Schreiben Waveform-Audio Daten

Nachdem Sie einen Waveform-Audio-Ausgabegerätetreiber erfolgreich geöffnet haben, können Sie mit der Wiedergabe eines Sounds beginnen. Windows stellt die [**waveOutWrite-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) zum Senden von Datenblöcken an Waveform-Audio-Ausgabegeräte bereit.

Verwenden Sie die [**WAVEHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) um den waveform-audio-Datenblock anzugeben, den Sie mit **waveOutWrite** senden. Diese Struktur enthält einen Zeiger auf einen gesperrten Datenblock, die Länge des Datenblocks und einige Flags. Dieser Datenblock muss vorbereitet werden, bevor Sie ihn verwenden. Informationen zum Vorbereiten eines Datenblocks finden Sie unter [Audiodatenblöcke.](audio-data-blocks.md)

Nachdem Sie einen Datenblock mit **waveOutWrite** an ein Ausgabegerät gesendet haben, müssen Sie warten, bis der Gerätetreiber mit dem Datenblock fertig ist, bevor Sie ihn freigeben. Wenn Sie mehrere Datenblöcke senden, müssen Sie die Vervollständigung von Datenblöcken überwachen, um zu wissen, wann zusätzliche Blöcke gesendet werden sollen. Weitere Informationen zu Datenblöcken finden Sie unter [Audiodatenblöcke.](audio-data-blocks.md)

## <a name="pcm-waveform-audio-data-format"></a>PCM Waveform-Audio-Datenformat

Der **lpData-Member** der [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) verweist auf die Waveform-Audio-Datenbeispiele. Für 8-Bit-PCM-Daten wird jedes Beispiel durch ein einzelnes Byte ohne Vorzeichen dargestellt. Bei 16-Bit-PCM-Daten wird jedes Beispiel durch einen 16-Bit-Wert mit Vorzeichen dargestellt. In der folgenden Tabelle werden die maximalen, minimalen und mittleren Werte für PCM Waveform-Audio-Daten zusammengefasst.



| Datenformat | Maximalwert   | Minimalwert    | Mittelpunktwert |
|-------------|-----------------|------------------|----------------|
| 8-Bit-PCM   | 255 (0xFF)      | 0                | 128 (0x80)     |
| 16-Bit-PCM  | 32.767 (0x7FFF) | –32.768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>PCM-Datenpacken

Die Reihenfolge der Datenbytes variiert zwischen 8-Bit- und 16-Bit-Formaten sowie zwischen Mono- und Stereoformaten. In der folgenden Liste wird das Packen von Daten für die verschiedenen PCM-Waveform-Audio-Datenformate beschrieben.



| PCM-Waveform-Audioformat | Beschreibung                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8-Bit-Mono                | Jedes Beispiel ist 1 Byte, das einem einzelnen Audiokanal entspricht. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 usw.                                                                                                                                                                                                                           |
| 8-Bit-Stereo              | Jedes Beispiel ist 2 Bytes. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 usw. Für jedes Beispiel ist das erste Byte Kanal 0 (der linke Kanal) und das zweite Byte Kanal 1 (der rechte Kanal).                                                                                                                                               |
| 16-Bit-Mono               | Jedes Beispiel ist 2 Bytes. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 usw. Für jedes Beispiel ist das erste Byte das Low-Order-Byte des Kanals 0 und das zweite Byte das hochwertige Byte des Kanals 0.                                                                                                                                         |
| 16-Bit-Stereo             | Jedes Beispiel ist 4 Bytes. Auf Beispiel 1 folgen die Beispiele 2, 3, 4 usw. Für jedes Beispiel ist das erste Byte das Low-Order-Byte des Kanals 0 (linker Kanal). Das zweite Byte ist das höher geordnete Byte des Kanals 0. das dritte Byte ist das Low-Order-Byte von Kanal 1 (rechter Kanal); und das vierte Byte ist das hohe Byte des Kanals 1. |
| Sonstige                    | Jedes Beispiel ist in einem Block enthalten, der ein Vielfaches von 4 Bytes ist, aber die Stichproben können nicht bytebündig ausgerichtet sein. Die Anordnung von Kanälen wird durch eine Maske angegeben. Weitere Informationen finden Sie unter [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Schließen von Waveform-Audio Ausgabegeräten

Nachdem die Wiedergabe von Waveform-Audio abgeschlossen ist, rufen Sie [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) auf, um das Ausgabegerät zu schließen. Wenn **waveOutClose** aufgerufen wird, während eine Waveform-Audiodatei wiedergegeben wird, schlägt der Schließvorgang fehl, und die Funktion gibt einen Fehlercode zurück, der angibt, dass das Gerät nicht geschlossen wurde. Wenn Sie nicht warten möchten, bis die Wiedergabe beendet ist, bevor Sie das Gerät schließen, rufen Sie die [**waveOutReset-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) vor dem Schließen auf. Dadurch wird die Wiedergabe beendet, und das Gerät kann geschlossen werden. Achten Sie darauf, die [**WaveOutUnprepareHeader-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) zu verwenden, um die Vorbereitung für alle Datenblöcke zu bereinigen, bevor Sie das Gerät schließen.

 

 