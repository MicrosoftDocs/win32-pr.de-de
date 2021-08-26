---
description: Die Zeitachse
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Die Zeitachse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f298c2649a280bf5fd622d5fb5a2aef820d1f340d45f7e2beb83fe9edd6a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050000"
---
# <a name="the-timeline"></a>Die Zeitachse

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Die Zeitachse macht die [**IAMTimeline-Schnittstelle**](iamtimeline.md) verfügbar. Diese Schnittstelle enthält Methoden zum Festlegen von Eigenschaften auf der Zeitachse. zum Hinzufügen von Gruppen zur Zeitachse und zum Erstellen von Zeitachsenobjekten wie Gruppen, Spuren und Quellen. Um eine neue Zeitachse zu erstellen, rufen Sie die **CoCreateInstance-Standardfunktion** wie folgt auf:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



Die neue Zeitachse ist leer. An diesem Punkt können Sie entweder eine vorhandene Projektdatei laden (siehe [Laden und Vorschau einer Project](loading-and-previewing-a-project.md)) oder die Zeitachse erstellen, indem Sie neue Objekte erstellen und einfügen (siehe Erstellen einer [Zeitachse](constructing-a-timeline.md)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Zeitachsenkomponenten](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



