---
description: Arbeiten mit Videoframes
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Arbeiten mit Videoframes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86407f99138e0b38b67468668fc963bd1bcd7b65e875571643bc7727b4d0d339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870930"
---
# <a name="working-with-video-frames"></a>Arbeiten mit Videoframes

Unkomprimiertes Video ist eine Sequenz von Bitmaps, die in schneller Folge abgespielt werden, in der Regel mit einer Rate von ca. 30 Bildern pro Sekunde. Da die meisten Videos in einem komprimierten Format in ein DirectShow-Filterdiagramm übertragen werden, durchläuft der Videostream in der Regel einen Decoder für die Dekomprimierung. Viele Decoder geben Daten im YUV-Format aus und lassen die endgültige Konvertierung in RGB für die Videohardware direkt vor dem Rendering erhalten. Wenn ein Decoder die DirectX-Videobeschleunigung verwendet, führt die Videohardware zusätzliche Aufgaben aus, um das Bild zu decodieren. Daher kann die endgültige Dekomprimierung der Bitmaps erst durchgeführt werden, wenn die Daten die Videohardware erreichen.

Um jedoch viele Arten von Videoanalyse, -verarbeitung oder -bearbeitung durchzuführen, ist es häufig erforderlich, mit unkomprimierten Bitmaps in einem RGB- oder YUV-Format zu arbeiten, bevor sie gerendert oder in eine Datei geschrieben werden. Diese Arbeit erfolgt in der Regel innerhalb eines Transformationsfilters, der auf der [**CTransformFilter-Basisklasse**](ctransformfilter.md) basiert, insbesondere in der **Transform-Methode.** Diese Methode empfängt einen Zeiger auf ein [**IMediaSample-Objekt,**](/windows/desktop/api/Strmif/nn-strmif-imediasample) das die Videodaten kapselt. Die **IMediaSample::GetPointer-Methode** gibt einen Zeiger auf das erste Byte der Rohdaten zurück. Bei unkomprimierten Frames bestehen diese Daten aus Pixeln, auf die direkt vom Filter zugegriffen oder geändert werden kann. Die folgenden Abschnitte enthalten Hintergrundinformationen, die Ihnen helfen, auf diese Weise effektiv mit DIB-Daten zu arbeiten.

> [!Note]  
> Sie können die Bits auch mithilfe der GDI-, GDI+-, DirectDraw- oder Direct3D-Funktionen ändern, aber diese Techniken gehen über den Rahmen dieses Artikels hinaus.

 

Dieser Abschnitt enthält die folgenden Themen:

-   [Von oben nach unten im Vergleich zu Bottom-Up DIBs](top-down-vs--bottom-up-dibs.md)
-   [Arbeiten mit 16-Bit-RGB](working-with-16-bit-rgb.md)

 

 



