---
description: Der FILTERS Renderer-Filter rendert DIE DATEN aus dem FILTERS Parser-Filter.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: RENDERerfilter FÜR DEN RENDERER (Windows.devices.hf.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 3727fb322e03338723eb3c9da1ac86d4e6a7145424cb04b0c050b67f83aa141a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791450"
---
# <a name="midi-renderer-filter"></a>FILTERS-Rendererfilter

Der FILTERS-Rendererfilter rendert DIE DATEN aus dem [FILTERS Parser-Filter.](midi-parser-filter.md)



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMClockSlave,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirectSound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicAudio,**](/windows/desktop/api/Control/nn-control-ibasicaudio) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Eingabepinmedientypen                    | \_MEDIATYPE- Und MEDIASUBTYPE \_ NULL-Werte                                                                                                                                                                                                                                                                                                                                                  |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Medientypen des Ausgabepins                   | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                       |
| Ausgabe-Pin-Schnittstellen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                       |
| Filtern von CLSID                             | CLSID \_ AVIMIDIRender                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                                                                                                                                                                                                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | \_VORGEZOGENE VORZEICHEN                                                                                                                                                                                                                                                                                                                                                                     |
| [Filterkategorie](filter-categories.md) | CLSID- \_ Oder-ID-Datei "Category"                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Die GUID für den Formattyp ist **NULL,** aber der Formatblock enthält die folgende Struktur:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



Der **dwDivision-Member** gibt die Zeitaufteilung der Datei an. Die Zeitdivision wird im Header einer beliebigen STANDARDMÄßIGEN CSV-Datei (SMF) im `MThd` Block angegeben. Der RENDERING Renderer legt diese Eigenschaft für den DATENQUELLEN-Datenstrom fest, indem er die **funktion "streamsStreamProperty"** aufruft.

Beispiele aus dem FILTER "PARSER" enthalten eine Sekunde der DATENQUELLEN-Daten. Der RENDERINGer verwendet die **funktion "streamingStreamOut",** um dieDATENÜBERTRAGUNG-Daten zu rendern. Jedes Beispiel ist ein Synchronisierungspunkt: Der Anfang des Puffers enthält alle Befehle, die erforderlich sind, um den richtigen Zustand für das Rendern dieses Puffers festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows.devices.hv.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




