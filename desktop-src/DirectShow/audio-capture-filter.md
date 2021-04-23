---
description: Audioaufnahmefilter
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Audioaufnahmefilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a630452565fafad3c4a4420154efd8fe6b282f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910208"
---
# <a name="audio-capture-filter"></a>Audioaufnahmefilter

Der Filter Audioaufnahme stellt ein Audioaufnahmegerät dar. Es verfügt über einen Erfassungsausgabepin und mehrere Eingabepins (einen für jeden Eingabetyp auf der Karte, z. B. Einfüge-, Mikrofon-, CD- und VBIs).

Dieser Filter kann mit mehreren Hardwaregeräten verwendet werden, sodass der Aufruf von CoCreateInstance zum Erstellen des Filters nicht funktioniert. Verwenden Sie stattdessen den [Systemgeräte-Enumerator](system-device-enumerator.md). Der Systemgeräte-Enumerator gibt einen eindeutigen Moniker für jedes Gerät zurück. Der Anzeigename des Monikers entspricht dem Namen des Geräts. (Dies ist der Name, der in GraphEdit angezeigt wird.) Weitere Informationen finden Sie unter [Aufzählen von Geräten und Filtern.](enumerating-devices-and-filters.md)



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMAudioInputMixer,**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Eingabe-Stecknadelmedientypen                    | MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                         |
| Eingabe-Pin-Schnittstellen                     | [**IAMAudioInputMixer,**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Medientypen des Ausgabepins                   | MEDIATYPE \_ Audio, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                               |
| Ausgabe-Pin-Schnittstellen                    | [**IAMBufferNegotiation,**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) [**IAMPushSource,**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IKsPropertySet,**](ikspropertyset.md) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | Nicht zutreffend                                                                                                                                                                                                                                                                                     |
| Eigenschaftenseite CLSID                      | CLSID \_ AudioInputMixerProperties                                                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ AudioInputDeviceCategory                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Die Eingabepins stellen physische Hardwareverbindungen dar und sind nie mit anderen Filtern in DirectShow verbunden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Audioaufnahme](audio-capture.md)
</dt> </dl>

 

 



