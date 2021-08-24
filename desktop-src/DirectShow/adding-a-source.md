---
description: Hinzufügen einer Quelle
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Hinzufügen einer Quelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab2440ff50bbb4a3a610f9341405538a88dc6bf16ce2153a327f3b4578f3aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690530"
---
# <a name="adding-a-source"></a>Hinzufügen einer Quelle

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Erstellen Sie ein Quellobjekt auf die gleiche Weise wie andere Zeitachsenobjekte. Vor dem Einfügen in die Zeitachse müssen Sie jedoch mindestens die folgenden Eigenschaften für die Quelle angeben.

-   Die Start- und Stoppzeiten relativ zur Zeitachse. Rufen Sie [**die IAMTimelineObj::SetStartStop-Methode**](iamtimelineobj-setstartstop.md) auf.
-   Die Mediendatei, die als Quelle verwendet werden soll. Rufen Sie [**die IAMTimelineSrc::SetMediaName-Methode**](iamtimelinesrc-setmedianame.md) mit einer Breitzeichenfolge auf, die den Namen der Datei darstellt.
-   Die Start- und Stoppzeiten der Medien, die relativ zur ursprünglichen Datei sind. Rufen Sie [**die IAMTimelineSrc::SetMediaTimes-Methode**](iamtimelinesrc-setmediatimes.md) auf. Weitere Informationen zu Medienzeiten finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Im folgenden Beispiel beginnt der Quellclip vier Sekunden in der Datei. Die Mediendauer beträgt 10 Sekunden, also doppelt so lange wie die Zeitachse, was bedeutet, dass die Quelle mit doppelt normaler Geschwindigkeit abspielt. Die Konstante UNITS ist als 100000000 (10^7) definiert und entspricht einer Sekunde.


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> Derzeit kann DES nicht mehr als 75 Quellen gleichzeitig rendern, die mit VCM-Codecs (Video Compression Manager) komprimiert wurden. Wenn das Projekt als Ganzes mehr als 75 solcher Quellen enthält, müssen Sie die dynamische Wiederherstellungsverbindung verwenden, oder DES kann keine Vorschau des Projekts anzeigen. Weitere Informationen finden Sie unter [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

 

Weitere Informationen zu Quellen finden Sie unter [Arbeiten mit Quellen.](working-with-sources.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 



