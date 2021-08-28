---
description: Referenzuhren
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Referenzuhren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ad0a262b36ce78c6a2f355b30b3c6876c7e78a7807970592b6f15287c0e2c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697110"
---
# <a name="reference-clocks"></a>Referenzuhren

Eine Funktion des Filter-Graph-Managers besteht in der Synchronisierung aller Filter im Diagramm mit der gleichen Uhr, die als *Referenzuhr bezeichnet wird.*

Jedes Objekt, das die [**IReferenceClock-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) verfügbar macht, kann als Referenzuhr fungieren. Die Referenzuhr kann von einem DirectShow-Filter bereitgestellt werden– in der Regel vom Audiorenderer, der Zugriff auf einen Hardwarezeitgeber hat. Als Fallback kann der Filter Graph Manager die Systemzeit verwenden.

Nominell misst eine Referenzuhr die Zeit in Intervallen von 100 Nanosekunden, obwohl die tatsächliche Genauigkeit der Uhr möglicherweise geringer ist. Um die aktuelle Uhrzeit der Uhr abzurufen, rufen Sie die [**IReferenceClock::GetTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) auf. Die Baseline der Uhr – die Zeit, ab der sie gezählt wird – hängt von der Implementierung ab, sodass der von **GetTime** zurückgegebene Wert von Natur aus nicht aussagekräftig ist. Wichtig ist das Delta ab dem Start der Ausführung des Graphen.

Obwohl die Genauigkeit einer Verweisuhr variieren kann, werden die von der [**GetTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) zurückgegebenen Zeiten garantiert monoton erhöht. Anders ausgedrückt: Die Zeitzeiten gehen nie rückwärts. Wenn eine Referenzuhr Uhrzeiten aus einer Hardwarequelle generiert und die Hardwareuhr rückwärts springt (z. B. bei einer Anpassung der Uhr), sollte die **GetTime-Methode** weiterhin die letzte gemeldete Zeit zurückgeben, bis die Hardwareuhr aufholt. Weitere Informationen finden Sie unter [**CBaseReferenceClock-Klasse.**](cbasereferenceclock.md)

**Standardreferenzuhr**

Der Filter Graph Manager wählt automatisch eine Referenzuhr aus, wenn das Diagramm ausgeführt wird. Sie verwendet den folgenden Algorithmus, um die Uhr auszuwählen:

-   Wenn die Anwendung eine Uhr ausgewählt hat (siehe unten), verwenden Sie diese Uhr.
-   Wenn das Diagramm einen Livequellenfilter enthält, der [**IReferenceClock unterstützt,**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)verwenden Sie diesen Filter. Informationen zur Definition einer Livequelle finden Sie unter [Livequellen.](live-sources.md)
-   Wenn das Diagramm KEINE Livequellenfilter enthält, verwenden Sie einen beliebigen Filter im Diagramm, der [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)unterstützt, beginnend mit den Renderern und dem Arbeiten im Upstream. Verbundene Filter gegenüber nicht verbundenen Filtern bevorzugen. (Wenn das Diagramm einen Audiostream rendert, wählt dieser Schritt im Algorithmus normalerweise den Audiorendererfilter aus.)
-   Wenn kein Filter eine geeignete Uhr enthält, verwenden Sie die [Systemverweisuhr,](system-reference-clock.md)die auf der Systemzeit basiert.

**Festlegen der Referenzuhr**

Eine Anwendung kann eine Uhr auswählen, indem sie die [**IMediaFilter::SetSyncSource-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) im Filter-Graph Manager aufruft. Dies sollten Sie nur tun, wenn Sie aus einem bestimmten Grund eine andere Uhr bevorzugen.

Sie können den Filter Graph Manager anweisen, keine Referenzuhr zu verwenden, indem [**Sie SetSyncSource mit**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) dem Wert **NULL aufrufen.** Sie können dies beispielsweise tun, um Beispiele so schnell wie möglich zu verarbeiten. Rufen Sie zum Wiederherstellen der Standardreferenzuhr die [**IFilterGraph::SetDefaultSyncSource-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) im Filter-Graph Manager auf.

Wenn sich die Referenzuhr ändert, benachrichtigt der Filter Graph Manager jeden Filter, indem er seine [**IMediaFilter::SetSyncSource-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) aufruft. Anwendungen sollten diese Methode niemals für Filter aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Graph Uhr](setting-the-graph-clock.md)
</dt> <dt>

[Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



