---
description: Filter für unendliche Pin-Tee
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filter für unendliche Pin-Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392738"
---
# <a name="infinite-pin-tee-filter"></a>Filter für unendliche Pin-Tee

Dieser Filter liefert der Eingabe-PIN übergebene Beispiele an eine Variable Anzahl von Ausgabe Pins. Wenn eine Instanz des Filters erstellt wird, verfügt sie über eine Ausgabe-PIN. Jedes Mal, wenn eine Ausgabepin verbunden ist, erstellt der Filter eine weitere Ausgabepin. Alle Ausgabe Pins haben denselben Medientyp wie die Eingabe-PIN.

Eine Version dieses Filters wird auch als SDK-Beispiel bereitgestellt. Siehe [Info Filter Sample](inftee-filter-sample.md).



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Eingabe-PIN-Medientypen                    | Beliebige Medientyp                                                                                                                                     |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabe-PIN-Medientypen                   | Ein beliebiger Medientyp. Der Ausgabetyp stimmt immer mit dem Eingabetyp für alle Ausgabe Pins überein.                                                                 |
| PIN-Schnittstellen                    | [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID \_ -Empfänger                                                                                                                                      |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite                                                                                                                                   |
| Ausführbare Datei                               | qcap.dll                                                                                                                                           |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



