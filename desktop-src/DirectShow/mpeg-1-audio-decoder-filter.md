---
description: MPEG-1-Audiodecoderfilter
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: MPEG-1-Audiodecoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa6e72d52d7dc25abd137f98a83b8ffce4359c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471256"
---
# <a name="mpeg-1-audio-decoder-filter"></a>MPEG-1-Audiodecoderfilter

Decodiert MPEG-1 Layer I- und Layer II-Audio in PCM.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Eingabepinmedientypen | MEDIATYPE_Audio, FORMAT_WaveFormatEx<br /> Die folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_MPEG1Packet</li><li>MEDIASUBTYPE_MPEG1Payload</li><li>MEDIASUBTYPE_MPEG1AudioPayload</li><li>GUID_NULL</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepinmedientypen | MEDIATYPE_Audio, MEDIASUBTYPE_PCM | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtern von CLSID-| CLSID_CMpegAudioCodec | | CLSID-| der Eigenschaftenseite CLSID_MpegAudioDecoderPropertyPage | | Ausführbare | quartz.dll | | <a href="merit.md">|</a> 0x03680001 | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




