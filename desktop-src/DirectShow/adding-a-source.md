---
description: Hinzufügen einer Quelle
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Hinzufügen einer Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342963"
---
# <a name="adding-a-source"></a>Hinzufügen einer Quelle

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Erstellen Sie ein Quell Objekt auf die gleiche Weise, wie Sie andere Timeline-Objekte erstellen. Vor dem Einfügen in die Zeitachse müssen Sie jedoch mindestens die folgenden Eigenschaften für die Quelle angeben.

-   Die Start-und Endzeit Zeiten, relativ zur Zeitachse. Aufrufen der [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md) -Methode.
-   Die Mediendatei, die als Quelle verwendet werden soll. Aufrufen der [**iamtimelinesrc:: setmedianame**](iamtimelinesrc-setmedianame.md) -Methode mit einer breit Zeichen-Zeichenfolge, die den Namen der Datei darstellt.
-   Die Start-und Endzeiten der Medien, die relativ zur ursprünglichen Datei sind. Aufrufen der [**iamtimelinesrc:: setmediatimes**](iamtimelinesrc-setmediatimes.md) -Methode. Weitere Informationen zu Medien Zeiten finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).

Im folgenden Beispiel startet der Quellclip vier Sekunden in der Datei. Die Medien Dauer beträgt 10 Sekunden, doppelt so lang die Dauer der Zeitachse, was bedeutet, dass die Quelle mit der doppelten normalen Geschwindigkeit wiedergegeben wird. Die Konstanten Einheiten werden als 10 Millionen (10 ^ 7) definiert und sind gleich einer Sekunde.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Derzeit kann des nicht gleichzeitig mehr als 75 Quellen gleichzeitig erzeugen, die mit Video Compression Manager-Codecs (VCM) komprimiert wurden. Wenn das Projekt als Ganzes mehr als 75 derartige Quellen enthält, müssen Sie auch die dynamische Neuverbindung verwenden, oder des kann das Projekt nicht in der Vorschau anzeigen. Weitere Informationen finden Sie unter " [**unenderengine:: setdynamikreconnectlevel**](irenderengine-setdynamicreconnectlevel.md)".

 

Weitere Informationen zu Quellen finden Sie unter [Arbeiten mit Quellen](working-with-sources.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 



