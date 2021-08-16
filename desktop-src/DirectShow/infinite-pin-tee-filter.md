---
description: Filter für unendliche Pin-Tees
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filter für unendliche Pin-Tees
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28edb67da9d6aae01786cece43b45dfcd33d571b82bdbab21ecf82a2473ff0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818785"
---
# <a name="infinite-pin-tee-filter"></a>Filter für unendliche Pin-Tees

Dieser Filter liefert Beispiele, die an den Eingabepin übermittelt werden, an eine variable Anzahl von Ausgabepins. Wenn eine Instanz des Filters erstellt wird, verfügt sie über einen Ausgabepin. Jedes Mal, wenn ein Ausgabepin verbunden wird, erstellt der Filter einen weiteren Ausgabepin. Alle Ausgabepins haben denselben Medientyp wie der Eingabepin.

Eine Version dieses Filters wird auch als SDK-Beispiel bereitgestellt. Weitere Informationen finden Sie [unter InfTee-Filterbeispiel.](inftee-filter-sample.md)



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabepinmedientypen                    | Beliebiger Medientyp                                                                                                                                     |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Medientypen des Ausgabepins                   | Ein beliebiger Medientyp. Der Ausgabetyp stimmt für alle Ausgabepins immer mit dem Eingabetyp überein.                                                                 |
| Ausgabe-Pin-Schnittstellen                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern von CLSID                             | CLSID \_ InfTee                                                                                                                                      |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                           |
| [Verdienst](merit.md)                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



