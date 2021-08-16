---
description: Uhrzeiten
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Uhrzeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0075dc2d8c2273c8ade612244f0f7d551996756e55000043ffe3bc952227fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402070"
---
# <a name="clock-times"></a>Uhrzeiten

DirectShow definiert zwei zugehörige Uhrzeiten: Verweiszeit und Streamzeit.

-   *Die Verweiszeit* ist die absolute Zeit, die von der Verweisuhr zurückgegeben wird. (Siehe [Referenzuhren](reference-clocks.md).)
-   *Die Streamzeit* wird relativ zu dem Zeitpunkt definiert, zu dem das Diagramm zuletzt ausgeführt wurde.
    -   Während das Diagramm ausgeführt wird, entspricht die Streamzeit der Verweiszeit minus Startzeit.
    -   Während das Diagramm angehalten wird, verbleibt die Streamzeit zur Streamzeit, als es angehalten wurde.
    -   Nach einem Suchvorgang wird die Streamzeit auf 0 (null) zurückgesetzt.
    -   Während das Diagramm beendet wird, ist die Streamzeit nicht definiert.

Wenn ein Medienbeispiel über einen Zeitstempel *t* verfügt, bedeutet dies, dass das Beispiel zur Streamzeit *t* gerendert werden soll. Aus diesem Grund wird die Streamzeit auch als *Präsentationszeit* bezeichnet.

Wenn eine Anwendung [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) aufruft, um das Filterdiagramm auszuführen, ruft der Filter Graph Manager [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) für jeden Filter auf. Um die geringe Zeit zu kompensieren, die für die Ausführung der Filter benötigt wird, gibt der Filter Graph Manager eine Startzeit für die Zukunft an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Zeitstempel](time-stamps.md)
</dt> </dl>

 

 



