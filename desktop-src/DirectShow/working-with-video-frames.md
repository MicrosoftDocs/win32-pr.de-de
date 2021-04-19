---
description: Arbeiten mit Video Frames
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Arbeiten mit Video Frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356215"
---
# <a name="working-with-video-frames"></a>Arbeiten mit Video Frames

Unkomprimiertes Video ist eine Sequenz von Bitmaps, die in schneller Folge abgespielt werden, in der Regel mit einer Rate von ungefähr 30 Frames pro Sekunde. Da in den meisten Videos ein DirectShow-Filter Diagramm in einem komprimierten Format eingegeben wird, durchläuft der Videostream in der Regel einen Decoder zur Dekomprimierung. Viele Decoder geben Daten in einem YUV-Format aus und belassen die endgültige Konvertierung für die Video Hardware direkt vor dem Rendering in RGB. Wenn ein Decoder eine DirectX-Videobeschleunigung verwendet, führt die Video Hardware zusätzliche Arbeit aus, um das Bild zu decodieren. Folglich wird die endgültige decokomprimierung der Bitmaps möglicherweise erst ausgeführt, wenn die Daten die Video Hardware erreichen.

Um jedoch viele Arten der Videoanalyse,-Verarbeitung oder-Bearbeitung auszuführen, ist es oft notwendig, in einem Typ des RGB-oder YUV-Formats an unkomprimierten Bitmaps zu arbeiten, bevor Sie gerendert oder in eine Datei geschrieben werden. Diese Arbeit erfolgt in der Regel in einem Transformations Filter, der auf der [**ctransformfilter**](ctransformfilter.md) -Basisklasse basiert, insbesondere in der **Transformations** Methode. Diese Methode empfängt einen Zeiger auf ein [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Objekt, das die Videodaten kapselt. Die **imediasample:: getpointer** -Methode gibt einen Zeiger auf das erste Byte der Rohdaten zurück. Bei nicht komprimierten Frames bestehen diese Daten aus Pixeln, die direkt durch den Filter aufgerufen oder geändert werden können. In den folgenden Abschnitten finden Sie Hintergrundinformationen, die Ihnen helfen, auf diese Weise mit DIB-Daten effektiv zu arbeiten.

> [!Note]  
> Sie können die Bits auch mithilfe von GDI-, GDI+-, DirectDraw-oder Direct3D-Funktionen ändern, aber diese Techniken gehen über den Rahmen dieses Artikels hinaus.

 

Dieser Abschnitt enthält die folgenden Themen:

-   [Top-Down-und Bottom-Up Disb](top-down-vs--bottom-up-dibs.md)
-   [Arbeiten mit 16-Bit-RGB](working-with-16-bit-rgb.md)

 

 



