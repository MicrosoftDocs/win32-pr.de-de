---
description: MPEG-2-Splittermedientypen
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2-Splittermedientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e025fafabdeb8c437cc1d1cd6fbb843cf63e3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119975"
---
# <a name="mpeg-2-splitter-media-types"></a>MPEG-2-Splittermedientypen

Der [MPEG-2-Splitterfilter](mpeg-2-splitter.md) unterstützt derzeit Audio und Video. Dolby AC-3 wird als Unterstream unterstützt, wie von dvd definiert. Der Filter unterstützt auch MPEG-2-Audio. Die Medientypen hängen davon ab, ob der MPEG-2-Splitter PES-Pakete oder PES-Nutzlasten liefert.

### <a name="video"></a>Video

Für MPEG-2-Videos sind die Medientypen wie folgt.


|                | PES-Ausgabe | Nutzlastausgabe
|------------------|------------------------------------------|--------------------------------|
| **Haupttyp**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **\_MEDIATYPE-Video**           |
| **Untertyp**          | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**           | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO** |
| **Formattyp**      | **FORMAT \_ MPEG2Video**                   | **FORMAT \_ MPEG2Video**         |
| **Formatstruktur** | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>AC-3-Audio

Für AC-3-Audio sind die Medientypen wie folgt.

| | PES-Ausgabe | Nutzlastausgabe |
|------------------|--------------------------------------|------------------------------|
| **Haupttyp**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **MEDIATYPE \_ Audio**         |
| **Untertyp**          | **MEDIASUBTYPE \_ DOLBY \_ AC3**             | **MEDIASUBTYPE \_ DOLBY \_ AC3** |
| **Formattyp**      | FORMAT \_ WaveFormatEx                 | **FORMAT \_ WaveFormatEx**     |
| **Formatstruktur** | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für AC-3 ist derzeit **WAVE FORMAT \_ \_ UNKNOWN**, aber dies kann sich ändern.

### <a name="mpeg-2-audio"></a>MPEG-2-Audio

Für MPEG-2-Audio sind die Medientypen wie folgt.



|  | PES-Ausgabe | Nutzlastausgabe |
|------------------|-------------------------------|--------------------------------|
| **Haupttyp**       | **MEDIATYPE \_ MPEG2 \_ PES**     | **MEDIATYPE \_ Audio**           |
| **Untertyp**          | **MEDIASUBTYE \_ MPEG2 \_ AUDIO** | **MEDIASUBTYPE \_ MPEG2 \_ AUDIO** |
| **Formattyp**      | **FORMAT \_ WaveFormatEx**      | **FORMAT \_ WaveFormatEx**       |
| **Formatstruktur** | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für MPEG-2 Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN**, aber dies kann sich ändern.

Der MPEG-2-Splitter geht davon aus, dass Streams D0 über DF für den Multichannel-Erweiterungsstream verwendet werden, ebenso wie für DVD MPEG-2-Audio. Daher leitet der Splitter immer dann, wenn Stream C *x* ausgewählt wird, die Pakete für Stream D *x* weiter.

### <a name="lpcm-audio"></a>LPCM-Audio

Für LPCM-Audio sind die Medientypen wie folgt.



|  | PES-Ausgabe | Nutzlastausgabe |
|------------------|------------------------------------|------------------------------------|
| **Haupttyp**       | **MEDIATYPE \_ MPEG2 \_ PES**          | **MEDIATYPE \_ Audio**               |
| **Untertyp**          | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** |
| **Formattyp**      | **FORMAT \_ WaveFormatEx**           | **FORMAT \_ WaveFormatEx**           |
| **Formatstruktur** | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für LPCM-Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN,** aber dies kann sich ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 
