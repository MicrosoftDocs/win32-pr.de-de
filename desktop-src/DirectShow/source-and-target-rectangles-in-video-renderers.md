---
description: Quell- und Zielrechtecke in Videorenderern
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Quell- und Zielrechtecke in Videorenderern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020be0786a071c6bbdf33649405517ed3788789268052b61ee89d97a23f357f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072544"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Quell- und Zielrechtecke in Videorenderern

Es gibt drei Größen in den [**Formatstrukturen VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) von Videomedientypen. In diesem Artikel wird erläutert, was sie sind und wie sie funktionieren.

Erstens gibt es eine Größe im **bmiHeader-Member** dieser Strukturen. Das **bmiHeader-Element** ist eine [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) mit eigenen Breiten- und Höhenmitgliedern, **bmiHeader.biWidth** und **bmiHeader.biHeight.**

Zweitens gibt es ein Rechteck im **rcSource-Member** dieser Strukturen. und schließlich gibt es ein Rechteck im **rcTarget-Member** dieser Strukturen.

Angenommen, Sie haben zwei Filter, A und B, und diese Filter sind mit einem bestimmten Videomedientyp miteinander verbunden (A links oder upstream und B rechts oder downstream).

Die Puffer, die zwischen den Filtern A und B übergeben werden, haben die Größe (**bmiHeader.biWidth**, **bmiHeader.biHeight**). Filter A sollte einen Teil seines Eingabevideos, das von **rcSource** bestimmt wird, übernehmen und das Video strecken, um den **rcTarget-Teil** des Puffers zu füllen. Der zu verwendende Teil des Eingabevideos basiert darauf, wie **rcSource** mit der Größe (**biWidth**, **biHeight**) des Medientyps verglichen wird, mit dem A und B ursprünglich verbunden wurden. Wenn **rcSource** leer ist, verwendet Filter A das gesamte Eingabevideo. Wenn **rcTarget** leer ist, füllt Filter A den gesamten Ausgabepuffer aus.

Angenommen, Filter A empfängt Videodaten von 160 x 120 Pixeln. Gehen Sie auch davon aus, dass Filter A mit Filter B mit dem folgenden Medientyp verbunden ist.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rcTarget**: (0, 0, 0, 0)

Dies bedeutet, dass Filter A das empfangene Video in x- und y-Richtung um 2 streckt und einen 320 x 240-Ausgabepuffer füllt.

Angenommen, Filter A empfängt 160 x 120 Videodaten und ist mit filter B mit dem folgenden Medientyp verbunden.

-   (**biWidth**, **biHeight**): 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rcTarget**: (0, 0, 0, 0)

Der **rcSource-Member** ist relativ zur verbundenen Puffergröße von 320, 240. Da die angegebene **rcSource** (0, 0, 160, 240) ist die linke Hälfte des Puffers, Filter A nimmt die linke Hälfte des Eingabevideos oder (0, 0, 80, 120) und streckt das Video auf eine Größe von (320, 240) (um 4 in x-Richtung und um 2 in y-Richtung) und füllt den Ausgabepuffer 320 x 240 auf.

Angenommen, filter A ruft [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md)auf, und dem zurückgegebenen Medienbeispiel ist ein Medientyp angefügt. Dies bedeutet, dass Filter B filter A eine andere Größe oder Art von Video bereitstellen möchte als zuvor. Angenommen, der neue Medientyp ist:

-   (**biWidth**, **biHeight**): 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rcTarget**: (0, 0, 80, 60)

Dies bedeutet, dass das Medienbeispiel über einen Puffer mit einer Größe von 640 x 480 verfügt. Der **rcSource-Member** ist relativ zum ursprünglichen verbundenen Medientyp (320, 240) und nicht zum neuen Medientyp (640, 480). Daher gibt **rcSource** an, dass die linke obere Ecke (25 %) des Eingabevideos verwendet werden soll. Dieser Teil des Eingabevideos wird in der linken oberen Ecke (80, 60) Pixel des 640 x 480-Ausgabepuffers platziert, wie von **rcTarget** von (0, 0, 80, 60) angegeben. Da Filter A 160 x 120 Videos empfängt, ist die linke obere Ecke des Eingabevideos ein Teil (80, 60), die gleiche Größe der Ausgabebitmap, und es ist kein Stretching erforderlich.

Filter A platzieren keine Daten in den anderen Pixeln des Ausgabepuffers und lassen diese Bits unverändert. Das **rcSource-Member** wird durch **die biWidth-** und biHeight-Klasse des ursprünglichen verbundenen Medientyps zwischen den Filtern A und B und **rcTarget** durch die neuen **biWidth-** und **biHeight-Typen** des Medienbeispiels gebunden.  Im vorherigen Beispiel konnte **rcSource** die Grenzen von (0, 0, 320, 240) nicht überschreiten, und **rcTarget** konnte die Grenzen von (0, 0, 640, 480) nicht überschreiten.

 

 



