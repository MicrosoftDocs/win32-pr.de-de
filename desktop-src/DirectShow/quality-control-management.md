---
description: Quality-Control Verwaltung
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343542"
---
# <a name="quality-control-management"></a>Quality-Control Verwaltung

Bei der Qualitätskontrolle handelt es sich um einen Mechanismus, mit dem die Geschwindigkeit des Datenflusses über das Filter Diagramm als Reaktion auf die Laufzeitleistung angepasst wird. Wenn ein rendererfilter zu viele oder zu wenige Daten empfängt, kann er eine *Qualitäts Nachricht* senden. Die Qualitäts Meldung fordert eine Anpassung in der Datenrate an. Standardmäßig werden qualitativ hochwertige Nachrichten vom Renderer hoch bewegt, bis Sie einen Filter erreichen, der (sofern vorhanden) Antworten kann. Eine Anwendung kann auch einen benutzerdefinierten Quality Manager implementieren. In diesem Fall übergibt der Renderer Qualitäts Meldungen direkt an den Quality Manager der Anwendung.

Dieser Artikel enthält die folgenden Themen:

-   [Qualitäts Meldungen](quality-messages.md)
-   [Standardmäßige Qualitätskontrolle](default-quality-control.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



