---
description: Zeitstempel
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Zeitstempel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed14f0155a0bfbf209719f4aff97cbbd19501e6aa32d57e9f0c1cbb2df0964b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072314"
---
# <a name="time-stamps"></a>Zeitstempel

Der *Zeitstempel* definiert die Start- und Endzeiten eines Medienbeispiels, gemessen in der Streamzeit. Der Zeitstempel wird manchmal als *Präsentationszeit bezeichnet.* Beachten Sie beim Lesen des restlichen Artikels, dass nicht in allen Formaten Zeitstempel auf die gleiche Weise verwendet werden. Beispielsweise werden nicht alle MPEG-Beispiele mit einem Zeitstempel versehen. In MPEG-Filterdiagrammen wird der Zeitstempel erst dann auf jeden Frame angewendet, wenn sie aus dem Decoder ausgegeben werden.

Wenn ein Rendererfilter ein Beispiel empfängt, wird das Rendering basierend auf dem Zeitstempel geplant. Wenn das Beispiel zu spät eintrifft oder keinen Zeitstempel hat, rendert der Filter das Beispiel sofort. Andernfalls wartet der Filter bis zur Startzeit des Beispiels, bevor er das Beispiel rendert. (Er wartet auf die Startzeit durch Aufrufen der [**IReferenceClock::AdviseTime-Methode.)**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime)

Quellfilter und Parserfilter sind dafür verantwortlich, die richtigen Zeitstempel für die von ihnen verarbeiteten Beispiele zu setzen. Befolgen Sie die folgenden Richtlinien.

-   Dateiwiedergabe: Das erste Beispiel wird mit einem Zeitstempel mit einer Startzeit von 0 (null) versehen. Nachfolgende Zeitstempel werden durch die Stichprobenlänge und die Wiedergaberate bestimmt, die selbst durch das Dateiformat bestimmt wird. Der Filter, der die Datei analysiert, ist für die Berechnung der richtigen Zeitstempel verantwortlich (z. B. der [AVI-Splitter](avi-splitter-filter.md)).
-   Video- und Audioaufnahme: Jede Stichprobe wird mit einem Zeitstempel versehen, der der Startzeit entspricht, zu der sie erfasst wurde, mit den folgenden Einschränkungen:
    -   Videoframes von einem Vorschaupin (im Gegensatz zu einem Aufnahmepin) werden nicht mit einem Zeitstempel versehen. Aufgrund der Graphlatenz wird ein Videoframe, der mit der Erfassungszeit gestempelt wird, immer zu spät beim Videorenderer eintreffen. Dies kann dazu führen, dass der Renderer Frames bei einem Versuch der Qualitätskontrolle verdrungen hat. Informationen zur Qualitätskontrolle finden Sie unter [Quality-Control Management](quality-control-management.md).
    -   Audioaufnahme: Der Audioerfassungsfilter verwendet einen eigenen Satz von Puffern, die von denen des Audiotreibers getrennt sind. Der Audiotreiber füllt die Puffer des Erfassungsfilters in festen Intervallen aus. Das Intervall hängt vom Treiber ab, beträgt aber im Allgemeinen nicht mehr als 10 Millisekunden. Die Zeitstempel der Audiobeispiele geben die Zeit an, zu der der Treiber die Puffer des Audioaufnahmefilters gefüllt hat. Diese Zeiten können etwas ungenau sein, insbesondere, wenn die Anwendung eine sehr kleine Puffergröße verwendet. Die Medienzeiten spiegeln jedoch genau die Anzahl der Audiobeispiele im Puffer wider.
-   Muxfilter: Je nach Ausgabeformat muss ein Muxfilter möglicherweise Zeitstempel generieren, oder nicht. Beispielsweise verwendet das AVI-Dateiformat eine feste Framerate ohne Zeitstempel, daher geht der [AVI Mux-Filter](avi-mux-filter.md) davon aus, dass Die Stichproben ungefähr zum richtigen Zeitpunkt eintreffen. Wenn die eingehenden Zeitstempel jedoch eine Lücke anzeigen, die größer als ein Frame ist, schreibt die AVI Mux einen Indexeintrag mit der Größe 0 (null), um einen gelöschten Frame anzugeben. Bei der Dateiwiedergabe werden zur Laufzeit neue Zeitstempel generiert, wie zuvor beschrieben.

Rufen Sie zum Festlegen des Zeitstempels für ein Beispiel die [**IMediaSample::SetTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) auf.

**Medienzeiten**

Optional kann der Filter auch eine *Medienzeit für* das Beispiel angeben. In einem Videostream stellt die Medienzeit die Framenummer dar. In einem Audiostream stellt die Medienzeit die Beispielnummer im Paket dar. Wenn jedes Paket beispielsweise eine Sekunde von 44,1 Kilohertz-Audiodaten (kHz) enthält, hat das erste Paket eine Medienstartzeit von 0 (null) und eine Medienstoppzeit von 44100. In einem suchbaren Stream ist die Medienzeit immer relativ zur Startzeit des Streams. Angenommen, Sie versuchen 2 Sekunden ab dem Start eines 15-fps-Videostreams. Das erste Medienbeispiel nach der Suche hat einen Zeitstempel von null, aber eine Medienzeit von 30.

Renderer- und Muxfilter können die Medienzeit verwenden, um zu bestimmen, ob Frames oder Beispiele gelöscht wurden, indem sie auf Lücken prüfen. Filter sind jedoch nicht erforderlich, um die Medienzeit festlegen zu können. Rufen Sie zum Festlegen der Medienzeit für ein Beispiel die [**IMediaSample::SetMediaTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



