---
description: In dieser Übersicht wird das RESOURCE INTERCHANGE-Dateiformat (Resource Interchange File Format) beschrieben, das in WAV-Dateien verwendet wird. DIE ist das typische Format, aus dem Audiodaten für XAudio2 geladen werden.
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: Resource Interchange File Format (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c223c5a1047ffc9828a42ccc09ce4a94f5e766a1bc4851996b911f15f90995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054330"
---
# <a name="resource-interchange-file-format-riff"></a>Resource Interchange File Format (RIFF)

In dieser Übersicht wird das RESOURCE INTERCHANGE-Dateiformat (Resource Interchange File Format) beschrieben, das in WAV-Dateien verwendet wird. DIE ist das typische Format, aus dem Audiodaten für XAudio2 geladen werden.

## <a name="riff"></a>RIFF

EineUNK-Datei besteht aus mehreren diskreten Datenabschnitten, die als *Chunks bezeichnet werden.*

## <a name="fourcc-identifiers"></a>FOURCC-Bezeichner

Der Datentyp in einem Block wird durch einen VIER-Zeichen-Codebezeichner (FOURCC) angegeben. Ein FOURCC ist eine 32-Bit-Ganzzahl ohne Vorzeichen, die durch Verkettung von vier ASCII-Zeichen erstellt wird, die zum Identifizieren von Blocktypen in einer ASCII-Datei verwendet werden. Beispielsweise wird FOURCC "abcd" auf einem Little-Endian-System als 0x64636261. FOURCCs können Leerzeichen enthalten, sodass "abc" ein gültiges FOURCC ist. Audiodateien verwenden FOURCC-Codes, um Audioformat-, Audiodaten- und andere, für das Audioformat spezifische Bereiche zu identifizieren.

Die folgende Tabelle zeigt die FOURCC-Bezeichner, die in den von XAudio2 unterstützten Audioformaten erwartet werden können. 

| Format | FOURCC-Bezeichner                     | Zusätzliche Informationen                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| PCM    | "MK", "fmt" , "data"                 |                                                                                                      |
| Adpcm  | "änder", "fmt", "data", "smpl", "wsmpl" | Eine Beschreibung der ADPCM-spezifischen FOURCC-Bezeichner finden Sie unter [Übersicht über ADPCM.](adpcm-overview.md) |



 

Die FOURCC-Bezeichner "SOLLEN", "fmt" und "data" gelten für alle unterstützten Formate. In der folgenden Tabelle werden die FOURCC-Bezeichner beschrieben, die in allen unterstützten Formaten gefunden werden. 

| FOURCC-Bezeichner | BESCHREIBUNG                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| „RIFF“            | Standard-BLOCK MIT EINEM Dateityp mit dem Wert "WAVE" oder "XWMA" in den ersten vier Bytes des Datenabschnitts und den anderen Blocken in der Datei im restlichen Datenabschnitt.                                   |
| „fmt“             | Enthält den Formatheader für die Audiodatei. Die Daten in diesem Block entsprechen einer der folgenden Strukturen: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.                                                  |
| „data“            | Enthält Audiodaten für die Audiodatei. In XAudio2 wird der Inhalt des Daten chunk in einen Puffer gelesen und als **pAudioData-Element** einer [**XAUDIO2 \_ BUFFER-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) an eine Quellstimme übergeben. |



 

## <a name="chunks"></a>Chunks

EineUNK-Datei besteht aus einem BLOCK DES-Blockes, der 0 (null) oder mehr andere Block enthält.

-   Der block -Block hat die folgende Form:

    "ENUMERATION", fileSize, fileType, data

    Dabei ist "COD" der literale FOURCC-Code "CODES", *fileSize* ein 4-Byte-Wert, der die Größe der Daten in der Datei anspricht, und *fileType* ist ein FOURCC, der den spezifischen Dateityp identifiziert. Der Wert von *fileSize* enthält die Größe des *fileType* FOURCC sowie die Größe der folgenden Daten, jedoch nicht die Größe des FOURCC"-Werts "ENUMERATION" oder die Größe von *fileSize.* Die Daten bestehen aus Teilen in beliebiger Reihenfolge.

-   Andere Chunks haben das folgende Formular:

    ```
    chunkID, chunkSize, data
    ```

    

    Dabei *ist chunkID* ein FOURCC-Wert, der die im Block enthaltenen Daten identifiziert, *chunkSize* ein 4-Byte-Wert, der die Größe des Datenabschnitts des Blockes an und die Daten 0 (null) oder mehr Byte an Daten sind. Die Daten werden immer bis zur nächsten WORD-Grenze aufschlossen. *chunkSize* gibt die Größe der gültigen Daten im Block an. Er enthält nicht die Aufleerung, die Größe von *chunkID* oder die Größe *von chunkSize.*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[So wird's gemacht: Wiedergeben von Ton mit XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 



