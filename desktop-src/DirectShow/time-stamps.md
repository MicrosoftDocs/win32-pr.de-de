---
description: Zeitstempel
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Zeitstempel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855d2c472d7964ccad6ec8bbc87efd39b1c4cdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366322"
---
# <a name="time-stamps"></a>Zeitstempel

Der *Zeitstempel* definiert die Start-und Endzeit der Medien Stichprobe, gemessen in der streamzeit. Der Zeitstempel wird manchmal als *Präsentationszeit* bezeichnet. Wenn Sie den Rest dieses Artikels lesen, müssen Sie daran denken, dass nicht alle Formate Zeitstempel auf die gleiche Weise verwenden. Beispielsweise werden nicht alle MPEG-Beispiele mit Zeitstempel versehen. In MPEG-Filter Diagrammen wird der Zeitstempel nicht auf jeden Frame angewendet, bis Sie vom Decoder ausgegeben werden.

Wenn ein rendererfilter ein Beispiel empfängt, plant er das Rendering basierend auf dem Zeitstempel. Wenn das Beispiel spät eintrifft oder keinen Zeitstempel aufweist, rendert der Filter das Beispiel sofort. Andernfalls wartet der Filter auf die Startzeit des Beispiels, bevor das Beispiel gerendert wird. (Er wartet auf die Startzeit durch Aufrufen der [**IReferenceClock:: advisettime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode.)

Quell Filter und Parserfilter sind dafür verantwortlich, die richtigen Zeitstempel für die zu verarbeitenden Beispiele festzulegen. Verwenden Sie die folgenden Richtlinien.

-   Dateiwiedergabe: das erste Beispiel ist ein Zeitstempel mit einer Startzeit von 0 (null). Nachfolgende Zeitstempel werden anhand der Stichproben Länge und der Wiedergabe Rate bestimmt, die selbst durch das Dateiformat bestimmt wird. Der Filter, mit dem die Datei analysiert wird, ist für die Berechnung der korrekten Zeitstempel (z. b. der [avi-Splitter](avi-splitter-filter.md)) verantwortlich.
-   Video-und Audioerfassung: bei jedem Beispiel handelt es sich um einen Zeitstempel mit einer Startzeit, die der streamzeit entspricht, zu der er aufgezeichnet wurde, mit den folgenden Einschränkungen:
    -   Video Rahmen aus einer Vorschau-PIN (im Gegensatz zu einer Erfassungs-PIN) werden nicht mit einem Zeitstempel versehen. Aufgrund der Diagramm Latenz wird ein Video Frame, der mit der Erfassungs Zeit versehen wird, immer spät am Videorenderer eintreffen. Dies kann dazu führen, dass der Renderer Frames ablöscht, bei einem Versuch, die Qualität zu steuern. Informationen zur Qualitätskontrolle finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).
    -   Audioerfassung: der audioerfassungs Filter verwendet einen eigenen Satz von Puffern, die von den vom Audiotreiber verwendeten getrennt sind. Der Audiotreiber füllt die Puffer des Erfassungs Filters in festgelegten Intervallen aus. Das Intervall hängt vom Treiber ab, ist jedoch im Allgemeinen nicht länger als 10 Millisekunden. Die Zeitstempel in den Audiobeispielen geben die Zeit an, zu der der Treiber die Puffer des audioerfassungs Filters gefüllt hat. Diese Zeiten können etwas ungenau sein, insbesondere dann, wenn die Anwendung eine sehr geringe Puffergröße verwendet. Die Medien Zeiten reflektieren jedoch genau die Anzahl der Audiobeispiele im Puffer.
-   MUX-Filter: abhängig vom Ausgabeformat muss ein Mux-Filter möglicherweise Zeitstempel generieren, oder dies ist nicht möglich. Beispielsweise verwendet das AVI-Dateiformat eine Fixed-Frame-Rate ohne Zeitstempel, sodass der [AVI MUX](avi-mux-filter.md) -Filter annimmt, dass die Beispiele ungefähr zum richtigen Zeitpunkt eintreffen. Wenn die eingehenden Zeitstempel eine Lücke aufweisen, die größer als ein Frame ist, schreibt der AVI MUX jedoch einen Index Eintrag mit einer Größe von 0 (null), um einen gelöschten Frame anzugeben. Bei der Dateiwiedergabe werden neue Zeitstempel zur Laufzeit generiert, wie zuvor beschrieben.

Um den Zeitstempel für ein Beispiel festzulegen, müssen Sie die [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) -Methode aufrufen.

**Medien Zeiten**

Optional kann der Filter auch eine *Medien Zeit* für das Beispiel angeben. In einem Videostream stellt die Medien Zeit die Rahmen Zahl dar. In einem Audiostream stellt die Medien Zeit die Stichproben Nummer im Paket dar. Wenn jedes Paket z. b. eine Sekunde von 44,1 Kilohertz (kHz)-Audiodaten enthält, hat das erste Paket eine Medien Start Zeit von 0 (null) und eine Medien Endzeit von 44100. In einem durchsuchbaren Datenstrom ist die Medien Zeit immer relativ zur Startzeit des Streams. Nehmen wir beispielsweise an, Sie suchen bis zu 2 Sekunden ab dem Anfang eines Videodaten Stroms mit 15 fps. Das erste Medien Beispiel nach dem suchen hat einen Zeitstempel von NULL, aber eine Medien Zeit von 30.

Renderer-und MUX-Filter können die Medien Zeit verwenden, um zu bestimmen, ob Frames oder Beispiele gelöscht wurden, indem Sie auf Lücken prüfen. Zum Festlegen der Medien Zeit sind jedoch keine Filter erforderlich. Um die Medien Zeit in einem Beispiel festzulegen, müssen Sie die [**imediasample:: setmediatime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) -Methode aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



