---
description: MPEG-2-Splitter
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2-Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417fcca0bfc7a5c24416cfc2cb915f968c12105d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465255"
---
# <a name="mpeg-2-splitter"></a>MPEG-2-Splitter

Ab Microsoft® Windows® XP ist der MPEG-2-Splitterfilter veraltet. Verwenden Sie stattdessen [mpeg-2 Demultiplexer.](mpeg-2-demultiplexer.md)

Verwenden Sie auf früheren Plattformen den MPEG-2-Splitter für MPEG-2-Programmstreams, die im Pullmodus bereitgestellt werden und mindestens einen der folgenden Streamtypen enthalten: MPEG-2-Video; MPEG-2-Audio; AC3-audiocodiert wie für DVD-Video definiert; oder PCM-Audio, das gemäß definition für DVD-Video codiert ist. Dieser Filter analysiert die Streams, erstellt einen Ausgabepin für jeden Stream und gibt die komprimierten MPEG-Audio- oder Videopakete an einen MPEG-2-Decoderfilter aus.

Verwenden Sie für Programm- und Transportstreams, die im Pushmodus bereitgestellt werden, den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md)auf allen Plattformen.

> [!Note]  
> Der MPEG-2-Splitter unterstützt keine framegenaue Suche.

 




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <strong>ISpecifyPropertyPages,</strong> <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | | Eingabepinmedientypen | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepinmedientypen | Hängt vom Streamtyp ab. Weitere Informationen finden Sie unter <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | | Filtern von CLSID-| CLSID_MMSPLITTER | | CLSID-| der Eigenschaftenseite Nicht zutreffend | | Ausführbare | mpg2splt.ax | | <a href="merit.md">|</a> MERIT_NORMAL + 1 | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Verwenden des MPEG-2-Splitters](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



