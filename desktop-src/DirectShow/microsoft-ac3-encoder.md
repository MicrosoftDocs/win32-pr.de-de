---
description: Der Microsoft AC-3-Encoderfilter codiert Stereo-PCM-Audio in einen Dolby Digital-Bitstream.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Microsoft AC-3 Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35984975fc5a56b043f1b2ceda56505ee6fe74038034fb35deb09b6a5f6a0f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153168"
---
# <a name="microsoft-ac-3-encoder"></a>Microsoft AC-3-Encoder

Der Microsoft AC-3-Encoderfilter codiert Stereo-PCM-Audio in einen Dolby Digital-Bitstream.

> [!Note]  
> Die Microsoft-Implementierung der Dolby Digital-Technologie ist im Rahmen des Dolby Digital-Lizenzierungsprogramms auf die Verwendung durch Microsoft-Anwendungen beschränkt.

 

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filterinformationen

Filterschnittstellen

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Eingabepinmedientypen

**MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ PCM**<br/> Der Eingabetyp muss stereo mit 48 kHz und 16 Bits pro Stichprobe sein.<br/>

Eingabe-Pin-Schnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Medientypen des Ausgabepins

**MEDIATYPE \_ Audio,** **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/> **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/>

Ausgabe-Pin-Schnittstellen

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtern von CLSID

**CLSID \_ CMSAC3Enc** (deklariert in wmcodecdsp.h)

Ausführbare Datei

msac3enc.dll

[Verdienst](merit.md)

**NOT USE (NICHT \_ \_ \_ VERWENDEN)**

[Filterkategorie](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Hinweise

Dieser Filter ist nicht für die Verwendung durch Drittanbieteranwendungen verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, nur Windows 7 \[ Ultimate-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




