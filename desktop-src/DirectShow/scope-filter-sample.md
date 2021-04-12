---
description: Bereich Filter Beispiel
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Bereich Filter Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481518"
---
# <a name="scope-filter-sample"></a>Bereich Filter Beispiel

## <a name="description"></a>BESCHREIBUNG

Der Bereichs Filter ist ein rendererfilter, der Audiodaten als Wellenformen anzeigt.

## <a name="usage"></a>Verbrauch

Um diesen Filter zu verwenden, öffnen Sie GraphEdit und stellen eine Audiodatei (oder eine Videodatei mit einem Audiostream) dar. Trennen Sie den audiorenderer temporär, und fügen Sie den Beispiel Filter Infinite-Pin Tee ([Info Filter Sample](inftee-filter-sample.md)) ein. Stellen Sie erneut eine Verbindung mit dem audiorenderer her. Verbinden Sie dann die zweite Ausgabe-PIN des Infinite-Pin Tee-Filters mit dem Bereichs Filter. Führen Sie nun das Diagramm aus.

Das Fensterbereich wird als Dialogfeld, nicht als tatsächliches Fenster implementiert. Entwickler, die Steuerelemente zum Ändern von Filter Parametern in Echtzeit erstellen, möchten möglicherweise eine Technik wie diese anstelle von Eigenschaften Seiten verwenden.

Der Bereichs Filter veranschaulicht das Einrichten eines separaten Threads zum Verarbeiten von Daten. In diesem Fall werden die Daten einfach in einen separaten Puffer in der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode kopiert und anschließend im Fensterbereich im separaten Thread gezeichnet.

Mit dem Bereichs Filter können Sie auch die Audioausgabe überwachen, um zu bestimmen, ob Sie das Clipping durchlaufen, sodass Sie den Gewinn anpassen können.

Dieser Filter wird in GraphEdit als "oszillobereich" angezeigt.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \]*-Stamm \\ Beispiele \\ \\ multimediaredirectshow- \\ Filter \\ Bereich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



