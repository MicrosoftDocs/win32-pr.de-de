---
description: MPEG-2-Splitter Medientypen
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: MPEG-2-Splitter Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355716"
---
# <a name="mpeg-2-splitter-media-types"></a>MPEG-2-Splitter Medientypen

Der [MPEG-2-Splitter](mpeg-2-splitter.md) Filter unterstützt derzeit Audiodateien und Videos. Dolby AC-3 wird als ein untergeordneter Stream unterstützt, wie von DVD definiert. Der Filter unterstützt auch MPEG-2-Audiodaten. Die Medientypen hängen davon ab, ob der MPEG-2-Splitter PE-Pakete oder PE-Nutzlasten bereitstellt.

### <a name="video"></a>Video

Bei MPEG-2-Videos lauten die Medientypen wie folgt.



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | Ausgabe von PES                               | Nutz Last Ausgabe                 |
| Haupttyp       | **MediaType \_ MPEG2 \_**                | **MediaType- \_ Video**           |
| Subtype          | **Video zu mediasubtype \_ MPEG2 \_**           | **Video zu mediasubtype \_ MPEG2 \_** |
| Formattyp      | **MPEG2Video formatieren \_**                   | **MPEG2Video formatieren \_**         |
| Format Struktur | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>AC-3-Audiodatei

Bei AC-3-Audiodaten lauten die Medientypen wie folgt.



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | Ausgabe von PES                           | Nutz Last Ausgabe               |
| Haupttyp       | MediaType \_ MPEG2 \_                | **MediaType \_ -Audiodatei**         |
| Subtype          | Mediasubtype \_ Dolby \_ AC3             | **Mediasubtype \_ Dolby \_ AC3** |
| Formattyp      | Formatieren von \_ WaveFormatEx                 | **Formatieren von \_ WaveFormatEx**     |
| Format Struktur | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

Das **wformattag** -Element der **WaveFormatEx** -Struktur für AC-3 ist zurzeit **\_ \_ unbekannt**. Dies kann sich jedoch ändern.

### <a name="mpeg-2-audio"></a>MPEG-2-Audiodatei

Bei MPEG-2-Audiodaten lauten die Medientypen wie folgt.



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | Ausgabe von PES                    | Nutz Last Ausgabe                 |
| Haupttyp       | **MediaType \_ MPEG2 \_**     | **MediaType \_ -Audiodatei**           |
| Subtype          | **Mediasubtye \_ \_ -Audiodatei** | **Mediasubtype \_ \_ -Audiodatei** |
| Formattyp      | **Formatieren von \_ WaveFormatEx**      | **Formatieren von \_ WaveFormatEx**       |
| Format Struktur | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

Das **wformattag** -Element der **WaveFormatEx** -Struktur für MPEG-2-Audiodaten ist zurzeit **\_ \_ unbekannt**, dies kann sich jedoch ändern.

Der MPEG-2-Splitter geht davon aus, dass Datenströme D0 bis DF für den Multichannel-Erweiterungs Datenstrom verwendet werden, wie Sie für die DVD MPEG-2-Audiodaten verwendet werden Daher leitet der Splitter, wenn Stream C *x* ausgewählt ist, auch die Pakete für Stream D *x* weiter.

### <a name="lpcm-audio"></a>LPCM-Audiodatei

Bei LPCM-Audiodaten lauten die Medientypen wie folgt.



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | Ausgabe von PES                         | Nutz Last Ausgabe                     |
| Haupttyp       | **MediaType \_ MPEG2 \_**          | **MediaType \_ -Audiodatei**               |
| Subtype          | **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei** | **mediasubtype \_ DVD \_ LPCM \_ -Audiodatei** |
| Formattyp      | **Formatieren von \_ WaveFormatEx**           | **Formatieren von \_ WaveFormatEx**           |
| Format Struktur | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Das **wformattag** -Element der **WaveFormatEx** -Struktur für LPCM-Audiodaten ist zurzeit **\_ \_ unbekannt**, dies kann sich jedoch ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Medientypen](mpeg-2-media-types.md)
</dt> </dl>

 

 
