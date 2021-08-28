---
description: Compositor-Übergang
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Compositor-Übergang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763194308ea01a31e132aebccdfca84f06dae56e9c01b47c689b03215cdb2698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084294"
---
# <a name="compositor-transition"></a>Compositor-Übergang

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Der Compositor-Übergang zusammengesetzt einen Unterordngle aus dem Vordergrund in ein bestimmtes Rechteck im Hintergrund, ohne den Rest des Hintergrunds zu ändern. Verwenden Sie diesen Übergang, um Split-Screen- oder Picture-in-Picture-Effekte zu erstellen.

Die folgende Abbildung zeigt den Compositorübergang:

![Compositorübergang](images/trans-compositor.png)

Klassen-ID (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

CLSID-Variablenname: CLSID \_ DxtCompositor

Name der Beschriftung: "DxtCompositor"

Eigenschaften



| Eigenschaft   | type | Standard | BESCHREIBUNG                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Height     | long | 0       | Höhe des Zielrechtecks in Pixel.                     |
| OffsetX    | long | 0       | Horizontaler Offset des Zielrechtecks in Pixel.          |
| OffsetY    | long | 0       | Vertikaler Offset des Zielrechtecks in Pixel.            |
| SrcHeight  | long | 0       | Die Höhe des UntergeordnetenRectangles auf der Quelle in Pixel.       |
| SrcOffsetX | long | 0       | Die x-Koordinate des Subrekttangles auf der Quelle in Pixel. |
| SrcOffsetY | long | 0       | Die y-Koordinate des Subrectangles auf der Quelle in Pixel. |
| SrcWidth   | long | 0       | Die Breite des UntergeordnetenRectangles auf der Quelle in Pixel.        |
| Width      | long | 0       | Breite des Zielrechtecks in Pixel.                      |



 

Das folgende Diagramm veranschaulicht diese Eigenschaften:

![Compositoreigenschaften](images/compmeasure.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übergänge und Effekte](transitions-and-effects.md)
</dt> </dl>

 

 



