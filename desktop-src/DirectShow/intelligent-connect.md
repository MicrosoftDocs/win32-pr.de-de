---
description: Intelligent Connect
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Intelligent Connect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aead305867ccec1f1f1f0cbd76c652ba3ec412
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482302"
---
# <a name="intelligent-connect"></a>Intelligent Connect

Intelligent Connect ist der Mechanismus, den der Filter Graph-Manager zum Erstellen von Filter Diagrammen verwendet. Sie besteht aus mehreren verwandten Algorithmen, die Filter auswählen und dem Filter Diagramm hinzufügen.

Lesen Sie dieses Thema, wenn Sie Probleme beim Erstellen eines bestimmten Filter Diagramms haben und das Problem beheben möchten, oder wenn Sie einen eigenen Filter schreiben und ihn für die automatische Diagramm Erstellung zur Verfügung stellen möchten.

Intelligent Connect umfasst die folgenden [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Methoden:

-   [**Igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**Igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**Igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**Igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>Igraphbuilder:: addsourcefilter

Die [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) -Methode fügt einen Quell Filter hinzu, der eine angegebene Datei erzeugen kann. Zuerst sucht Sie in der Registrierung und findet eine Übereinstimmung mit dem Protokoll (z. b. `https://` ), der Dateinamenerweiterung oder einer Gruppe von vordefinierten *Prüf Bytes*, bei denen es sich um Bytes in bestimmten Offsets in der Datei handelt, die bestimmten Mustern entsprechen. Weitere Informationen finden Sie unter [Registrieren eines benutzerdefinierten Dateityps](registering-a-custom-file-type.md). Vorausgesetzt, dass die-Methode einen geeigneten Quell Filter ausstellt, erstellt Sie eine Instanz dieses Filters, fügt Sie dem Diagramm hinzu und ruft die [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) -Methode des Filters mit dem Dateinamen auf.

### <a name="igraphbuilderrender"></a>Igraphbuilder:: Rendering

Die [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) -Methode erstellt einen unter Abschnitt eines Diagramms. Er beginnt mit einer nicht verbundenen Ausgabepin und funktioniert nach dem Bedarf, wobei nach Bedarf neue Filter hinzugefügt werden. Der Start Filter muss bereits im Diagramm vorhanden sein. Bei jedem Schritt sucht die Methode " **Rendering** " nach einem Filter, der eine Verbindung mit dem vorherigen Filter herstellen kann. Der Stream kann verzweigt werden, wenn ein Verbindungs Filter über mehrere Ausgabe Pins verfügt. Die Suche wird beendet, wenn jeder Stream einen Renderer hat. Wenn die **Rendering** -Methode hängen bleibt, kann Sie wieder gesichert werden, und es wird versucht, eine andere Gruppe von Filtern zu verwenden.

Zum Verbinden der einzelnen Ausgabepin führt die [**Rendermethode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) Folgendes aus:

1.  Wenn die PIN die [**istreambuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) -Schnittstelle unterstützt, delegiert der Filter Graph-Manager den gesamten Prozess an die [**istreambuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) -Methode der PIN. Wenn diese Schnittstelle verfügbar gemacht wird, übernimmt die PIN die Verantwortung für das aufbauen des restlichen Diagramms, bis zum Renderer. Diese Schnittstelle wird jedoch von sehr wenigen Pins unterstützt.
2.  Der Filter Graph-Manager versucht, ggf. Filter zu verwenden, die im Arbeitsspeicher zwischengespeichert werden. Während des intelligenten Verbindungsprozesses kann der Filter Graph-Manager Filter aus früheren Schritten im Prozess Zwischenspeichern. (Siehe auch [dynamische Diagramm Bildung](dynamic-graph-building.md).)
3.  Wenn das Filter Diagramm Filter mit nicht verbundenen Eingabe Pins enthält, versucht der Filter Graph-Manager Sie als nächstes. Sie können erzwingen, dass die [**Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) -Methode einen bestimmten Filter ausprobiert, indem Sie diesen Filter dem Diagramm hinzufügen, bevor Sie **Rendering** aufrufen.
4.  Ab Windows 7 verfügt DirectShow über eine Liste der bevorzugten Filter für bestimmte Medien Untertypen. Wenn für den Medientyp, der gerendert wird, ein bevorzugter Filter vorhanden ist, versucht der Filter Graph-Manager, den Filter Next zu filtern. Eine Anwendung kann die Liste der bevorzugten Filter mithilfe der [**iamplugincontrol**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) -Schnittstelle ändern. Änderungen an der Liste wirken sich auf den aktuellen Prozess der Anwendung aus und werden verworfen, nachdem der Prozess beendet wurde.
5.  Wenn kein geeigneter Filter gefunden wurde, durchsucht der Filter Graph-Manager die Registrierung mithilfe der [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode. Es wird versucht, die bevorzugten Medientypen der Ausgabepin mit den in der Registrierung aufgelisteten Medientypen abzugleichen.

    Jeder Filter wird mit einem *Verdienst* registriert, einem numerischen Wert, der angibt, wie vorzuziehen der Filter ist, relativ zu anderen Filtern. Die [**enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) -Methode gibt Filter in der Reihenfolge der Vorzüge zurück, mit einem minimal Verdienst, dass **\_ Sie \_ nicht \_** + 1 verwenden. Sie ignoriert Filter mit dem Verdienst, dass Sie nicht oder weniger **\_ \_ \_ verwenden** . Filter werden auch in Kategorien gruppiert, die durch GUID definiert werden. Die Kategorien selbst haben einen Verdienst, und die **enummatchingfilters** -Methode ignoriert alle Kategorien mit einem Verdienst, die nicht oder weniger **\_ \_ \_ verwenden** , auch wenn die Filter in dieser Kategorie höhere Werte aufweisen.

    Ab Windows 7 enthält DirectShow eine Liste der blockierten Filter für bestimmte Medien Untertypen. Der Filter Graph-Manager überspringt Filter in dieser Liste. Eine Anwendung kann die Liste der blockierten Filter mithilfe der [**iamplugincontrol**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) -Schnittstelle ändern. Änderungen an dieser Liste wirken sich auf den aktuellen Prozess der Anwendung aus und werden verworfen, nachdem der Prozess beendet wurde.

Zusammenfassend versucht die [**Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) -Methode Filter in der folgenden Reihenfolge:

1.  Verwenden Sie [**istreambuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder).
2.  Testen Sie zwischengespeicherte Filter.
3.  Testen Sie die Filter im Diagramm.
4.  Windows 7 oder höher: Testen Sie ggf. den bevorzugten Filter für den Medientyp.
5.  Suchen Sie in der Registrierung nach Filtern.

### <a name="igraphbuilderrenderfile"></a>Igraphbuilder:: RenderFile

Die [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) -Methode erstellt ein Standard Wiedergabe Diagramm aus einem Dateinamen. Intern verwendet diese Methode [**addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , um den richtigen Quell Filter zu suchen, und [**Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) , um den Rest des Diagramms zu erstellen.

### <a name="igraphbuilderconnect"></a>Igraphbuilder:: Connect

Die [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) -Methode verbindet eine Ausgabe-PIN mit einer Eingabe-PIN. Diese Methode fügt bei Bedarf zwischen Filter hinzu, wobei eine Variation des Algorithmus verwendet wird, [](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) der für die Renderingmethode beschrieben wird:

1.  Versuchen Sie, eine direkte Verbindung zwischen den Filtern ohne zwischen Filter herzustellen.
2.  Testen Sie zwischengespeicherte Filter.
3.  Testen Sie die Filter im Diagramm.
4.  Windows 7 oder höher: Testen Sie ggf. den bevorzugten Filter für den Medientyp.
5.  Suchen Sie in der Registrierung nach Filtern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Filter Kategorien](filter-categories.md)
</dt> <dt>

[Verdienst](merit.md)
</dt> <dt>

[Simulieren der Diagramm Erstellung mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Aufbauen des Filter Diagramms](building-the-filter-graph.md)
</dt> </dl>

 

 



