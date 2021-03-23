---
title: Verwenden von deskriptortabellen
description: Deskriptortabellen, von denen jedes einen Bereich in einem deskriptorheap identifiziert, werden an Slots gebunden, die durch die aktuelle Stamm Signatur in einer Befehlsliste definiert sind.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104230"
---
# <a name="using-descriptor-tables"></a>Verwenden von deskriptortabellen

Deskriptortabellen, von denen jedes einen Bereich in einem deskriptorheap identifiziert, werden an Slots gebunden, die durch die aktuelle Stamm Signatur in einer Befehlsliste definiert sind.

-   [Indizieren von deskriptortabellen](#indexing-descriptor-tables)
-   [Verwandte Themen](#related-topics)

Shader können Ressourcen suchen, auf die von den Deskriptoren verwiesen wird, aus denen die Deskriptortabelle besteht. Andere Ressourcen Bindungen: Index Puffer, Vertex-Puffer, streamausgabepuffer, Renderziele und tiefen Schablone werden direkt in einer Befehlsliste und nicht über Deskriptoren ausgeführt. Zusammenfassung:

Die folgenden Ressourcen Verweise können dieselbe Deskriptortabelle und denselben Heap aufweisen:

-   Shaderressourcenansichten
-   Ungeordnete Zugriffs Sichten
-   Konstantenpuffersichten

Die folgenden Ressourcen Verweise müssen sich in einem eigenen deskriptorheap befinden:

-   Sampler

Die folgenden Ressourcen werden nicht in deskriptortabellen oder Heaps abgelegt, sondern direkt mithilfe von Befehlslisten gebunden:

-   Indexpuffer
-   Vertex-Puffer
-   Stream-Ausgabepuffer
-   Renderziele
-   Ansicht der tiefen Schablone

## <a name="indexing-descriptor-tables"></a>Indizieren von deskriptortabellen

Shader können nicht über deskriptortabellengrenzen hinweg dynamisch von einer bestimmten CallSite im Shader indizieren. Allerdings kann die Auswahl eines Deskriptors in einer Deskriptortabelle dynamisch im Shader-Code innerhalb von Bereichen desselben deskriptortyps (z. b. Indizierung über einen zusammenhängenden Bereich von Srvs) indiziert werden.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptortabellen](descriptor-tables.md)
</dt> </dl>

 

 




