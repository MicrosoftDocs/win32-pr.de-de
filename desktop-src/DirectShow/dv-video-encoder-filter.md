---
description: DV-Videoencoderfilter
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: DV-Videoencoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14928c937313d056549a348bd255f251354c0ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482636"
---
# <a name="dv-video-encoder-filter"></a>DV-Videoencoderfilter

Dieser Filter codiert einen nicht komprimierten Videodatenstrom in digitale Videos (DV). Sie stellt eine benutzerdefinierte Schnittstelle [**(IDVEnc)**](/windows/desktop/api/Strmif/nn-strmif-idvenc)zum Festlegen der Codierungsauflösung und des Formats bereit.




| | | Filterschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong> | | Eingabepinmedientypen | <ul><li>Haupttyp: MEDIATYPE_VideoThe folgenden Untertypen sind gültig:<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Formattyp: FORMAT_VideoInfo</li></ul> | | Eingabepinschnittstellen | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Ausgabepinmedientypen | <ul><li>Haupttyp: MEDIATYPE_Video</li><li>Untertyp: MEDIASUBTYPE_dvsd</li><li>Formattyp: FORMAT_VideoInfo</li></ul> | | Ausgabepinschnittstellen | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtern von CLSID-| CLSID_DVVideoEnc | | CLSID-| der Eigenschaftenseite CLSID_DVEncPropertiesPage | | Ausführbare | qdv.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">| "Filterkategorie"</a> CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Hinweise

Für 16-Bit-Videos (MEDIASUBTYPE \_ RGB555 oder MEDIASUBTYPE \_ RGB565) muss die Eingabe 720 x 480 Pixel für NTSC oder 720 x 576 Pixel für PAL betragen. Für 24-Bit-Videos gelten keine Größeneinschränkungen für die Eingabe.

Die Ausgabe ist immer 720 x 480 für NTSC oder 720 x 576 für PAL. 24-Bit-Video wird so skaliert, dass es diesen Dimensionen entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




