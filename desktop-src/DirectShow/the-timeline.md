---
description: Die Zeitachse
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Die Zeitachse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351153"
---
# <a name="the-timeline"></a>Die Zeitachse

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Die Zeitachse macht die [**iamtimeline**](iamtimeline.md) -Schnittstelle verfügbar. Diese Schnittstelle enthält Methoden zum Festlegen von Eigenschaften auf der Zeitachse. zum Hinzufügen von Gruppen zur Zeitachse; und zum Erstellen von Zeitachsen Objekten, wie z. b. Gruppen, Spuren und Quellen. Um eine neue Zeitachse zu erstellen, rufen Sie die standardmäßige **cokreateinstance** -Funktion wie folgt auf:


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



Die neue Zeitachse ist leer. An diesem Punkt können Sie entweder eine vorhandene Projektdatei laden (siehe [Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md)) oder die Zeitachse erstellen, indem Sie neue Objekte erstellen und Einfügen (siehe [Erstellen einer Zeitachse](constructing-a-timeline.md)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Zeitachsen Komponenten](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



