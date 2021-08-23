---
description: Festlegen und Abrufen der Position
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Festlegen und Abrufen der Position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7951ce12fe498a4f230ab3d1ac84796621e04ed025010678f1c43a39d88eb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683690"
---
# <a name="setting-and-retrieving-the-position"></a>Festlegen und Abrufen der Position

Das Filterdiagramm behält zwei Positionswerte bei: die aktuelle Position und die Stoppposition. Diese werden wie folgt definiert:

-   Wenn das Diagramm ausgeführt wird, ist die aktuelle Position die aktuelle Wiedergabeposition relativ zum Anfang der Quelle. Wenn das Diagramm beendet oder angehalten wird, ist die aktuelle Position der Punkt, an dem das Streaming beim nächsten Ausführungsbefehl beginnt.
-   Die Stoppposition ist der Punkt, an dem der Stream endet. Wenn das Diagramm die Stoppposition erreicht, werden keine Daten mehr gestreamt, und der Filtergraph-Manager sendet ein [**EC \_ COMPLETE-Ereignis.**](ec-complete.md) (Das Diagramm wechselt jedoch nicht automatisch in den Zustand "Beendet". Weitere Informationen finden Sie unter [Reagieren auf Ereignisse](responding-to-events.md).)

Um diese Werte abzurufen, rufen Sie die [**IMediaSeeking::GetPositions-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) auf. Die zurückgegebenen Werte sind immer relativ zur ursprünglichen Medienquelle. Standardmäßig befinden sich die Werte in Bezugszeiteinheiten. In einigen Fällen können Sie die Zeiteinheiten ändern. Weitere Informationen finden Sie unter [Zeitformate für Seek-Befehle.](time-formats-for-seek-commands.md)

Um eine neue Position zu suchen oder eine neue Stoppposition festzulegen, rufen Sie die [**IMediaSeeking::SetPositions-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) auf, wie im folgenden Beispiel gezeigt:


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
> Eine Sekunde beträgt 10.000.000 Einheiten der Referenzzeit. Der Einfachheit halber wird dieser Wert im Beispiel als ONE \_ SECOND definiert. Wenn Sie die DirectShow-Basisklassenbibliothek verwenden, hat die Konstante UNITS den gleichen Wert.

 

Der *rtNow-Parameter* gibt die neue aktuelle Position an. Der zweite Parameter ist ein Flag, das definiert, wie rtNow interpretiert werden *soll.* In diesem Beispiel gibt das FLAG AM \_ SEEKING \_ AbsolutePositioning an, dass *rtNow* eine absolute Position in der Quelle angibt. Daher sucht das Filterdiagramm zwei Sekunden nach dem Start des Streams nach einer Position. Der *rtStop-Parameter* gibt die Beendigungszeit an. Der letzte Parameter gibt an, dass *rtStop* auch eine absolute Position ist.

Um eine Position relativ zum vorherigen Positionswert anzugeben, verwenden Sie das FLAG AM \_ SEEKING \_ RelativePositioning. Um einen der Positionswerte unverändert zu lassen, verwenden Sie das AM \_ SEEKING \_ NoPositioning-Flag. Der entsprechende Zeitparameter kann in diesem Fall **NULL** sein. Im folgenden Beispiel wird nach 10 Sekunden gesucht, die Stoppposition bleibt jedoch unverändert:


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



Wenn das Filterdiagramm beendet wird, aktualisiert der Videorenderer das Bild nach einem Suchvorgang nicht. Für den Benutzer sieht es so aus, als ob die Suche nicht erfolgt wäre. Um das Bild zu aktualisieren, halten Sie das Diagramm nach dem Suchvorgang an. Durch Anhalten des Diagramms wird ein neuer Videoframe für den Videorenderer angezeigt. Sie können die [**IMediaControl::StopWhenReady-Methode**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) verwenden, die das Diagramm anhält und dann beendet.

 

 



