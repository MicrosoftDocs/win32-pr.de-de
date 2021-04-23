---
description: MPEG-2-Splitter-Medientypen
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2-Splitter-Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909427"
---
# <a name="mpeg-2-splitter-media-types"></a>MPEG-2-Splitter-Medientypen

Der [MPEG-2-Splitterfilter](mpeg-2-splitter.md) unterstützt derzeit Audio und Video. Dolby AC-3 wird als Teilstream unterstützt, wie von DVD definiert. Der Filter unterstützt auch MPEG-2-Audio. Die Medientypen hängen davon ab, ob der MPEG-2-Splitter PES-Pakete oder PES-Nutzlasten liefert.

### <a name="video"></a>Video

Für MPEG-2-Videos lauten die Medientypen wie folgt.



| Bezeichnung | Wert |
|------------------|------------------------------------------|--------------------------------|
|                  | PES-Ausgabe                               | Nutzlastausgabe                 |
| Haupttyp       | **MEDIATYPE \_ MPEG2 \_ PES**                | **\_MEDIATYPE-Video**           |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**           | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO** |
| Formattyp      | **FORMAT \_ MPEG2Video**                   | **FORMAT \_ MPEG2Video**         |
| Formatstruktur | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>AC-3-Audio

Für AC-3-Audio sind die Medientypen wie folgt.



| Bezeichnung | Wert |
|------------------|--------------------------------------|------------------------------|
|                  | PES-Ausgabe                           | Nutzlastausgabe               |
| Haupttyp       | MEDIATYPE \_ MPEG2 \_ PES                | **MEDIATYPE \_ Audio**         |
| Subtype          | MEDIASUBTYPE \_ DOLBY \_ AC3             | **MEDIASUBTYPE \_ DOLBY \_ AC3** |
| Formattyp      | FORMAT \_ WaveFormatEx                 | **FORMAT \_ WaveFormatEx**     |
| Formatstruktur | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für AC-3 ist derzeit **WAVE FORMAT \_ \_ UNKNOWN**, aber dies kann sich ändern.

### <a name="mpeg-2-audio"></a>MPEG-2-Audio

Für MPEG-2-Audio sind die Medientypen wie folgt.



| Bezeichnung | Wert |
|------------------|-------------------------------|--------------------------------|
|                  | PES-Ausgabe                    | Nutzlastausgabe                 |
| Haupttyp       | **MEDIATYPE \_ MPEG2 \_ PES**     | **MEDIATYPE \_ Audio**           |
| Subtype          | **MEDIASUBTYE \_ \_ MPEG2-AUDIO** | **MEDIASUBTYPE \_ \_ MPEG2-AUDIO** |
| Formattyp      | **FORMAT \_ WaveFormatEx**      | **FORMAT \_ WaveFormatEx**       |
| Formatstruktur | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

Das **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für MPEG-2 Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN,** aber dies kann sich ändern.

Der MPEG-2-Splitter geht davon aus, dass datenströme D0 bis DF für den Multichannel-Erweiterungsstream verwendet werden, wie sie für MPEG-2-DVD-Audio verwendet werden. Daher werden die Pakete bei jeder Auswahl von Stream C *x* vom Splitter auch für Stream D *x* weitergeleitet.

### <a name="lpcm-audio"></a>LPCM-Audio

Für LPCM-Audio lauten die Medientypen wie folgt.



| Bezeichnung | Wert |
|------------------|------------------------------------|------------------------------------|
|                  | PES-Ausgabe                         | Nutzlastausgabe                     |
| Haupttyp       | **MEDIATYPE \_ MPEG2 \_ PES**          | **MEDIATYPE \_ Audio**               |
| Subtype          | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** |
| Formattyp      | **FORMAT \_ WaveFormatEx**           | **FORMAT \_ WaveFormatEx**           |
| Formatstruktur | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Der **wFormatTag-Member** der **WAVEFORMATEX-Struktur** für LPCM-Audio ist derzeit **WAVE FORMAT \_ \_ UNKNOWN,** aber dies kann sich ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 
