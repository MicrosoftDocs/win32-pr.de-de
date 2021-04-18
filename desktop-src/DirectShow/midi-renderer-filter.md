---
description: Der-rendererfilterfilter rendert die Daten vom Typ "MIDI" aus dem-
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: MIDI-rendererfilter (Windows. Devices. MIDI. h)
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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371480"
---
# <a name="midi-renderer-filter"></a>MIDI-rendererfilter

Der-rendererfilterfilter rendert die Daten vom Typ "MIDI" [aus dem-](midi-parser-filter.md)



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Iamclockslave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**iamdirectsound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**iamresourcecontrol**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ibasicaudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Eingabe-PIN-Medientypen                    | MediaType \_ MIDI, mediasubtype \_ null                                                                                                                                                                                                                                                                                                                                                  |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Ausgabe-PIN-Medientypen                   | Nicht verfügbar                                                                                                                                                                                                                                                                                                                                                                       |
| PIN-Schnittstellen                    | Nicht verfügbar                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID Filtern                             | CLSID \_ avimidirendering                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                                                                                                                                                                                                                                                                     |
| Ausführbare Datei                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Verdienst](merit.md)                       | \_bevorzugter Vorteil                                                                                                                                                                                                                                                                                                                                                                     |
| [Filter Kategorie](filter-categories.md) | CLSID \_ midirenderercategory                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für den Formattyp ist **null**, aber der Format Block enthält die folgende Struktur:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



Der **dwdivision** -Member gibt die Zeiteinteilung der Datei an. Die Zeiteinteilung wird in der Kopfzeile einer beliebigen Standard-MIDI-Datei (SMF) im Block angegeben `MThd` . Der MIDI-Renderer legt diese Eigenschaft für den Datenstrom von MIDI fest, indem er die **midistreamproperty** -Funktion aufruft.

Die Beispiele aus dem Code des MIDI-Parsers enthalten eine Sekunde der Daten von MIDI. Der MIDI-Renderer verwendet die **midistreamout** -Funktion, um die Daten des Datenstroms zu Rendering Jedes Beispiel ist ein Synchronisierungs Punkt: der Anfang des Puffers enthält alle Befehle, die erforderlich sind, um den korrekten Zustand für das Rendern dieses Puffers festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Windows. Devices. MIDI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 




