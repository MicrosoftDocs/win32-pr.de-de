---
description: Direct3D wendet die folgenden Formeln auf die DU- und DV-Komponenten in jedem Bumpmappixel an.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Formeln für die Bumpzuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035a28966c841f7d593cb46c7c7d969f7b2addaacb6cf43e25ceebdca83ff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805855"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Formeln für die Bumpzuordnung (Direct3D 9)

Direct3D wendet die folgenden Formeln auf die D<sub>U-</sub> und D<sub>V-Komponenten</sub> in jedem Bumpmappixel an.

![Formeln von Matrixtransformationen für die Bumpzuordnung](images/dudv-transform.png)

In diesen Formeln werden die Variablen D<sub>U</sub> und D<sub>V</sub> direkt aus einem Bumpmappixel übernommen und von einer 2x2-Matrix transformiert, um die Ausgabedeltawerte D<sub>U</sub>' und D<sub>V</sub>' zu erzeugen. Das System verwendet die Ausgabewerte, um die Texturkoordinaten zu ändern, die die Umgebungskarte in der nächsten Texturphase adressieren. Die Koeffizienten der Transformationsmatrix werden über die Texturphasenzustände D3DTSS \_ BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 und D3DTSS \_ BUMPENVMAT11 festgelegt.

Zusätzlich zu den Deltawerten "you" und "v" kann das System einen Leuchtdichtewert berechnen, der verwendet wird, um die Farbe der Umgebungszuordnung in der nächsten Mischungsphase zu modulieren, wie in der folgenden Formel gezeigt.

![Formel für ausgabedominanz, berechnet aus Skalierungsfaktor und Offset](images/l-transform.png)

In dieser Formel ist L' die Ausgabe-Luminanz, die berechnet wird. Die L-Variable ist der Leuchtdichtewert, der aus einem Bumpmappixel übernommen wird, der mit dem Skalierungsfaktor, S und Offset mit dem Wert in der Variablen O multipliziert wird. Die Texturphasenzustände D3DTSS \_ BUMPENVLSCALE und D3DTSS BUMPENVLOFFSET steuern die Werte für die \_ Variablen S und O in der Formel. Diese Formel wird nur angewendet, wenn der Texturmischungsvorgang für die Phase, die die Bumpmap enthält, auf D3DTOP \_ BUMPENVMAPLUMINANCE festgelegt ist. Bei Verwendung von D3DTOP BUMPENVMAP verwendet das System den Wert \_ 1,0 für L'.

Nach dem Berechnen der Ausgabedeltawerte D<sub>U</sub>' und D<sub>V</sub>' fügt das System sie den Texturkoordinaten in der nächsten Texturphase hinzu und moduliert die ausgewählte Farbe durch die Leuchtdichte, um die auf das Polygon angewendete Farbe zu erzeugen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bump-Zuordnung](bump-mapping.md)
</dt> </dl>

 

 



