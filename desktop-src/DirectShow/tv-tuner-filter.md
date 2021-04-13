---
description: TV-Tuner-Filter
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: TV-Tuner-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348558"
---
# <a name="tv-tuner-filter"></a>TV-Tuner-Filter

Der TV-Tuner-Filter wählt einen analogen Broadcast-oder Kabelkanal aus, der angezeigt werden soll. Der einzelne Ausgabestream ist ein Hardware Pfad für das analoge Baseband-Video. Diese Ausgabe sollte eine Verbindung mit dem analogen Video Querbalken Filter herstellen. Die Eingabe Pins enthalten eine Eingabe für Kabel-und Antennen Eingaben.



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**iamtvtuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **iksobject**, [**ikspropertyset**](ikspropertyset.md) |
| Eingabe-PIN-Medientypen                    | Nicht zutreffend                                                                                                                                                                   |
| PIN-Eingabeschnittstellen                     | Nicht zutreffend                                                                                                                                                                   |
| Ausgabe-PIN-Medientypen                   | Video: MediaType \_ Analog gvideo, ksdataformat \_ -Untertyp \_ keine Audiodatei: MediaType \_ Analog gaudiodatei, mediasubtype \_ null                                                                      |
| PIN-Schnittstellen                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| CLSID Filtern                             | CLSID- \_ tvtunerfilter                                                                                                                                                              |
| CLSID der Eigenschaften Seite                      | CLSID \_ tvtunerfilterpropertypage                                                                                                                                                  |
| Ausführbare Datei                               | KSTVTune.ax                                                                                                                                                                       |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                                               |
| [Filter Kategorie](filter-categories.md) | AM \_ kscategory- \_ TvTuner                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



