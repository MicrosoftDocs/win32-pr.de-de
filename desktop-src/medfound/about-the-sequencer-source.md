---
description: Informationen zur Sequencerquelle
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Informationen zur Sequencerquelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d81799a8bc1e46ade10989bbe485c69e839832fce0ded14220c536809e23e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065558"
---
# <a name="about-the-sequencer-source"></a>Informationen zur Sequencerquelle

Mit der Sequencerquelle kann eine Anwendung eine Sammlung von [Medienquellen](media-sources.md) sequenziell mit nahtlosen Übergängen zwischen den Quellen wieder geben. Die Sequencerquelle kann für die folgenden Szenarien verwendet werden:

-   Erstellen Sie eine Wiedergabeliste, die nahtlos von einer Medienquelle zur nächsten wechselt.
-   Gleichzeitiges Wiederspielen von Streams aus mehreren Quellen; Geben Sie z. B. die Audiodaten aus einer Datei mit dem Video aus einer anderen Datei wieder.
-   Wechseln zwischen Streams in verschiedenen Medienquellen in aufeinander folgenden Wiedergabelisteneinträgen Beispielsweise kann eine Wiedergabeliste Einträge enthalten, die dieselbe Videoquelle gemeinsam verwenden, während jeder Eintrag eine andere Audioquelle enthält.

Für jedes Element einer Wiedergabeliste erstellt die Anwendung eine separate Topologie. Die Medienquellen in diesen Topologien werden als native Quellen *bezeichnet,* um sie von der Sequencerquelle zu unterscheiden. Während der Wiedergabe wird die gesamte Sequenz von Topologien als Präsentation bezeichnet, und jede Topologie innerhalb der Sequenz wird als Segment *bezeichnet.*

Die Wiedergabe wird durch die [Mediensitzung](media-session.md)gesteuert, die Transportsteuerelemente wie Wiedergabe, Anhalten und Beenden bietet. Die Mediensitzung verwaltet auch die Präsentationszeit und sendet Ereignisse an die Anwendung. (Ereignisse aus der Sequencerquelle werden über die Mediensitzung an die Anwendung weitergeleitet.)

Zum Erstellen einer Wiedergabeliste erstellt die Anwendung eine oder mehrere Wiedergabetopologien und stellt sie in der Sequencerquelle in der gewünschten Wiedergabereihenfolge in die Warteschlange. Intern ändert die Sequencerquelle die Topologien so, dass die Quellknoten auf die Sequencerquelle anstatt auf die native Quelle zeigen. Die Anwendung sendet diese geänderten Topologien anstelle der ursprünglichen Topologien an die Mediensitzung. Dadurch kann die Sequencerquelle die nativen Quellen aggregieren und mit der Mediensitzung kommunizieren.

Um nahtlose Übergänge zwischen Segmenten zu erreichen, wird jedes Segment von der Sequencerquelle vorab gerollt. Während ein Segment wiedergegeben wird und es an der Zeit ist, das folgende Segment wieder zu spielen, gibt die Sequencerquelle ein [MENewPresentation-Ereignis](menewpresentation.md) aus, das einen Präsentationsdeskriptor enthält. Die Anwendung verwendet diesen Präsentationsdeskriptor, um die Topologie für das nächste Segment in der Präsentation zu erhalten, und stellt die Topologie in der Mediensitzung in die Warteschlange.

Die folgende Abbildung zeigt den Datenfluss für Wiedergabelisteneinträge durch die Sequencerquelle. Die Anwendung verwendet den Quellre konfliktlöser, um die nativen Quellen zu erstellen, Topologien für jedes Segment zu erstellen und die Topologien in der Sequencerquelle in die Warteschlange zu stellen.

![Diagramm, das den Datenfluss aus den Segmenten "mediasession", "abersequencersource" und "playlist" zeigt, die zu "mediasource" führen](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Wiedergabeliste](how-to-create-a-playlist.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> <dt>

[Verwenden der Sequencerquelle](using-the-sequencer-source.md)
</dt> <dt>

[Sequencerquelle](sequencer-source.md)
</dt> </dl>

 

 



