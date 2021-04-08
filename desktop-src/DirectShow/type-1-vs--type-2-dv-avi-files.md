---
description: Geben Sie-1 im Vergleich zu
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Type-1 im Vergleich zu Type-2 DV AVI-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959939"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a>Type-1 im Vergleich zu Type-2 DV AVI-Dateien

DV-Kameras liefern überlappende Audiovideo. jeder Frame des Videos enthält auch die Audioinformationen. Wenn Sie DV-Daten in einer AVI-Datei speichern, haben Sie folgende Möglichkeiten:

-   Speichern Sie die verschachtelten Daten als einen Datenstrom in der AVI-Datei. Dies wird als Type-1-Datei bezeichnet.
-   Teilen Sie die verschachtelten Daten in separate Audiodaten und Videostreams auf. Dies wird als Type-2-Datei bezeichnet.

Bei der Video Erfassung, bei der der maximale Durchsatz entscheidend ist, ist es besser, eine Type-1-Datei zu verwenden, da Type-2-Dateien redundante Audiodaten enthalten. (Der Videostream enthält immer noch die Audiodaten. Die Audiodaten werden einfach ausgeblendet, indem der Stream als Video gekennzeichnet wird.) Außerdem erfordert das Schreiben einer Type-2-Datei eine zusätzliche Prozessorzeit, um den verschachtelten Stream aufzuteilen.

Allerdings sind Typ-1-Dateien für die Echtzeitbearbeitung weniger effizient. Die Anwendung muss die Audiodatei aus dem überlappenden Datenstrom extrahieren, die Änderungen vornehmen und die Daten erneut interaktivieren. Außerdem ist das Type-1-Format nicht mit Microsoft® Video für Windows® (Vfw) kompatibel. DirectShow kann beide Dateitypen verarbeiten.

Eine Type-2-Datei kann mit dem [DV-Muxer](dv-muxer-filter.md) -Filter in Typ-1 konvertiert werden. Eine Type-1-Datei kann mit dem [DV-Splitter](dv-splitter-filter.md) Filter in Typ-2 konvertiert werden. Das folgende Diagramm veranschaulicht den Unterschied zwischen den beiden Formaten.

![Konvertierung zwischen Typ-1 und Typ-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DV-Daten im AVI-Datei Format](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



