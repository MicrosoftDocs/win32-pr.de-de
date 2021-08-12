---
description: In Direct3D werden alle zweidimensionalen Bilder (2D) durch einen linearen Speicherbereich dargestellt, der als Oberfläche bezeichnet wird.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Oberflächenformate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e54b6bf4573243e170f089a72d7d5c69e31c81a536703d764694d43f2dc33cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291497"
---
# <a name="surface-formats-direct3d-9"></a>Oberflächenformate (Direct3D 9)

In Direct3D werden alle zweidimensionalen Bilder (2D) durch einen linearen Speicherbereich dargestellt, der als Oberfläche bezeichnet wird. Eine Oberfläche kann als 2D-Array bezeichnet werden, in dem jedes Element einen Farbwert enthält, der einen kleinen Teil des Bilds darstellt, der als Pixel bezeichnet wird. Die Detailebene eines Bilds wird sowohl durch die Anzahl der Pixel definiert, die zum Darstellen des Bilds erforderlich sind, als auch durch die Anzahl der Bits, die für das Farbspektrum des Bilds benötigt werden. Ein Bild mit einer Breite von 800 Pixeln und einer Höhe von 600 Pixeln mit 32 Farbbits für jedes Pixel (geschrieben als 800 x 600 x 32) ist beispielsweise detaillierter als ein Bild, das 640 Pixel breit und 480 Pixel groß ist und 16 Bit Farbe für jedes Pixel hat (geschrieben als 640 x 480 x 16). Ebenso erfordert das detailliertere Bild eine größere Oberfläche zum Speichern der Daten. Bei einem 800x600x32-Bild sind die Arraydimensionen der Oberfläche 800 x 600, und jedes Element enthält einen 32-Bit-Wert, um seine Farbe zu darstellen.

Alle Oberflächen haben eine Größe und speichern eine bestimmte Anzahl von Bits, die farbe darstellen. Die Bits, die die Farbe darstellen, werden in einzelne Farbelemente getrennt: Rot, Grün und Blau. In Direct3D werden alle Farbelemente durch den [aufzählten D3DFORMAT-Typ](d3dformat.md) definiert. Ein Direct3D-Farbformat wird in die Anzahl der byes aufgeschlüsselt, die für jede Farbe reserviert sind. Beispielsweise wird ein 16-Bit-Farbformat in Direct3D als D3DFMT R5G6B5 definiert, wobei 5 Bits für Rot (R), 6 Bits für Grün (G) und 5 Bits für Blau \_ (B) reserviert sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 



