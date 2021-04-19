---
description: Referenzuhren
ms.assetid: 43f1a4d6-dbed-4940-a301-d863ddd34bce
title: Referenzuhren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b958787f4dbdb20cd595b10cf486f59222a072
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345987"
---
# <a name="reference-clocks"></a>Referenzuhren

Eine Funktion des Filter-Graph-Managers besteht darin, alle Filter im Diagramm mit derselben Uhr, dem sogenannten *verweistakt*, zu synchronisieren.

Jedes Objekt, das die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle verfügbar macht, kann als die verweisuhr fungieren. Die verweisuhr kann von einem DirectShow-Filter bereitgestellt werden – in der Regel der audiorenderer, der Zugriff auf einen Hardware-Timer hat. Der Filter Graph-Manager kann die Systemzeit als Fallback verwenden.

Nominell misst eine Referenzuhr die Zeit in 100-Nanosekunden-Intervallen, obwohl die tatsächliche Genauigkeit der Uhr geringer sein kann. Um die aktuelle Uhrzeit der Uhr abzurufen, rufen Sie die [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode auf. Die Baseline der Uhr – die Zeit, ab der die Zählung beginnt – hängt von der Implementierung ab, sodass der von **GetTime** zurückgegebene Wert nicht von Bedeutung ist. Was wichtig ist, wenn die Ausführung des Diagramms gestartet wurde.

Obwohl die Genauigkeit einer verweisuhr variieren kann, wird sichergestellt, dass die von der [**GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode zurückgegebenen Zeiten monoton zunehmen. Dies bedeutet, dass die Uhrzeiten nie rückwärts gehen. Wenn eine Referenzuhr Uhrzeiten aus einer Hardware Quelle erzeugt und die Hardwareuhr rückwärts springt (z. b. wenn es eine Anpassung an die Uhr gibt), sollte die **GetTime** -Methode die zuletzt gemeldete Zeit zurückgeben, bis die Hardware Uhr abfängt. Weitere Informationen finden Sie unter [**cbasereferenceclock-Klasse**](cbasereferenceclock.md).

**Standardmäßige verweisuhr**

Der Filter Graph-Manager wählt beim Ausführen des Diagramms automatisch eine Referenzuhr aus. Der folgende Algorithmus wird verwendet, um die Uhr auszuwählen:

-   Wenn die Anwendung eine Uhr ausgewählt hat (siehe unten), verwenden Sie diese Uhr.
-   Wenn das Diagramm einen Live Quell Filter enthält, der [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)unterstützt, verwenden Sie diesen Filter. Die Definition einer Live Quelle finden Sie unter [Live Sources (Live Quellen](live-sources.md)).
-   Wenn das Diagramm keine Live Quell Filter enthält, verwenden Sie einen beliebigen Filter in dem Diagramm, der [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)unterstützt, beginnend mit den Renderer und dem funktionierenden Upstream. Verbundene Filter vor nicht verbundenen Filtern bevorzugen. (Wenn das Diagramm einen Audiostream rendert, wählt dieser Schritt im Algorithmus normalerweise den audiorendererfilter aus.)
-   Wenn kein Filter eine passende Uhr bereitstellt, verwenden Sie die [System-verweisuhr](system-reference-clock.md), die auf der Systemzeit basiert.

**Festlegen der Referenzuhr**

Eine Anwendung kann eine Uhr auswählen, indem Sie die [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode für den Filter Graph-Manager aufruft. Dies sollten Sie nur tun, wenn Sie einen bestimmten Grund haben, eine andere Uhr zu bevorzugen.

Sie können den Filter Graph-Manager anweisen, keine verweisuhr zu verwenden, indem Sie [**setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) mit dem Wert **null** aufrufen. Beispielsweise können Sie dies tun, um Beispiele so schnell wie möglich zu verarbeiten. Um die standardmäßige Referenzuhr wiederherzustellen, müssen Sie die [**ifiltergraph:: setdefaultsyncsource**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-setdefaultsyncsource) -Methode für den Filter Graph-Manager aufrufen.

Wenn sich die Referenzuhr ändert, benachrichtigt der Filter Graph-Manager jeden Filter, indem er seine [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode aufruft. Anwendungen sollten diese Methode niemals für Filter aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der diagrammuhr](setting-the-graph-clock.md)
</dt> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



