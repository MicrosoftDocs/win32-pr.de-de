---
description: MPEG-2-Splitter
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: MPEG-2-Splitter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df24cb6542c335253c9f78051805b5810b5df67
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988323"
---
# <a name="mpeg-2-splitter"></a>MPEG-2-Splitter

Ab Microsoft® Windows® XP ist der MPEG-2-Splitterfilter veraltet. Verwenden Sie stattdessen [mpeg-2 Demultiplexer.](mpeg-2-demultiplexer.md)

Verwenden Sie auf früheren Plattformen den MPEG-2-Splitter für MPEG-2-Programmstreams, die im Pullmodus bereitgestellt werden und mindestens einen der folgenden Streamtypen enthalten: MPEG-2-Video; MPEG-2-Audio; AC3-audiocodiert wie für DVD-Video definiert; oder PCM-Audio, das gemäß definition für DVD-Video codiert ist. Dieser Filter analysiert die Streams, erstellt einen Ausgabepin für jeden Stream und gibt die komprimierten MPEG-Audio- oder Videopakete an einen MPEG-2-Decoderfilter aus.

Verwenden Sie für Programm- und Transportstreams, die im Pushmodus bereitgestellt werden, den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md)auf allen Plattformen.

> [!Note]  
> Der MPEG-2-Splitter unterstützt keine framegenaue Suche.

 




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | 
| Eingabepinmedientypen | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | 
| Eingabe-Pin-Schnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Medientypen des Ausgabepins | Hängt vom Streamtyp ab. Weitere Informationen finden Sie unter <a href="mpeg-2-splitter-media-types.md">MPEG-2-Splittermedientypen.</a> | 
| Ausgabe-Pin-Schnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| Filtern von CLSID | CLSID_MMSPLITTER | 
| CLSID der Eigenschaftenseite | Nicht zutreffend | 
| Ausführbare Datei | mpg2splt.ax | 
| <a href="merit.md">Verdienst</a> | MERIT_NORMAL + 1 | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Verwenden des MPEG-2-Splitters](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



