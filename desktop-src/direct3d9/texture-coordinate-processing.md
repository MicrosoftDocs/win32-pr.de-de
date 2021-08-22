---
description: Das folgende Diagramm zeigt den Pfad, der von den Texturkoordinaten von der Quelle, über die Verarbeitung und zum Rasterizer genommen wird.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Texturkoordinatenverarbeitung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5a002e7171f97ab60c0af3cd5e8228cb8222ba70b8e718f2d93c28cebf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044223"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Texturkoordinatenverarbeitung (Direct3D 9)

Das folgende Diagramm zeigt den Pfad, der von den Texturkoordinaten von der Quelle, über die Verarbeitung und zum Rasterizer genommen wird.

![Diagramm des Pfads für Texturkoordinaten von einer Quelle zum Rasterizer](images/tex-processing.png)

Es gibt zwei Quellen, aus denen das System Texturkoordinaten zeichnen kann. Für eine bestimmte Texturphase können Sie Texturkoordinaten verwenden, die im Scheitelpunktformat (D3DFVF \_ TEX1 bis D3DFVF \_ TEX8) enthalten sind, oder Sie können Texturkoordinaten verwenden, die automatisch von Direct3D generiert werden. Weitere Informationen zum letzteren Fall finden Sie unter [Automatisch generierte Texturkoordinaten (Direct3D 9).](automatically-generated-texture-coordinates.md) Wenn der Texturphasenzustand D3DTSS \_ TEXTURETRANSFORMFLAGS für die aktuelle Texturphase auf D3DTTFF \_ DISABLE (Standardeinstellung) festgelegt ist, werden Eingabekoordinaten nicht transformiert. Wenn D3DTSS \_ TEXTURETRANSFORMFLAGS> auf einen anderen Wert festgelegt ist, wird die Transformationsmatrix für diese Phase auf die Eingabekoordinaten angewendet.

Der [**D3DTEXTURETRANSFORMFLAGS-Enumerationstyp**](./d3dtexturetransformflags.md) definiert gültige Werte für den Texturphasenzustand D3DTSS \_ TEXTURETRANSFORMFLAGS. Mit Ausnahme des D3DTTFF \_ DISABLE-Flags, das die Texturkoordinatentransformation umgeht, konfigurieren die in dieser Enumeration definierten Werte die Anzahl der Ausgabekoordinaten, die das System an den Rasterizer übergibt. Die Flags D3DTTFF \_ COUNT1 bis D3DTTFF \_ COUNT4 weisen das System an, ein, zwei, drei oder vier Elemente aus den Ausgabekoordinaten an den Rasterizer zu übergeben.

Das D3DTTFF \_ PROJECTED-Flag ist etwas Besonderes: Es teilt dem System mit, dass die Texturkoordinaten für eine projizierte Textur vorgesehen sind. Kombinieren Sie das D3DTTFF \_ PROJECTED-Flag mit einem anderen Member von [**D3DTEXTURETRANSFORMFLAGS,**](./d3dtexturetransformflags.md) um den Rasterizer anzuweisen, alle Elemente vor der Rasterung durch das letzte Element zu teilen. Wenn Sie beispielsweise explizit Texturkoordinaten mit drei Elementen verwenden oder die Transformation zu einer Texturkoordinate mit drei Elementen führt, können Sie die Flags D3DTTFF \_ COUNT3 und D3DTTFF \_ PROJECTED kombinieren, damit der Rasterizer die ersten beiden Elemente durch die letzten dividiert, wodurch 2D-Texturkoordinaten erzeugt werden, die zum Adressieren einer 2D-Textur erforderlich sind.

> [!Note]  
> Mit Ausnahme von kubischen Umgebungszuordnungen und Volumentexturen können Rasterizer Texturen nicht mithilfe von Texturkoordinaten mit mehr als zwei Elementen adressieren. Wenn Sie mehr Elemente angeben, als zum Adressieren der aktuellen Textur für diese Phase verwendet werden können, werden die überflüssigen Elemente ignoriert. Dies gilt auch bei Verwendung von 2D-Texturkoordinaten für eine 1D-Textur.

 

Weitere Informationen finden Sie in den folgenden Themen.

-   [Automatisch generierte Texturkoordinaten (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Transformationen für Texturkoordinaten (Direct3D 9)](texture-coordinate-transformations.md)
-   [Sondereffekte (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinaten](texture-coordinates.md)
</dt> </dl>

 

 
