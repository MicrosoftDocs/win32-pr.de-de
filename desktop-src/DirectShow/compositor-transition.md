---
description: Compositorübergang
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Compositorübergang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566272"
---
# <a name="compositor-transition"></a>Compositorübergang

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der Compositor-Übergang setzt ein unter Rechteck aus dem Vordergrund in ein bestimmtes Rechteck im Hintergrund zusammen, ohne den Rest des Hintergrunds zu ändern. Verwenden Sie diesen Übergang, um Effekte im Bildschirm oder Bild in Bildern zu erstellen.

In der folgenden Abbildung ist der compositorübergang dargestellt:

![compositorübergang](images/trans-compositor.png)

Klassen-ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

CLSID-Variablen Name: CLSID \_ dxtcompositor

Anzeige Name: "dxtcompositor"

Eigenschaften



| Eigenschaft   | type | Standard | BESCHREIBUNG                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Höhe     | long | 0       | Höhe des Ziel Rechtecks in Pixel.                     |
| OffsetX    | long | 0       | Horizontaler Offset des Ziel Rechtecks in Pixel.          |
| OffsetY    | long | 0       | Vertikaler Offset des Ziel Rechtecks in Pixel.            |
| SrcHeight  | long | 0       | Die Höhe des unter Rechtecks in der Quelle in Pixel.       |
| Srcoffsetx | long | 0       | Die x-Koordinate des unter Rechtecks in der Quelle in Pixel. |
| Srcoff-Ty | long | 0       | Die y-Koordinate des unter Rechtecks in der Quelle in Pixel. |
| SrcWidth   | long | 0       | Die Breite des unter Rechtecks in der Quelle in Pixel.        |
| Breite      | long | 0       | Breite des Ziel Rechtecks in Pixel.                      |



 

Diese Eigenschaften werden im folgenden Diagramm veranschaulicht:

![Compositor-Eigenschaften](images/compmeasure.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übergänge und Effekte](transitions-and-effects.md)
</dt> </dl>

 

 



