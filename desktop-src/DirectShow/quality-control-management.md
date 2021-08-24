---
description: Quality-Control-Verwaltung
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control-Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824410b697a29ee73fc269748595fdcae91d054a161561b282536a05dcf92ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747710"
---
# <a name="quality-control-management"></a>Quality-Control-Verwaltung

Die Qualitätssteuerung ist ein Mechanismus zum Anpassen der Rate des Datenflusses durch das Filterdiagramm als Reaktion auf die Laufzeitleistung. Wenn ein Rendererfilter zu viele oder zu wenig Daten empfängt, kann er eine *Qualitätsmeldung* senden. Die Qualitätsmeldung fordert eine Anpassung der Datenrate an. Standardmäßig werden Qualitätsnachrichten vom Renderer vorgelagert, bis sie einen Filter erreichen, der (falls vorhanden) antworten kann. Eine Anwendung kann auch einen benutzerdefinierten Qualitäts-Manager implementieren. In diesem Fall übergibt der Renderer Qualitätsmeldungen direkt an den Qualitäts-Manager der Anwendung.

Dieser Artikel enthält die folgenden Themen.

-   [Qualitätsmeldungen](quality-messages.md)
-   [Standardqualitätskontrolle](default-quality-control.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Daten Flow für Filterentwickler](data-flow-for-filter-developers.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



