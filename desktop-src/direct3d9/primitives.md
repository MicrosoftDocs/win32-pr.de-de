---
description: Ein 3D-Primitiv ist eine Sammlung von Scheitelungen, die eine einzelne 3D-Entität bilden. Das einfachste Primitive ist eine Sammlung von Punkten in einem 3D-Koordinatensystem, das als Punktliste bezeichnet wird.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitive (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af846ded9798a25238287be7dd017dcf6efecdfb2976723638881c7e00f9642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092561"
---
# <a name="primitives-direct3d-9-graphics"></a>Primitive (Direct3D 9-Grafiken)

Ein 3D-Primitiv ist eine Sammlung von Scheitelungen, die eine einzelne 3D-Entität bilden. Das einfachste Primitive ist eine Sammlung von Punkten in einem 3D-Koordinatensystem, das als Punktliste bezeichnet wird.

Häufig sind 3D-Primitive Polygone. Ein Polygon ist eine geschlossene 3D-Abbildung, die durch mindestens drei Scheitelungen umgrenzt ist. Das einfachste Polygon ist ein Dreieck. Microsoft Direct3D verwendet Dreiecke, um die meisten Polygone zu bilden, da alle drei Scheitelstriche in einem Dreieck garantiert koplanar sind. Das Rendern nichtplanarer Scheitelungen ist ineffizient. Sie können Dreiecke kombinieren, um große, komplexe Polygone und Gitternetze zu bilden.

Die folgende Abbildung zeigt einen Cube. Zwei Dreiecke bilden jedes Gesicht des Cubes. Der gesamte Satz von Dreiecken bildet ein kubisches Primitiv. Sie können Texturen und Materialien auf die Oberflächen von Primitiven anwenden, damit sie als einzelne Vollbildform erscheinen. Weitere Informationen finden Sie unter [Materialien (Direct3D 9)](materials.md) und [Direct3D-Texturen (Direct3D 9).](direct3d-textures.md)

![Abbildung eines Würfels mit zwei Dreiecken auf jedem Gesicht](images/cube3d.png)

Sie können auch Dreiecke verwenden, um Primitive zu erstellen, deren Oberflächen wie weiche Kurven erscheinen. Die folgende Abbildung zeigt, wie eine Kugel mit Dreiecken simuliert werden kann. Nachdem ein Material angewendet wurde, sieht die Kugel gekrümmt aus, wenn sie gerendert wird. Dies gilt insbesondere, wenn Sie Gouraud Shading verwenden. Weitere Informationen finden Sie unter [Gouraud Shading](shading-modes.md).

![Abbildung einer Kugel, die mithilfe von Dreiecken simuliert wird](images/sphere3d.png)

Direct3D-Geräte können die folgenden Typen von Primitiven erstellen und bearbeiten.

-   [Punktlisten](point-lists.md)
-   [Zeilenlisten](line-lists.md)
-   [Linienstreifen](line-strips.md)
-   [Dreieckslisten](triangle-lists.md)
-   [Dreiecksstreifen](triangle-strips.md)
-   [Dreiecks-Lüfter (Direct3D 9)](triangle-fans.md)

Sie können primitive Typen aus einer C++-Anwendung mit einer der Renderingmethoden der [**IDirect3DDevice9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) rendern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
