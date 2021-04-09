---
description: Übersicht über die Diagramm Bildung
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Übersicht über die Diagramm Bildung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124364"
---
# <a name="overview-of-graph-building"></a>Übersicht über die Diagramm Bildung

Erstellen Sie zunächst eine Instanz des Filter Graph-Managers, um ein Filter Diagramm zu erstellen:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



Der Filter Graph-Manager unterstützt die folgenden Graph-erbauungsmethoden:

-   [**Ifiltergraph:: connectdirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) versucht, eine direkte Verbindung zwischen zwei Pins herzustellen. Wenn die Pins keine Verbindung herstellen kann, schlägt die Methode fehl.
-   [**Igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) verbindet zwei Pins. Wenn möglich, wird eine direkte Verbindung hergestellt. Andernfalls werden zwischen Filter verwendet, um die Verbindung abzuschließen.
-   [**Igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) beginnt mit einem Ausgabepin und erstellt den Rest des Diagramms. Mit diesen Methoden werden nach Bedarf Filter hinzugefügt, die nach unten laufen, bis ein rendererfilter erreicht wird.
-   [**Igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) erstellt ein ganzes Dateiwiedergabe Diagramm.
-   [**Ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) fügt dem Diagramm einen Filter hinzu. Der Filter wird nicht verbunden. Sie müssen den Filter vor dem Aufrufen dieser Methode erstellen, indem Sie entweder **CoCreateInstance** aufrufen oder den Filter Mapper oder den Enumerator des System Geräts verwenden.

Diese Methoden bieten drei grundlegende Ansätze zum Erstellen des Diagramms:

1.  Der Filter Graph-Manager erstellt das gesamte Diagramm.
2.  Der Filter Graph-Manager erstellt einen Teil des Diagramms.
3.  Die Anwendung erstellt das gesamte Diagramm.

**Der Filter Graph-Manager erstellt das gesamte Diagramm.**

Wenn Sie nur eine Datei wiedergeben möchten, die in einem erkannten Format (z. b. AVI, MPEG, WAV oder MP3) erstellt wurde, verwenden Sie die **RenderFile** -Methode. Der Artikel [zum Wiedergeben einer Datei](how-to-play-a-file.md) zeigt, wie Sie dies tun.

Die **RenderFile** -Methode beginnt mit der Suche nach einem Quell Filter, mit dem die Datei analysiert werden kann, in der Registrierung. Er verwendet das Protokoll (z. b. " `https://` " in der URL), die Dateierweiterung oder vordefinierte Byte Muster in der Datei, um den Quell Filter zu ermitteln. Weitere Informationen finden Sie unter [Registrieren eines benutzerdefinierten Dateityps](registering-a-custom-file-type.md).

Um den Rest des Diagramms zu erstellen, verwendet der Filter Graph-Manager einen iterativen Prozess, bei dem die von einem Filter unterstützten Medientypen auf den Ausgabe Pins verwendet werden, und durchsucht die Registrierung nach Filtern, die den Medientyp als Eingabe akzeptieren. Es werden verschiedene Kriterien verwendet, um die Such-und Priorisieren von Filtern einzuschränken:

-   Die *Kategorie Filter* identifiziert die allgemeine Funktionalität des Filters.
-   Der Medientyp beschreibt, welche Art von Daten der Filter als Eingabe oder als Ausgabe annehmen kann.
-   Das *Verdienst* legt die Reihenfolge fest, in der Filter ausprobiert werden. Wenn zwei Filter in der gleichen Filterkategorie beide dieselben Eingabetypen unterstützen, wählt der Filter Graph-Manager den Wert mit dem höchsten Wert aus. Einige Filter verfügen über einen niedrigen Wert, da Sie für spezielle Zwecke konzipiert sind und nur dem Graph von der Anwendung hinzugefügt werden sollen.

Der Filter Graph-Manager verwendet das [Filter Mapper](filter-mapper.md) -Objekt, um die Registrierung zu durchsuchen.

Wenn jeder Filter hinzugefügt wird, versucht der Filter Graph-Manager, ihn mit der Ausgabe-PIN des vorherigen Filters zu verbinden. Die Filter werden ausgehandelt, um zu bestimmen, ob Sie eine Verbindung herstellen können. wenn dies der Fall ist, welcher Medientyp für die Verbindung verwendet werden soll. Wenn der neue Filter keine Verbindung herstellen kann, verwirft der Filter Graph-Manager ihn und versucht einen anderen Filter. Dieser Prozess wird fortgesetzt, bis jeder Stream gerendert wird.

**Der Filter Graph-Manager erstellt einen Teil des Diagramms.**

Um etwas über das einfache Abspielen einer Datei hinaus zu tun, muss Ihre Anwendung mindestens einen Teil der Diagramm erbauarbeit ausführen. Beispielsweise muss eine Video Erfassungs Anwendung einen Erfassungs Quell Filter auswählen und dem Diagramm hinzufügen. Wenn Sie Daten in eine AVI-Datei schreiben, müssen Sie dem Diagramm die Filter "AVI MUX" und "File Writer" hinzufügen. Es ist jedoch oft möglich, dass der Filter Graph-Manager das Diagramm vervollständigt. Beispielsweise können Sie eine PIN für die Vorschau durch Aufrufen der **Rendering** -Methode Rendering.

**Die Anwendung erstellt das gesamte Diagramm.**

In einigen Szenarien muss Ihre Anwendung möglicherweise das Diagramm erstellen, indem Sie die einzelnen Filter hinzufügen und verbinden. In diesem Fall wissen Sie wahrscheinlich genau, welche Filter dem Diagramm hinzugefügt werden sollen. Bei dieser Vorgehensweise fügt die Anwendung jeden Filter hinzu, indem Sie **addFilter** aufrufen, die Pins für die Filter auflistet und Sie durch Aufrufen von **Connect** oder **connectdirect** verbindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Auflisten von Geräten und Filtern](enumerating-devices-and-filters.md)
</dt> <dt>

[Auflisten von Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> <dt>

[Aufbauen des Filter Diagramms](building-the-filter-graph.md)
</dt> </dl>

 

 



