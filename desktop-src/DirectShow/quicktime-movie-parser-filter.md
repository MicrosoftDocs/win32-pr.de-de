---
description: QuickTime Movie Parser-Filter
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: QuickTime Movie Parser-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a65ba14cb748eb10c6afddf3e4747f11d68a4f9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476716"
---
# <a name="quicktime-movie-parser-filter"></a>QuickTime Movie Parser-Filter

Diese Komponente wurde aus den Betriebssystemen Windows Vista und höher entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

Der Filter QuickTime Movie Parser teilt Apple® QuickTime®daten in Audio- und Videostreams auf. QuickTime 2.0 und früher wird unterstützt. Der Eingabepin stellt eine Verbindung mit einem Quellfilter wie dem [Filter Async File Source](file-source--async--filter.md) oder dem Filter URL File Source [(URL-Dateiquelle)](file-source--url--filter.md) herstellt. Der Parser verwendet den [AVI-Dekomprimierungsfilter](avi-decompressor-filter.md) oder [QT-Dekomprimierungsfilter,](qt-decompressor-filter.md) um QuickTime-Dateien zu dekomprimieren. Der Filter erstellt einen Ausgabepin für den Videostream und einen Ausgabepin für den Audiostream.




| | | Filtern von Schnittstellen | <a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter | |</strong></a> Eingabepin-Medientypen | MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie; | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepin-Medientypen | <ul><li>MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</li><li>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</li></ul> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Filtern von CLSID-| CLSID_QuickTimeParser | | CLSID-Eigenschaftsseite | Keine Eigenschaftenseite. | | Ausführbare | quartz.dll | | <a href="merit.md">Leistungs-|</a> MERIT_NORMAL | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



