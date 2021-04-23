---
description: TV-Tunerfilter
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: TV-Tunerfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909028"
---
# <a name="tv-tuner-filter"></a>TV-Tunerfilter

Der Filter TV Tuner wählt einen analogen Broadcast- oder Kabelkanal aus, der angezeigt werden soll. Der einzelne Ausgabestream ist ein Hardwarepfad für analoge Basebandvideos. Diese Ausgabe sollte eine Verbindung mit dem Analog Video Crossbar-Filter herstellen. Die Eingabepins enthalten eine Eingabe für Kabel und eine Antenne.



| Bezeichnung | Wert |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMTVTuner,**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) **ISpecifyPropertyPages,** **IPersistPropertyBag,** **IKsObject,** [**IKsPropertySet**](ikspropertyset.md) |
| Eingabe-Stecknadelmedientypen                    | Nicht zutreffend                                                                                                                                                                   |
| Eingabe-Pin-Schnittstellen                     | Nicht zutreffend                                                                                                                                                                   |
| Medientypen des Ausgabepins                   | Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                      |
| Ausgabe-Pin-Schnittstellen                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| Filtern von CLSID                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| CLSID der Eigenschaftenseite                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| Ausführbare Datei                               | KSTVTune.ax                                                                                                                                                                       |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                               |
| [Filterkategorie](filter-categories.md) | AM \_ KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



