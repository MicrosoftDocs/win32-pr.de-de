---
description: Verwenden des MPEG-2-Splitters
ms.assetid: a08e079c-41be-475a-9e88-ee46d17fe938
title: Verwenden des MPEG-2-Splitters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60505ef242c2ed9c1eab3031a005a2582b99608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358573"
---
# <a name="using-the-mpeg-2-splitter"></a>Verwenden des MPEG-2-Splitters

> [!Note]  
> Ab Microsoft® Windows® XP ist der MPEG-2-Splitter Filter veraltet. Verwenden Sie stattdessen den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) .

 

Der MPEG-2-Splitter Filter unterstützt die Wiedergabe von MPEG-2-Programmstreams im Pull-Modus, die mindestens einen der folgenden Streamtypen enthalten.

-   MPEG-2-Video
-   MPEG-2-Audiodatei
-   Dolby AC-3-Audiocodierung, wie für DVD-Video definiert
-   LPCM (Linear Pulse Code moduliert) audiocodiert, wie für DVD-Video definiert

Eine Liste der Medientypen, die der MPEG-2-Splitter unterstützt, finden Sie unter [MPEG-2 Splitter Medien Types](mpeg-2-splitter-media-types.md).

Der MPEG-2-Splitter analysiert keine Transportdaten Ströme. Verwenden Sie den MPEG-2 Demultiplexer-Filter für Transport Datenströme (nur Pushmodus).

**Zeitstempel**

Bei der Wiedergabe von MPEG-2-Programmstreams behandelt der MPEG-2-Splitter Filter den ersten systemtaktsverweis, der als Zeit Ursprung eines beliebigen Streams auftritt. Dies unterscheidet sich vom [MPEG-1-Datenstrom Splitter](mpeg-1-stream-splitter-filter.md), der Präsentationszeit Stempel verwendet. Die [**iamparser:: getsamantime**](/previous-versions/windows/desktop/api/Amparse/nf-amparse-iamparse-getparsetime) -Methode gibt die (möglicherweise geschätzte) Datenstrom System-Uhrzeitangabe für die verarbeiteten Daten zurück.

Wenn der MPEG-2-Splitter Filter ein Eingabe Beispiel mit der Diskontinuität-Eigenschaft festgelegt hat (die Diskontinuität-Eigenschaft kann mithilfe von [**imediasample festgelegt werden: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) oder [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties)) überspringt die Daten, bis das erste Paket in den Daten gefunden wird, und passt die Zeitstempel so an, dass der System Takt Verweis (SCR) für dieses Paket vor der Diskontinuität als identisch mit der SCR-Zeit gilt. Wenn die SCR-Uhr angezeigt wird, um mehr als eine Sekunde rückwärts zu springen oder um mehr als eine Sekunde zu springen, wird dies (in Verbindung mit der MPEG-2-Programm Datenstrom Spezifikation) ebenfalls als Zeit Abweichung der Uhr behandelt, und die offensichtliche Takt Abweichung wird von den Zeitstempeln subtrahiert, die an downstreamfilter weitergeleitet werden.

**Streamauswahl**

Bei der Wiedergabe des MPEG-2-Programm Datenstroms werden der erste Videostream und der erste Audiostream, der durchlaufen des Programm Datenstroms gefunden wird, ausgewählt. Bis zu eine Audiodatei und eine Videoausgabe-PIN werden unterstützt. Über die [**iamstreamselect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect) -Schnittstelle können unterschiedliche Streams desselben Typs bis zu der Zahl ausgewählt werden, die durch das audiolimit im System Header angegeben wird. Bei MPEG-2-Audiodaten wird derzeit angenommen, dass die Streams einen zusammenhängenden Bereich bilden, beginnend bei Stream 0xC0.

**Unterstützte Schnittstellen**

Der MPEG-2-Splitter Filter unterstützt die folgenden Schnittstellen.

-   [**Iamanalysieren**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse). Nur MPEG-2-Programm Datenstrom.
-   [**Iamstreamselect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect). Nur MPEG-2-Programmstream, nur Audiostreams.
-   [**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking). Schließt bytemodusansuchen ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Unterstützung in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



