---
description: Der FILTERS-Rendererfilter rendert DIE DATEN aus dem FILTERS Parser-Filter.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: RENDERerfilter FÜR DEN RENDERER (Windows.devices.xp.h)
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
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909408"
---
# <a name="midi-renderer-filter"></a>FILTERS-Rendererfilter

Der FILTERS-Rendererfilter rendert DIE DATEN aus dem [FILTERS Parser-Filter.](midi-parser-filter.md)



| Bezeichnung | Wert |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IAMClockSlave,**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave) [**IAMDirectSound,**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IBasicAudio,**](/windows/desktop/api/Control/nn-control-ibasicaudio) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Eingabe-Stecknadelmedientypen                    | \_MEDIATYPE- Und MEDIASUBTYPE \_ NULL-Werte                                                                                                                                                                                                                                                                                                                                                  |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Medientypen des Ausgabepins                   | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                       |
| Ausgabe-Pin-Schnittstellen                    | Nicht zutreffend                                                                                                                                                                                                                                                                                                                                                                       |
| Filtern von CLSID                             | CLSID \_ AVIMIDIRender                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                                                                                                                                                                                                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | \_VORGEZOGENE VORZEICHEN                                                                                                                                                                                                                                                                                                                                                                     |
| [Filterkategorie](filter-categories.md) | CLSID- \_ Und -Vererbungskategorie                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für den Formattyp ist **NULL,** aber der Formatblock enthält die folgende Struktur:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



Das **dwDivision-Element** gibt die Zeitdivision der Datei an. Die Zeitdivision wird im Header einer beliebigen STANDARD-FORMAT-Datei (SMF) im `MThd` Block angegeben. Der RENDERING-Renderer legt diese Eigenschaft für denDATENÜBERTRAGUNG-Datenstrom fest, indem er die **funktion "streamsStreamProperty"** aufruft.

Beispiele aus dem FILTER DES PARSER-Parsers enthalten eine Sekunde vonTEN-Daten. Der RENDERING-Renderer verwendet die **funktion "streamStreamOut",** um die DANN-Daten zu rendern. Jedes Beispiel ist ein Synchronisierungspunkt: Der Anfang des Puffers enthält alle Befehle, die zum Festlegen des richtigen Zustands für das Rendern dieses Puffers erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows.devices.format.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




