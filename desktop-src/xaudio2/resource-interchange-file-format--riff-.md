---
description: In dieser Übersicht wird das in WAV-Dateien verwendete Ressourcenaustausch Datei Format (-Riff) beschrieben. "Riff" ist das typische Format, aus dem Audiodaten für XAudio2 geladen werden.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Resource Interchange File Format (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363785"
---
# <a name="resource-interchange-file-format-riff"></a>Resource Interchange File Format (RIFF)

In dieser Übersicht wird das in WAV-Dateien verwendete Ressourcenaustausch Datei Format (-Riff) beschrieben. "Riff" ist das typische Format, aus dem Audiodaten für XAudio2 geladen werden.

## <a name="riff"></a>RIFF

Eine Riff Datei besteht aus mehreren diskreten Abschnitten von Daten, die als *Blöcke bezeichnet werden*.

## <a name="fourcc-identifiers"></a>FourCC-Bezeichner

Der Typ der Daten in einem Block wird durch einen vierstelligen Code (FourCC) angegeben. Ein FourCC ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen, die zum Identifizieren von Segmenttypen in einer Riff Datei verwendet werden, erstellt wird. Beispielsweise wird das FourCC "abcd" in einem Little-in-System als 0x64636261 dargestellt. Fourccs kann Leerzeichen enthalten, sodass "ABC" ein gültiges FourCC ist. Audiodateien verwenden FOURCC-Codes, um audioformatblöcke, Audiodatenblöcke und andere Segmente zu identifizieren, die für das Audioformat spezifisch sind.

Die folgende Tabelle zeigt die FourCC-IDs, die in den von XAudio2 unterstützten Audioformaten erwartet werden können. 

| Format | FourCC-Bezeichner                     | Zusätzliche Informationen                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "Riff", "f", "Data"                 |                                                                                                      |
| ADPCM  | "Riff", "f", "Data", "SMPL", "wsmpl" | Eine Beschreibung der ADPCM-spezifischen FourCC-IDs finden Sie unter [Übersicht über ADPCM](adpcm-overview.md) . |



 

Die FourCC-IDs "Riff", "fmt" und "Data" sind für alle unterstützten Formate üblich. In der folgenden Tabelle werden die FourCC-IDs beschrieben, die in allen unterstützten Formaten gefunden werden. 

| FourCC-Bezeichner | BESCHREIBUNG                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| „RIFF“            | Der Standard-Riff Block, der einen Dateityp mit dem Wert "Wave" oder "xwma" in den ersten vier Bytes des Daten Abschnitts und die anderen Blöcke in der Datei im Rest des Daten Abschnitts enthält.                                   |
| „fmt“             | Enthält den Format Header für die Audiodatei. Die Daten in diesem Block entsprechen einer der folgenden Strukturen: **WaveFormatEx**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| „data“            | Enthält Audiodaten für die Audiodatei. In XAudio2 wird der Inhalt des Datensegments in einen Puffer eingelesen und als **paudiodata** -Member einer [**XAudio2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur an eine Quell Stimme übergeben. |



 

## <a name="chunks"></a>Chunks

Eine Riff Datei besteht aus einem Riff Block, der 0 (null) oder mehr andere Blöcke enthält.

-   Der Riff Block weist die folgende Form auf:

    "Riff", Filesize, filetype, Data

    Wenn "Riff" der Literale FourCC-Code "Riff" ist, ist *FileSize* ein 4-Byte-Wert, der die Größe der Daten in der Datei angibt, und *filetype* ist ein FourCC, der den spezifischen Dateityp identifiziert. Der Wert von *FileSize* umfasst die Größe von *filetype* FourCC plus die Größe der nachfolgenden Daten, jedoch nicht die Größe des "Riff"-FourCC oder die Größe der *Dateigröße*. Die Daten bestehen aus Blöcken in beliebiger Reihenfolge.

-   Andere Blöcke weisen die folgende Form auf:

    ```
    chunkID, chunkSize, data
    ```

    

    Wenn " *segkid* " ein FourCC ist, das die im Block enthaltenen Daten identifiziert, ist " *ChunkSize* " ein 4-Byte-Wert, der die Größe des Abschnitts "Data" des Blocks angibt, und die Daten sind 0 (null) oder mehr Bytes an Daten. Die Daten werden immer bis zur nächsten Wort Grenze aufgefüllt. *ChunkSize* gibt die Größe der gültigen Daten im Block an. Es enthält keine Auffüll Zeichen, die Größe von *segbrocken* oder die Größe von Block *Größe*.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[So wird's gemacht: Wiedergeben von Ton mit XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 



