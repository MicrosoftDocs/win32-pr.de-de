---
description: Audioerfassungs Filter
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Audioerfassungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73da50653a4a159d30a6ca1b83ebc1f37a6de42c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747257"
---
# <a name="audio-capture-filter"></a>Audioerfassungs Filter

Der audioerfassungs Filter stellt ein audioerfassungs-Gerät dar. Sie verfügt über eine Ausgabe-PIN und mehrere Eingabe Pins (eine für jeden Typ der Eingabe auf der Karte, z. b. Line in, MIC, CD und MIDI).

Dieser Filter kann mit mehreren Hardware Geräten verwendet werden, sodass das Aufrufen von CoCreateInstance zum Erstellen des Filters nicht funktioniert. Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md)". Der Enumerator für System Geräte gibt einen eindeutigen Moniker für jedes Gerät zurück. Der Anzeige Name des Monikers entspricht dem Namen des Geräts. (Dies ist der Name, der in GraphEdit angezeigt wird.) Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).



|                                          |                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**iamfilterfehlflags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**iamresourcecontrol**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Eingabe-PIN-Medientypen                    | MediaType \_ Analog gaudiodatei, mediasubtype \_ null                                                                                                                                                                                                                                                         |
| PIN-Eingabeschnittstellen                     | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Ausgabe-PIN-Medientypen                   | MediaType \_ -Audiodatei, mediasubtype \_ null                                                                                                                                                                                                                                                               |
| PIN-Schnittstellen                    | [**Iambufferaushandlung**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**iampushsource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**ikspropertyset**](ikspropertyset.md), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | Nicht verfügbar                                                                                                                                                                                                                                                                                     |
| CLSID der Eigenschaften Seite                      | CLSID \_ audioinputmixerproperties                                                                                                                                                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                                                                                                                                                                |
| [Filter Kategorie](filter-categories.md) | CLSID \_ audioinputentvicecategory                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Die Eingabe Pins stellen physische Hardware Verbindungen dar und sind nie mit anderen Filtern in DirectShow verbunden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Audioerfassung](audio-capture.md)
</dt> </dl>

 

 



