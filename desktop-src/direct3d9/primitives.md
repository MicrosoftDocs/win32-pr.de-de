---
description: Ein 3D-primitiv ist eine Sammlung von Vertices, die eine einzelne 3D-Entität bilden. Das einfachste primitive ist eine Auflistung von Punkten in einem 3D-Koordinatensystem, das als Punkt Liste bezeichnet wird.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitive (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123433"
---
# <a name="primitives-direct3d-9-graphics"></a>Primitive (Direct3D 9-Grafiken)

Ein 3D-primitiv ist eine Sammlung von Vertices, die eine einzelne 3D-Entität bilden. Das einfachste primitive ist eine Auflistung von Punkten in einem 3D-Koordinatensystem, das als Punkt Liste bezeichnet wird.

Häufig sind 3D-primitive Polygone. Ein Polygon ist eine geschlossene 3D-Abbildung, die durch mindestens drei Vertices getrennt ist. Das einfachste Polygon ist ein Dreieck. Microsoft Direct3D verwendet Dreiecke, um die meisten Polygone zu verfassen, da alle drei Scheitel Punkte in einem Dreieck vollständig Coplanar sind. Das Rendern von nicht planaren Vertices ist ineffizient. Dreiecke können kombiniert werden, um große, komplexe Polygone und Netze zu bilden.

In der folgenden Abbildung ist ein Cube dargestellt. Zwei Dreiecke bilden jedes Gesicht des Cubes. Der gesamte Satz von Dreiecken bildet einen kubischen primitiven. Sie können Texturen und Materialien auf die Oberflächen von primitiven anwenden, damit Sie als ein einzelnes voll solides Formular angezeigt werden. Weitere Informationen finden Sie unter [Material (Direct3D 9)](materials.md) and [Direct3D Texturen (Direct3D 9)](direct3d-textures.md).

![Abbildung eines Cubes mit zwei Dreiecken auf jeder Seite](images/cube3d.png)

Sie können auch Dreiecke verwenden, um primitive zu erstellen, deren Oberflächen als glatte Kurven angezeigt werden. In der folgenden Abbildung wird gezeigt, wie eine Kugel mit Dreiecken simuliert werden kann. Nachdem ein Material angewendet wurde, wird die Kugel beim Rendern gerendert. Dies gilt insbesondere, wenn Sie die Verwendung von Gouraud-Schattierung verwenden. Weitere Informationen finden Sie unter [Gouraud-Schattierung](shading-modes.md).

![Abbildung einer Kugel, die mithilfe von Dreiecken simuliert wird](images/sphere3d.png)

Direct3D-Geräte können die folgenden Typen von primitiven erstellen und bearbeiten.

-   [Punkt Listen](point-lists.md)
-   [Linien Listen](line-lists.md)
-   [Zeilen Streifen](line-strips.md)
-   [Dreiecks Listen](triangle-lists.md)
-   [Dreiecks Streifen](triangle-strips.md)
-   [Dreiecks Lüfter (Direct3D 9)](triangle-fans.md)

Sie können primitive Typen aus einer C++-Anwendung mit einer beliebigen Renderingmethode der [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle rendern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Geräte](direct3d-devices.md)
</dt> </dl>

 

 
