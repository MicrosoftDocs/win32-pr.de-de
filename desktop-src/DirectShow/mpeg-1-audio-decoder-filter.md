---
description: MPEG-1-Audiodecoderfilter
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: MPEG-1-Audiodecoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3c014497d8b3db5aaf3031250e78edd8b59cb2
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983823"
---
# <a name="mpeg-1-audio-decoder-filter"></a>MPEG-1-Audiodecoderfilter

Decodiert MPEG-1 Layer I- und Layer II-Audio in PCM.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | 
| Eingabepin-Medientypen | MEDIATYPE_Audio, FORMAT_WaveFormatEx<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_MPEG1Packet</li><li>MEDIASUBTYPE_MPEG1Payload</li><li>MEDIASUBTYPE_MPEG1AudioPayload</li><li>GUID_NULL</li></ul> | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | MEDIATYPE_Audio, MEDIASUBTYPE_PCM | 
| Ausgabe-PIN-Schnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtern der CLSID | CLSID_CMpegAudioCodec | 
| Eigenschaftenseite CLSID | CLSID_MpegAudioDecoderPropertyPage | 
| Ausführbare Datei | quartz.dll | 
| <a href="merit.md">Verdienst</a> | 0x03680001 | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




