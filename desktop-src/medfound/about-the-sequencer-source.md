---
description: Informationen über die Sequencer-Quelle
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Informationen über die Sequencer-Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526612"
---
# <a name="about-the-sequencer-source"></a>Informationen über die Sequencer-Quelle

Mithilfe der Sequencer-Quelle kann eine Anwendung eine Auflistung von [Medienquellen](media-sources.md) sequenziell wiedergeben, wobei nahtlose Übergänge zwischen den Quellen möglich sind. Die Sequencer-Quelle kann für die folgenden Szenarien verwendet werden:

-   Erstellen Sie eine Wiedergabeliste, die nahtlos von einer Medienquelle zum nächsten wechselt.
-   Wiedergabe von Streams aus mehreren Quellen gleichzeitig; Beispielsweise können Sie die Audiodatei aus einer Datei mit dem Video aus einer anderen Datei abspielen.
-   Wechsel zwischen Streams in unterschiedlichen Medienquellen in aufeinander folgenden Wiedergabelisten Einträgen Beispielsweise kann eine Wiedergabeliste Einträge aufweisen, die dieselbe Videoquelle gemeinsam verwenden, während jeder Eintrag eine andere Audioquelle enthält.

Für jedes Element einer Wiedergabeliste erstellt die Anwendung eine separate Topologie. Die Medienquellen in diesen Topologien werden als *native Quellen* bezeichnet, um Sie von der Sequencer-Quelle zu unterscheiden. Während der Wiedergabe wird die gesamte Sequenz von Topologien als *Darstellung* bezeichnet, und jede Topologie innerhalb der Sequenz wird als *Segment* bezeichnet.

Die Wiedergabe wird von der [Medien Sitzung](media-session.md)gesteuert, die Transport Steuerelemente bereitstellt, z. b. Wiedergabe, anhalten und anhalten. Die Medien Sitzung verwaltet auch die Präsentationszeit und sendet Ereignisse an die Anwendung. (Ereignisse aus der Sequencer-Quelle werden über die Medien Sitzung an die Anwendung weitergeleitet.)

Um eine Wiedergabeliste zu erstellen, erstellt die Anwendung eine oder mehrere Wiedergabe Topologien und fügt Sie in der gewünschten Wiedergabe Reihenfolge an der Sequencer-Quelle in die Warteschlange ein. Intern ändert die Sequencer-Quelle die Topologien so, dass die Quellknoten anstelle der systemeigenen Quelle auf die Sequencer-Quelle zeigen. Die Anwendung sendet diese geänderten Topologien anstelle der ursprünglichen Topologien an die Medien Sitzung. Dadurch kann die Sequencer-Quelle die systemeigenen Quellen aggregieren und mit der Medien Sitzung kommunizieren.

Um nahtlose Übergänge zwischen Segmenten zu erreichen, werden die einzelnen Segmente durch die Sequencer-Quelle vorab überschritten. Während ein Segment abgespielt wird und bevor es an der Zeit ist, das folgende Segment wiederzugeben, löst die Sequencer-Quelle ein [menewpresentation](menewpresentation.md) -Ereignis aus, das einen Präsentations Deskriptor enthält. Die Anwendung verwendet diesen Präsentations Deskriptor, um die Topologie für das nächste Segment in der Präsentation zu erhalten, und fügt die Topologie in die Medien Sitzung ein.

Die folgende Abbildung zeigt den Datenfluss für Wiedergabelisten Einträge über die Sequencer-Quelle. Die Anwendung verwendet den quellresolver zum Erstellen der systemeigenen Quellen, erstellt Topologien für die einzelnen Segmente und fügt die Topologien in der Sequencer-Quelle in die Warteschlange ein.

![Diagramm, das den Datenfluss von imfmediasession-, imfsequencersource-und Wiedergabelisten Segmenten anzeigt, die zu imfmediasource führen](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Wiedergabeliste](how-to-create-a-playlist.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> <dt>

[Verwenden der Sequencer-Quelle](using-the-sequencer-source.md)
</dt> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 



