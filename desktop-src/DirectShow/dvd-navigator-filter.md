---
description: DVD Navigator-Filter
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: DVD Navigator-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d248e490201536e92afeb38f520028e29ea9a5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477297"
---
# <a name="dvd-navigator-filter"></a>DVD Navigator-Filter

Der FILTER DVD Navigator ist der Quellfilter für ein DVD-Video Wiedergabefilterdiagramm. Es öffnet alle erforderlichen Dateien in einem DVD-Video-Volume, navigiert durch die linearen DVD-Video.vob-Dateien, analysiert den resultierenden MPEG-2-Programmstream und teilt den Stream in drei Ausgabepins (Video, Audio, Unterbild) auf.

Der FILTER DVD Navigator implementiert auch die [**Schnittstellen IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) und [**IDvdInfo2,**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) die es einer DVD-Wiedergabeanwendung ermöglichen, die Wiedergabe DVD-Video steuern.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Eingabepin-Medientypen | MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM | | Eingabepinschnittstellen | Nicht zutreffend. | | Ausgabepin-Medientypen | Basistypen:<br /><ul><li>Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li>Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li>Unterbild: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Erweiterte Typen:<br /> Video:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li></ul>Audio:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li></ul>Subpicture:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Um die erweiterten Typen zu aktivieren, rufen Sie <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>IDvdControl2::SetOption</strong></a> auf, und legen Sie fest. <br /> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl | |</strong></a> Filtern von CLSID-| CLSID_DVDNavigator | | CLSID-Eigenschaftsseite | Keine Eigenschaftenseite. | | Ausführbare | qdvd.dll | | <a href="merit.md">Leistungs-|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filterkategorie-|</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 




