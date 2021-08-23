---
description: TV Tuner Filter
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: TV Tuner Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101dfcce4877570a2072d9e4c116466223e56889fb5e66de3e6ef0ec24afad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015518"
---
# <a name="tv-tuner-filter"></a>TV Tuner Filter

Der Tv-Tuner-Filter wählt einen analogen Broadcast- oder Kabelkanal aus, der angezeigt werden soll. Der einzelne Ausgabestream ist ein Hardwarepfad für analoges Basebandvideo. Diese Ausgabe sollte eine Verbindung mit dem Analog Video Crossbar-Filter herstellen. Die Eingabepins enthalten eine Eingabe für Kabel und eine Antenne.



| Bezeichnung | Wert |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md) |
| Eingabepin-Medientypen                    | Nicht zutreffend                                                                                                                                                                   |
| Eingabepinschnittstellen                     | Nicht zutreffend                                                                                                                                                                   |
| Ausgabepin-Medientypen                   | Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                      |
| Ausgabe-PIN-Schnittstellen                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| Filtern der CLSID                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| Eigenschaftenseite CLSID                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| Ausführbare Datei                               | KSTVTune.ax                                                                                                                                                                       |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                                               |
| [Filterkategorie](filter-categories.md) | AM \_ KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



