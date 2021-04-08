---
description: Festlegen und Abrufen der Position
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Festlegen und Abrufen der Position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745409"
---
# <a name="setting-and-retrieving-the-position"></a>Festlegen und Abrufen der Position

Im Filter Diagramm werden zwei Positionswerte, die aktuelle Position und die Position des Stopps, beibehalten. Diese werden wie folgt definiert:

-   Wenn das Diagramm ausgeführt wird, ist die aktuelle Position die aktuelle Wiedergabe Position relativ zum Anfang der Quelle. Wenn das Diagramm beendet oder angehalten wird, ist die aktuelle Position der Punkt, an dem das Streaming mit dem Befehl für die nächste Ausführung beginnt.
-   Die Position des Stopps ist der Punkt, an dem der Stream endet. Wenn das Diagramm die Stoppposition erreicht, werden keine weiteren Daten gestreamt, und der Filter Graph-Manager stellt ein [**EC \_ Complete**](ec-complete.md) -Ereignis zur Verfügung. (Das Diagramm wechselt jedoch nicht automatisch in den Zustand "beendet". Weitere Informationen finden Sie unter [reagieren auf Ereignisse](responding-to-events.md).)

Um diese Werte abzurufen, rufen Sie die [**imediaseeking:: getpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) -Methode auf. Die zurückgegebenen Werte sind immer relativ zur ursprünglichen Medienquelle. Standardmäßig befinden sich die Werte in den Bezugszeit Einheiten. In einigen Fällen können Sie die Zeiteinheiten ändern. Weitere Informationen finden Sie unter [Zeitformate für Such Befehle](time-formats-for-seek-commands.md).

Um an einer neuen Position zu suchen oder eine neue Halteposition festzulegen, rufen Sie die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode auf, wie im folgenden Beispiel gezeigt:


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> Eine Sekunde ist 10 Millionen Einheiten der Verweis Zeit. Der praktische Wert definiert dieses Beispiel als eine \_ Sekunde. Wenn Sie die DirectShow-Basisklassen Bibliothek verwenden, haben die Konstanten Einheiten denselben Wert.

 

Der *rtnow* -Parameter gibt die neue aktuelle Position an. Der zweite Parameter ist ein Flag, das definiert, wie *rtnow* interpretiert werden soll. In diesem Beispiel gibt das Flag für die \_ Suche nach \_ absolutepositionierung an, dass *rtnow* eine absolute Position in der Quelle angibt. Daher sucht das Filter Diagramm zwei Sekunden vom Anfang des Streams bis zu einer Position. Der *rtstoppt* -Parameter gibt die Endzeit an. Der letzte Parameter gibt an, dass *rtbeenden* auch eine absolute Position ist.

Um eine Position relativ zum vorherigen Positionswert anzugeben, verwenden Sie das \_ Flag zum Suchen der \_ relativepositionierung. Wenn Sie einen der Positionswerte unverändert lassen möchten, verwenden Sie das Flag für die \_ Suche nach \_ nopositionsflag. Der entsprechende Zeitparameter kann in diesem Fall **null** sein. Im folgenden Beispiel wird die Position um 10 Sekunden Fortschritt und die Position des Stopps unverändert gelassen:


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Wenn das Filter Diagramm angehalten wird, aktualisiert der Videorenderer das Bild nach einem Suchvorgang nicht. Für den Benutzer wird er so angezeigt, als ob die Suche nicht durchgeführt wurde. Um das Bild zu aktualisieren, halten Sie das Diagramm nach dem Suchvorgang an. Durch Anhalten des Diagramms wird ein neuer Videoframe für den Videorenderer angezeigt. Sie können die [**IMediaControl:: stopaconready**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) -Methode verwenden, die das Diagramm anhält und dann beendet.

 

 



