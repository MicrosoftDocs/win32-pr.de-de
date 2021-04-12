---
description: Live Quellen
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Live Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43486cf3db797f493c9446bf782989b8beaae829
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481750"
---
# <a name="live-sources"></a>Live Quellen

Eine Live Quelle, auch als *pushquelle* bezeichnet, empfängt Daten in Echtzeit. Beispiele hierfür sind Video Erfassung und Netzwerkübertragungen. Im Allgemeinen kann eine Live Quelle die Rate, mit der Daten eintreffen, nicht steuern.

Ein Filter wird als Live Quelle betrachtet, wenn eine der folgenden Optionen zutrifft:

-   Der Filter gibt das Flag "am \_ Filter \_ misc \_ Flags \_ is \_ Source" aus der [**iamfilterfehlflags:: getfehlflags**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) -Methode zurück, und mindestens einer seiner Ausgabe Pins macht die [**iampushsource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) -Schnittstelle verfügbar.
-   Der Filter macht die " [**ikspropertyset**](ikspropertyset.md) "-Schnittstelle verfügbar und verfügt über eine Aufzeichnungs-PIN (Erfassung der PIN- \_ Kategorie \_ ) Weitere Informationen finden Sie unter [PIN-Eigenschaften Satz](pin-property-set.md) .

Wenn ein Live Quell Filter eine Uhr bereitstellt, bevorzugt der Filter Graph-Manager diese Uhr, wenn er die Diagramm-verweisuhr auswählt. Weitere Informationen finden Sie unter [Referenzuhren](reference-clocks.md) .

**Latenz**

Die Latenz eines Filters ist die Zeitspanne, die der Filter für die Verarbeitung eines Beispiels benötigt. Bei Live Quellen wird die Latenz durch die Größe des Puffers bestimmt, der zum Speichern von Beispielen verwendet wird. Angenommen, das Filter Diagramm enthält eine Videoquelle mit einer Latenz von 33 Millisekunden (MS) und einer Audioquelle mit einer Latenz von 500 ms. Jeder Video Frame kommt bei dem Videorenderer ungefähr 470 MS vor, bevor das entsprechende Audiobeispiel den audiorenderer erreicht. Die Audiodatei und das Video werden nicht synchronisiert, es sei denn, das Diagramm kompensiert den Unterschied.

Live Quellen können über die [**iampushsource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) -Schnittstelle synchronisiert werden. Der Filter Graph-Manager synchronisiert keine Live Quellen, es sei denn, die Anwendung ermöglicht die Synchronisierung durch Aufrufen der [**iamgraphstreams:: syncusingstreamoffset**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) -Methode. Wenn die Synchronisierung aktiviert ist, fragt der Filter Diagramm-Manager jeden Quell Filter nach **iampushsource** ab. Wenn der Filter **iampushsource** unterstützt, ruft der Filter Graph-Manager [**iamlatency:: getlatency**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) auf, um die erwartete Latenzzeit des Filters abzurufen. (Die **iampushsource** -Schnittstelle erbt [**iamlatency**](/windows/desktop/api/Strmif/nn-strmif-iamlatency).) Aus den kombinierten Latenz Werten bestimmt der Filter Diagramm-Manager die maximale erwartete Latenz im Diagramm. Anschließend wird [**iampushsource:: setstreamoffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) aufgerufen, um jedem Quell Filter einen Streamoffset zu verleihen, den dieser Filter den von ihm generierten Zeitstempeln hinzufügt.

Diese Methode ist hauptsächlich für die Live Vorschau vorgesehen. Beachten Sie jedoch, dass eine Vorschau-PIN auf einem Live Erfassungsgerät (z. b. eine Kamera) keine Zeitstempel für die von ihm bereitgestellten Beispiele festgelegt hat. Um diese Methode mit einem Live Capture-Gerät verwenden zu können, müssen Sie daher eine Vorschau von der Erfassungs-PIN verwenden. Weitere Informationen finden Sie unter [DirectShow-Video Erfassungs Filter](directshow-video-capture-filters.md).

Derzeit wird die [**iampushsource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) -Schnittstelle durch den [VFW-Erfassungs](vfw-capture-filter.md) Filter und den [audioerfassungs](audio-capture-filter.md) Filter unterstützt.

**Raten Übereinstimmung**

Wenn ein rendererfilter Beispiele mit einer verweiszeit plant, der Quell Filter Sie jedoch mit einer anderen Uhr erzeugt, können bei der Wiedergabe Fehler auftreten. Der Renderer kann schneller als die Quelle ausgeführt werden, wodurch Lücken in den Daten verursacht werden. Oder es kann langsamer als die Quelle ausgeführt werden, sodass sich die Stichproben von Beispielen anwachsen lassen, bis zu einem bestimmten Zeitpunkt das Diagramm Beispiele löscht. In der Regel kann eine Live Quelle die Produktionsrate nicht steuern. Daher sollte der Renderer die Raten mit der Quelle vergleichen.

Zurzeit führt nur der audiorenderer eine Raten Übereinstimmung aus, da die Abrufe in der Audiowiedergabe besser erkennbar sind als in Videos. Um die Raten Übereinstimmung auszuführen, muss der audiorenderer etwas auswählen, mit dem die Raten übereinstimmen. Dabei wird der folgende Algorithmus verwendet:

-   Wenn das Diagramm keine verweisuhr verwendet, versucht der audiorenderer nicht, die Raten abzugleichen. (Wenn das Diagramm keine Referenzuhr hat, werden die Beispiele immer sofort beim Eintreffen gerendert.)
-   Wenn für das Diagramm eine Referenzuhr vorhanden ist, prüft der audiorenderer, ob eine Livequelle mit den zuvor beschriebenen Kriterien vorhanden ist. Andernfalls stimmt der audiorenderer nicht mit den Raten identisch.
-   Wenn eine streamingstromquelle vorhanden ist und diese Quelle die [**iampushsource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) -Schnittstelle in der Ausgabe-PIN verfügbar macht, ruft der audiorenderer [**iampushsource:: getpushsourceflags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags)auf. Es sucht nach einem der folgenden Flags:
    -   ist \_ pushsourcecaps \_ internal \_ RM. Dieses Flag bedeutet, dass der Quell Filter über einen eigenen Mechanismus zur Raten Übereinstimmung verfügt, sodass der audiorenderer nicht mit den Sätzen übereinstimmt.
    -   " \_ pushsourcecaps" ist \_ nicht \_ Live. Dieses Flag bedeutet, dass der Quell Filter nicht wirklich eine Live Quelle ist, obwohl er die [**iampushsource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) -Schnittstelle verfügbar macht. Daher stimmt der audiorenderer nicht mit den Raten identisch.
    -   Uhr \_ pushsourcecaps \_ private \_ Uhr. Dieses Flag bedeutet, dass der Quell Filter eine private Uhr verwendet, um Zeitstempel zu generieren. In diesem Fall gleicht der audiorenderer die Raten für die Zeitstempel ab. (Wenn die Beispiele jedoch keine Zeitstempel haben, ignoriert der Renderer dieses Flag.)
-   Wenn [**getpushsourceflags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) keine Flags (null) zurückgibt, hängt das Verhalten des audiorenderers von der graphuhr und davon ab, ob die Beispiele Zeitstempel haben:
    -   Wenn es sich bei dem audiorenderer nicht um die graphuhr handelt und die Beispiele Zeitstempel haben, gleicht der audiorenderer die Raten für die Zeitstempel ab.
    -   Wenn die Beispiele nicht über Zeitstempel verfügen, versucht der audiorenderer, die Rate eingehender Audiodaten abzugleichen.
    -   Wenn der audiorenderer die Diagramm Uhr ist, versucht er, die eingehende Datenrate abzugleichen.

Der Grund für den letzten Fall ist Folgendes: Wenn es sich beim audiorenderer um die Referenzuhr handelt und der Quell Filter die gleiche Uhr zum Generieren von Zeitstempeln verwendet, kann der audiorenderer keine Raten mit den Zeitstempeln vergleichen. Wenn dies der Fall war, würde er versuchen, die Raten mit sich selbst abzugleichen, was zu einer Abweichung der Uhr führen könnte. In diesem Fall entspricht der Renderer daher der Rate eingehender Audiodaten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



