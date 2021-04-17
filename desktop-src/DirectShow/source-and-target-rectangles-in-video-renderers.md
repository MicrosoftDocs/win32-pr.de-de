---
description: Quell-und Ziel Rechtecke in Videorenderer
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: Quell-und Ziel Rechtecke in Videorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556aea6aad22e5ea6df61c74ed0a46d2e3984d67
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521872"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a>Quell-und Ziel Rechtecke in Videorenderer

Es gibt drei Größen in den Video Medientypen [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo), [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format. In diesem Artikel wird erläutert, was Sie sind und wie Sie funktionieren.

Zuerst gibt es eine Größe im **bmiheader** -Member dieser Strukturen. Der **bmiheader** -Member ist eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur mit eigenen Width-und Height-Elementen, **bmiheader. biwidth** und **bmiheader. biheight**.

Zweitens gibt es ein Rechteck im **rcSource** -Member dieser Strukturen. und zuletzt ist ein Rechteck im **rctarget** -Member dieser Strukturen vorhanden.

Angenommen, Sie verfügen über zwei Filter: a und b, und diese Filter sind miteinander verbunden (ein auf der linken Seite, ein Upstream und b auf der rechten oder nach unten) mit einem bestimmten Video Medientyp.

Die Puffer, die zwischen den Filtern A und B bestehen, haben die Größe (**bmiheader. biwidth**, **bmiheader. biheight**). Filter a sollte einen Teil des von **rcSource** ermittelten Eingabe Videos annehmen und dieses Video so Strecken, dass der **rctarget** -Teil des Puffers ausgefüllt wird. Der Teil des zu verwendenden Eingabe Videos basiert darauf, wie **rcSource** mit der Größe (**biwidth**, **biheight**) des Medientyps vergleicht, der einen filtert, und B, der ursprünglich mit verbunden war. Wenn **rcSource** leer ist, verwendet Filter A das gesamte Eingabe Video. Wenn **rctarget** leer ist, füllt Filter A den gesamten Ausgabepuffer aus.

Nehmen Sie beispielsweise an, dass Filter A Videodaten empfängt, die 160 x 120 Pixel betragen. Nehmen Sie auch an, dass Filter a mit Filter B mit dem folgenden Medientyp verbunden ist.

-   (**biwidth**, **biheight**): 320, 240
-   **rcSource**: (0, 0, 0, 0)
-   **rctarget**: (0,0, 0,0)

Dies bedeutet, dass Filter A das empfangene Video in der x-und der y-Richtung um 2 ausdehnt und einen 320 x 240-Ausgabepuffer ausfüllen soll.

Nehmen wir als weiteres Beispiel an, dass Filter A 160 x 120-Videodaten empfängt und dass es mit Filter B mit dem folgenden Medientyp verbunden ist.

-   (**biwidth**, **biheight**): 320, 240
-   **rcSource**: (0, 0, 160, 240)
-   **rctarget**: (0,0, 0,0)

Der **rcSource** -Member ist relativ zur verbundenen Puffergröße von 320, 240. Da die angegebene **rcSource** (0, 0, 160, 240) ist die linke Hälfte des Puffers, der Filter A nimmt die linke Hälfte des Eingabe Videos oder den (0,0) Teil (0, 0, 80, 120) und streckert das Video auf eine Größe von (320, 240) (4 in der x-Richtung und 2 in der y-Richtung) und füllt den 320 x 240-Ausgabepuffer auf.

Nehmen Sie nun an, dass Filter a [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md)aufruft und dem zurückgegebenen Medien Beispiel ein Medientyp zugeordnet ist. Dies bedeutet, dass Filter B einen filtern muss, um eine andere Größe oder Art von Video als zuvor bereitzustellen. Angenommen, der neue Medientyp lautet:

-   (**biwidth**, **biheight**): 640, 480
-   **rcSource**: (0, 0, 160, 120)
-   **rctarget**: (0, 0, 80, 60)

Dies bedeutet, dass das Medien Beispiel über einen Puffer mit einer Größe von 640 x 480 verfügt. Der **rcSource** -Member ist relativ zum ursprünglichen verbundenen Medientyp (320, 240), nicht zum neuen Medientyp von (640, 480), weshalb **rcSource** angibt, dass die obere linke Ecke (25%) ist. der Eingabe Video muss verwendet werden. Dieser Teil des Eingabe Videos wird in der linken oberen Ecke (80, 60) des Ausgabepuffers 640 x 480 platziert, wie von **rctarget** von (0, 0, 80, 60) angegeben. Da Filter A 160 x 120-Videos empfängt, ist die linke obere Ecke des Eingabe Videos ein (80, 60) Stück, dieselbe Größe der Ausgabe Bitmap, und es ist keine Streckung erforderlich.

Filter A fügt keine Daten in den anderen Pixeln des Ausgabepuffers ein und lässt diese Bits unverändert. Der **rcSource** -Member wird durch die **biwidth** und die **biheight** des ursprünglichen verbundenen Medientyps zwischen den Filtern A und B und **rctarget** von der neuen **biwidth** und **biheight** des Medien Beispiels begrenzt. Im vorherigen Beispiel konnte **rcSource** nicht außerhalb der Grenzen von (0, 0, 320, 240) liegen, und **rctarget** konnte nicht außerhalb der Grenzen von (0, 0, 640, 480) liegen.

 

 



