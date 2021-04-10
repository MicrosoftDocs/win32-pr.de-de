---
description: In Direct3D werden alle zweidimensionalen (2D) Bilder durch einen linearen Bereich von Speicher dargestellt, der als Oberfläche bezeichnet wird.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Oberflächen Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124813"
---
# <a name="surface-formats-direct3d-9"></a>Oberflächen Formate (Direct3D 9)

In Direct3D werden alle zweidimensionalen (2D) Bilder durch einen linearen Bereich von Speicher dargestellt, der als Oberfläche bezeichnet wird. Eine Oberfläche kann als 2D-Array betrachtet werden, wobei jedes Element einen Farbwert enthält, der einen kleinen Abschnitt des Bilds darstellt, der als Pixel bezeichnet wird. Die Detailebene eines Bilds wird sowohl durch die Anzahl der Pixel, die zum Darstellen des Bilds benötigt werden, als auch durch die Anzahl der Bits definiert, die für das Farbspektrum des Bilds benötigt werden. Beispielsweise wird ein Bild, das 800 Pixel breit und 600 Pixel hoch und 32 Bits Farben für jedes Pixel ist (als 800x600x32 geschrieben), ausführlicher als ein Bild mit einer Breite 480 von 640 Pixel und einer Höhe von jeweils 16 Bits pro Pixel (als 640 x480x16 geschrieben) dargestellt. Entsprechend ist für das ausführlichere Bild eine größere Oberfläche erforderlich, um die Daten zu speichern. Bei einem 800x600x32-Bild sind die Array Dimensionen der Oberfläche 800x600, und jedes Element enthält einen 32-Bit-Wert, der seine Farbe darstellt.

Alle Oberflächen verfügen über eine Größe und speichern eine bestimmte Anzahl von Bits, die Farbe darstellen. Die Bits, die die Farbe darstellen, werden in einzelne Farbelemente aufgeteilt: rot, grün und blau. In Direct3D werden alle Color-Elemente durch den [D3DFORMAT](d3dformat.md) -enumerierten Typ definiert. Ein Direct3D-Farb Format wird in die Anzahl der für die einzelnen Farben reservierten Byes aufgeteilt. Beispielsweise wird ein 16-Bit-Farb Format in Direct3D als D3DFMT \_ R5G6B5 definiert, wobei 5 Bits für Rot (R), 6 Bits für Grün (G) und 5 Bits für blau (B) reserviert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 



