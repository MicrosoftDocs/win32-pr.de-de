---
description: Uhrzeiten
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Uhrzeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392405"
---
# <a name="clock-times"></a>Uhrzeiten

DirectShow definiert zwei zugehörige Uhrzeiten: Verweis Zeit und streamzeit.

-   Die *Verweis Zeit* ist die absolute Zeit, die von der Referenzuhr zurückgegeben wurde. (Siehe [Referenzuhren](reference-clocks.md).)
-   Die *streamzeit* wird relativ zum Zeitpunkt der letzten Ausführung des Diagramms definiert.
    -   Während der Ausführung des Diagramms ist die streamzeit gleich der Verweis Zeit abzüglich der Startzeit.
    -   Während das Diagramm angehalten wird, verbleibt die streamzeit zum Zeitpunkt des anhalten.
    -   Nach einem Suchvorgang wird die streamzeit auf 0 zurückgesetzt.
    -   Während das Diagramm angehalten wird, ist die streamzeit nicht definiert.

Wenn ein Medien Beispiel einen Zeitstempel *t* aufweist, bedeutet dies, dass das Beispiel in der streamzeit *t* gerendert werden soll. Aus diesem Grund wird die streamzeit auch als *Präsentationszeit* bezeichnet.

Wenn eine Anwendung [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) aufruft, um das Filter Diagramm auszuführen, ruft der Filter Graph-Manager [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) für jeden Filter auf. Um die Zeitspanne zu kompensieren, die für die Ausführung der Filter benötigt wird, gibt der Filter Graph-Manager eine Startzeit etwas in der Zukunft an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Zeitstempel](time-stamps.md)
</dt> </dl>

 

 



