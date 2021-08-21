---
description: Übersicht über Graph Building
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Übersicht über Graph Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16b943714e2e559286b805a8489152805d9b0e037a77603bacd00f8b0135cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152946"
---
# <a name="overview-of-graph-building"></a>Übersicht über Graph Building

Um ein Filterdiagramm zu erstellen, erstellen Sie zunächst eine Instanz von Filter Graph Manager:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



Der Filter Graph Manager unterstützt die folgenden Grapherstellungsmethoden:

-   [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) versucht, eine direkte Verbindung zwischen zwei Pins herzustellen. Wenn die Pins keine Verbindung herstellen können, schlägt die -Methode fehl.
-   [**IGraphBuilder::Verbinden**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) verbindet zwei Pins. Wenn möglich, wird eine direkte Verbindung hergestellt. Andernfalls werden Zwischenfilter verwendet, um die Verbindung abzuschließen.
-   [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) beginnt mit einem Ausgabepin und erstellt den Rest des Diagramms. Diese Methode fügt nach Bedarf Filter hinzu, die nachgeschaltet werden, bis sie einen Rendererfilter erreicht.
-   [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) erstellt ein vollständiges Dateiwiedergabediagramm.
-   [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) fügt dem Diagramm einen Filter hinzu. Der Filter wird nicht verbunden. Sie müssen den Filter erstellen, bevor Sie diese Methode aufrufen, indem Sie **Entweder CoCreateInstance** aufrufen oder den Filterzuordnungs- oder Systemgeräte-Enumerator verwenden.

Diese Methoden bieten drei grundlegende Ansätze zum Erstellen des Graphen:

1.  Der Filter Graph Manager erstellt das gesamte Diagramm.
2.  Der Filter Graph Manager erstellt einen Teil des Diagramms.
3.  Die Anwendung erstellt das gesamte Diagramm.

**Der Filter Graph Manager erstellt die gesamte Graph**

Wenn Sie einfach eine Datei wiedergeben möchten, die in einem erkannten Format wie AVI, MPEG, WAV oder MP3 erstellt wurde, verwenden Sie die **RenderFile-Methode.** Dies wird im Artikel How To Play a File (Wiedergeben [einer Datei)](how-to-play-a-file.md) erläutert.

Die **RenderFile-Methode** sucht zunächst in der Registrierung nach einem Quellfilter, der die Datei analysieren kann. Es verwendet das Protokoll (z. `https://` B. " " in der URL), die Dateierweiterung oder vordefinierte Bytemuster in der Datei, um den Quellfilter zu bestimmen. Weitere Informationen finden Sie unter [Registrieren eines benutzerdefinierten Dateityps.](registering-a-custom-file-type.md)

Um den Rest des Diagramms zu erstellen, verwendet der Filter Graph Manager einen iterativen Prozess, wobei er die Medientypen verwendet, die ein Filter auf den Ausgabepins unterstützt, und die Registrierung nach Filtern durchsucht, die diesen Medientyp als Eingabe akzeptieren. Es werden mehrere Kriterien verwendet, um die Suche einzugrenzen und Filter zu priorisieren:

-   Die *Filterkategorie* identifiziert die allgemeine Funktionalität des Filters.
-   Der Medientyp beschreibt, welche Art von Daten der Filter als Eingabe akzeptieren oder als Ausgabe übermitteln kann.
-   Die *Leistung* bestimmt die Reihenfolge, in der Filter ausprobiert werden. Wenn zwei Filter in derselben Filterkategorie dieselben Eingabetypen unterstützen, wählt der Filter Graph Manager den Filter mit dem höchsten Wert aus. Einige Filter erhalten absichtlich einen niedrigen Wert, da sie für spezielle Zwecke konzipiert sind und nur dem Graphen von der Anwendung hinzugefügt werden sollten.

Der Filter Graph Manager verwendet das [Filterzuordnungsobjekt,](filter-mapper.md) um die Registrierung zu durchsuchen.

Wenn jeder Filter hinzugefügt wird, versucht der Filter Graph Manager, ihn mit dem Ausgabepin des vorherigen Filters zu verbinden. Die Filter handeln aus, um zu bestimmen, ob sie eine Verbindung herstellen können, und wenn ja, welcher Medientyp für die Verbindung verwendet werden soll. Wenn der neue Filter keine Verbindung herstellen kann, verwirft der Filter Graph Manager ihn und versucht einen anderen Filter. Dieser Prozess wird fortgesetzt, bis jeder Stream gerendert wird.

**Der Filter Graph-Manager erstellt einen Teil der Graph**

Um etwas zu tun, das über das einfache Wiedergeben einer Datei hinausgeht, muss Ihre Anwendung mindestens einen Teil der Grapherstellung ausführen. Beispielsweise muss eine Videoerfassungsanwendung einen Erfassungsquellfilter auswählen und dem Diagramm hinzufügen. Wenn Sie Daten in eine AVI-Datei schreiben, müssen Sie dem Diagramm die FILTER AVI Mux und File Writer hinzufügen. Es ist jedoch häufig möglich, den Filter Graph Manager das Diagramm vervollständigen zu lassen. Beispielsweise können Sie eine Stecknadel für die Vorschau rendern, indem Sie die **Render-Methode** aufrufen.

**Die Anwendung erstellt die gesamte Graph**

In einigen Szenarien muss Ihre Anwendung möglicherweise den Graphen erstellen, indem sie jeden Filter hinzufügt und verbindet. In diesem Fall wissen Sie wahrscheinlich genau, welche Filter dem Diagramm hinzugefügt werden sollten. Bei diesem Ansatz fügt die Anwendung jeden Filter durch Aufrufen von **AddFilter** hinzu, listet die Pins für die Filter auf und verbindet sie, indem sie entweder **Verbinden** oder **ConnectDirect** aufruft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Diagrammen mit dem Capture Graph Builder](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Aufzählen von Geräten und Filtern](enumerating-devices-and-filters.md)
</dt> <dt>

[Aufzählen von Objekten in einem Filter Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> <dt>

[Erstellen des filter-Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



