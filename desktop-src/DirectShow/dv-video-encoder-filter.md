---
description: DV-Videoencoderfilter
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: DV-Videoencoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c89574ab257467e16b566fe899a5ab32384e48e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986793"
---
# <a name="dv-video-encoder-filter"></a>DV-Videoencoderfilter

Dieser Filter codiert einen unkomprimierten Videostream in digitales Video (DV). Es stellt eine benutzerdefinierte Schnittstelle, [**IDVEnc,**](/windows/desktop/api/Strmif/nn-strmif-idvenc)zum Festlegen der Codierungsauflösung und des Formats bereit.




| Bezeichnung | Wert |
|--------|-------|
| Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong> | 
| Eingabepin-Medientypen | <ul><li>Haupttyp: MEDIATYPE_VideoThe folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Formattyp: FORMAT_VideoInfo</li></ul> | 
| Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Ausgabepin-Medientypen | <ul><li>Haupttyp: MEDIATYPE_Video</li><li>Untertyp: MEDIASUBTYPE_dvsd</li><li>Formattyp: FORMAT_VideoInfo</li></ul> | 
| Ausgabe-PIN-Schnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtern der CLSID | CLSID_DVVideoEnc | 
| Eigenschaftenseite CLSID | CLSID_DVEncPropertiesPage | 
| Ausführbare Datei | qdv.dll | 
| <a href="merit.md">Verdienst</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Filterkategorie</a> | CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Bemerkungen

Für 16-Bit-Videos (MEDIASUBTYPE \_ RGB555 oder MEDIASUBTYPE RGB565) muss die Eingabe \_ 720 x 480 Pixel für NTSC oder 720 x 576 Pixel für PAL betragen. Für 24-Bit-Videos gibt es keine Größeneinschränkungen für die Eingabe.

Die Ausgabe beträgt immer 720 x 480 für NTSC oder 720 x 576 für PAL. 24-Bit-Video wird skaliert, um diese Dimensionen zu erreichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




