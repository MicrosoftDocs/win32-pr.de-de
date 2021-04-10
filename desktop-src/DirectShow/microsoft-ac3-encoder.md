---
description: Der Microsoft AC-3-Encoder-Filter codiert Stereo PCM-Audiodaten in einen Dolby Digital Bitstream.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Microsoft AC-3 Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124519"
---
# <a name="microsoft-ac-3-encoder"></a>Microsoft AC-3-Encoder

Der Microsoft AC-3-Encoder-Filter codiert Stereo PCM-Audiodaten in einen Dolby Digital Bitstream.

> [!Note]  
> Die Microsoft-Implementierung der Dolby Digital-Technologie ist gemäß den Bedingungen des Dolby Digital Licensing Program eingeschränkt, das von Microsoft-Anwendungen verwendet werden kann.

 

> [!Note]  
> Dieser Filter wird auf IA-64-basierten Plattformen nicht unterstützt.

 



Filter Informationen

Filter Schnittstellen

[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Eingabe-PIN-Medientypen

**MediaType \_ Audiodatei**, **mediasubtype \_ PCM**<br/> Der Eingabetyp muss 48-kHz-Stereo, 16 Bits pro Beispiel sein.<br/>

PIN-Eingabeschnittstellen

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Ausgabe-PIN-Medientypen

**MediaType \_ Audiodatei**, **mediasubtype \_ Dolby \_ AC3**<br/> **MediaType \_ Stream**, **mediasubtype \_ Dolby \_ AC3**<br/>

PIN-Schnittstellen

[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID Filtern

**CLSID \_ CMSAC3Enc** (in wmcodecdsp. h deklariert)

Ausführbare Datei

msac3enc.dll

[Verdienst](merit.md)

**das Verdienst wird \_ \_ nicht \_ verwendet.**

[Filter Kategorie](filter-categories.md)

**CLSID \_ legacyamfiltercategory**



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter ist nicht zur Verwendung durch Drittanbieter Anwendungen verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                                                                     |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




