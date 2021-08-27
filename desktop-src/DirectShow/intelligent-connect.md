---
description: Intelligente Verbinden
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Intelligente Verbinden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2248dc936076dfcad1b2ad934da4ef6a8b1e28a260ff75ebca3a63ec6356bf6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107700"
---
# <a name="intelligent-connect"></a>Intelligente Verbinden

Intelligent Verbinden ist der Mechanismus, den der Filter Graph Manager zum Erstellen von Filterdiagrammen verwendet. Sie besteht aus mehreren verwandten Algorithmen, die Filter auswählen und dem Filterdiagramm hinzufügen.

Lesen Sie dieses Thema, wenn Sie Probleme beim Erstellen eines bestimmten Filterdiagramms haben und das Problem beheben möchten, oder wenn Sie einen eigenen Filter schreiben und ihn für die automatische Graph-Erstellung verfügbar machen möchten.

Intelligent Verbinden umfasst die folgenden [**IGraphBuilder-Methoden:**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder::Verbinden**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

Die [**IGraphBuilder::AddSourceFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) fügt einen Quellfilter hinzu, der eine angegebene Datei rendern kann. Zuerst sucht er in der Registrierung und stimmt mit dem Protokoll überein (z. B. ), der Dateierweiterung oder einem Satz vordefinierter Prüfbytes, bei denen es sich um Bytes an bestimmten Offsets in der Datei handelt, die bestimmten Mustern `https://` entspricht.  Weitere Informationen finden Sie unter [Registrieren eines benutzerdefinierten Dateityps.](registering-a-custom-file-type.md) Angenommen, die Methode sucht einen geeigneten Quellfilter, erstellt dann eine Instanz dieses Filters, fügt sie dem Diagramm hinzu und ruft die [**IFileSourceFilter::Load-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) des Filters mit dem Dateinamen auf.

### <a name="igraphbuilderrender"></a>IGraphBuilder::Render

Die [**IGraphBuilder::Render-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) erstellt einen Unterabschnitt eines Diagramms. Er beginnt mit einem nicht verbundenen Ausgabepin und funktioniert nachgeschaltet und fügt bei Bedarf neue Filter hinzu. Der Startfilter muss bereits im Diagramm vorhanden sein. Bei jedem Schritt sucht die **Render-Methode** nach einem Filter, der eine Verbindung mit dem vorherigen Filter herstellen kann. Der Stream kann verzweigt werden, wenn ein Verbindungsfilter über mehrere Ausgabepins verfügt. Die Suche wird beendet, wenn jeder Stream über einen Renderer verfügt. Wenn die **Render-Methode** hängen bleibt, kann sie mit einem anderen Satz von Filtern sichern und es erneut versuchen.

Um die einzelnen Ausgabepins zu verbinden, führt [**die Render-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) Folgendes aus:

1.  Wenn der Pin die [**IStreamBuilder-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) unterstützt, delegiert der Filter Graph-Manager den gesamten Prozess an die [**IStreamBuilder::Render-Methode des**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) Pins. Indem diese Schnittstelle verfügbar gemacht wird, übernimmt die Stecknadel die Verantwortung für das Erstellen des restlichen Diagramms bis zum Renderer. Allerdings unterstützen nur sehr wenige Stecknadeln diese Schnittstelle.
2.  Der Filter Graph-Manager versucht, Filter zu verwenden, die im Arbeitsspeicher zwischengespeichert werden, sofern vorhanden. Während des intelligent Verbinden kann der Filter-Graph-Manager Filter aus früheren Schritten des Prozesses zwischenspeichern. (Siehe auch [Dynamic Graph Building](dynamic-graph-building.md).)
3.  Wenn das Filterdiagramm Filter mit nicht verbundenen Eingabepins enthält, versucht der Graph-Manager sie als Nächstes. Sie können erzwingen, dass [**die Render-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) einen bestimmten Filter versucht, indem Sie diesen Filter dem Diagramm hinzufügen, bevor Sie **Render aufrufen.**
4.  Ab Windows 7 enthält DirectShow eine Liste der bevorzugten Filter für bestimmte Medienuntertypen. Wenn es einen bevorzugten Filter für den Medientyp gibt, der gerendert wird, versucht der Graph-Manager, diesen Filter als Nächstes zu filtern. Eine Anwendung kann die Liste der bevorzugten Filter mithilfe der [**IAMPluginControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) ändern. Änderungen an der Liste wirken sich auf den aktuellen Prozess der Anwendung aus und werden verworfen, nachdem der Prozess beendet wurde.
5.  Wenn kein geeigneter Filter gefunden wurde, durchsucht der Filter-Graph-Manager die Registrierung mithilfe der [**IFilterMapper2::EnumMatchingFilters-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) Es wird versucht, die bevorzugten Medientypen des Ausgabepins mit den in der Registrierung aufgeführten Medientypen zu ab stimmen.

    Jeder Filter wird mit einem *numerischen Wert registriert,* der angibt, wie bevorzugt der Filter im Vergleich zu anderen Filtern ist. Die [**EnumMatchingFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) gibt Filter in der Reihenfolge ihrer Vorteile zurück, mit einem Mindestwert **von 1: NICHT \_ \_ \_** VERWENDEN + 1. Filter werden ignoriert, bei **derEN Bzw. deren Wert NICHT \_ \_ \_ VERWENDET** werden darf. Filter werden auch in Kategorien unterteilt, die durch GUID definiert werden. Kategorien selbst haben vorteile, und die **EnumMatchingFilters-Methode** ignoriert jede Kategorie mit einem Zuschlag von NICHT VERWENDEN oder weniger, auch wenn die Filter in dieser Kategorie höhere Werte haben. **\_ \_ \_**

    Ab Windows 7 enthält DirectShow eine Liste blockierter Filter für bestimmte Medienuntertypen. Der Filter Graph-Manager überspringt Filter für diese Liste. Eine Anwendung kann die Liste der blockierten Filter mithilfe der [**IAMPluginControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) ändern. Änderungen an dieser Liste wirken sich auf den aktuellen Prozess der Anwendung aus und werden verworfen, nachdem der Prozess beendet wurde.

Zusammenfassend lässt sich zusammenfassen, [**dass die Render-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) Filter in der folgenden Reihenfolge versucht:

1.  Verwenden [**Sie IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder).
2.  Probieren Sie zwischengespeicherte Filter aus.
3.  Probieren Sie Filter im Diagramm aus.
4.  Windows 7 oder höher: Probieren Sie den bevorzugten Filter für den Medientyp aus, falls der fall ist.
5.  Suchen sie Filter in der Registrierung.

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder::RenderFile

Die [**IGraphBuilder::RenderFile-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) erstellt ein Standardmäßiges Wiedergabediagramm aus einem Dateinamen. Intern verwendet diese Methode [**AddSourceFilter,**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) um den richtigen Quellfilter zu suchen, und [**Render,**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) um den Rest des Diagramms zu erstellen.

### <a name="igraphbuilderconnect"></a>IGraphBuilder::Verbinden

Die [**IGraphBuilder::Verbinden-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) verbindet einen Ausgabepin mit einem Eingabepin. Diese Methode fügt bei Bedarf Zwischenfilter hinzu, indem eine Variation des Algorithmus verwendet wird, der für die [**Render-Methode beschrieben**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) wird:

1.  Versuchen Sie, eine direkte Verbindung zwischen den Filtern ohne Zwischenfilter herzustellen.
2.  Probieren Sie zwischengespeicherte Filter aus.
3.  Probieren Sie Filter im Diagramm aus.
4.  Windows 7 oder höher: Probieren Sie den bevorzugten Filter für den Medientyp aus, falls der fall ist.
5.  Suchen sie Filter in der Registrierung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filterkategorien](filter-categories.md)
</dt> <dt>

[Verdienst](merit.md)
</dt> <dt>

[Simulieren von Graph Building mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Erstellen des Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



