---
description: Filter für unendliche Pin-Tees
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filter für unendliche Pin-Tees
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909228"
---
# <a name="infinite-pin-tee-filter"></a>Filter für unendliche Pin-Tees

Dieser Filter liefert Beispiele, die an den Eingabepin übermittelt werden, an eine variable Anzahl von Ausgabepins. Wenn eine Instanz des Filters erstellt wird, verfügt sie über einen Ausgabepin. Jedes Mal, wenn ein Ausgabepin verbunden wird, erstellt der Filter einen weiteren Ausgabepin. Alle Ausgabepins haben denselben Medientyp wie der Eingabepin.

Eine Version dieses Filters wird auch als SDK-Beispiel bereitgestellt. Weitere Informationen finden Sie [unter InfTee-Filterbeispiel.](inftee-filter-sample.md)



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabe-Stecknadelmedientypen                    | Beliebiger Medientyp                                                                                                                                     |
| Eingabe-Pin-Schnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Medientypen des Ausgabepins                   | Ein beliebiger Medientyp. Der Ausgabetyp stimmt für alle Ausgabepins immer mit dem Eingabetyp überein.                                                                 |
| Ausgabe-Pin-Schnittstellen                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern der CLSID                             | CLSID \_ InfTee                                                                                                                                      |
| Eigenschaftenseite CLSID                      | Keine Eigenschaftenseite                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                           |
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



