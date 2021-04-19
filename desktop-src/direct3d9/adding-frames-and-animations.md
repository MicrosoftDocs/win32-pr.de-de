---
description: In diesem Abschnitt wird gezeigt, wie Sie einem einfachen Cube Frames und Animationen hinzufügen.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Hinzufügen von Frames und Animationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344347"
---
# <a name="adding-frames-and-animations-direct3d-9"></a>Hinzufügen von Frames und Animationen (Direct3D 9)

In diesem Abschnitt wird gezeigt, wie Sie einem einfachen Cube Frames und Animationen hinzufügen.

## <a name="working-with-frames"></a>Arbeiten mit Frames

Für einen Frame wird die folgende Struktur erwartet.


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



Platzieren Sie das definierte Cube-Mesh in einem Frame mit einer Identitäts Transformation. Wenden Sie dann eine Animation auf diesen Frame an.


```
Frame CubeFrame {
FrameTransformMatrix {
1.000000, 0.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000,
0.000000, 0.000000, 1.000000, 0.000000,
0.000000, 0.000000, 0.000000, 1.000000;;
}
{CubeMesh}        // You could have the mesh inline, but this 
                  // uses an object reference instead.
}
```



## <a name="working-with-animations"></a>Arbeiten mit Animationen

Eine Animation wird durch einen Satz von Schlüsseln definiert. Ein Schlüssel ist ein Zeitwert, der einem Skalierungs Vorgang, einer Ausrichtung oder einer Position zugeordnet ist.


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



Animationen werden dann in animationsets gruppiert:


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



Nehmen Sie jetzt den Cube durch eine Animation.


```
AnimationSet AnimationSet0 {
Animation Animation0 {
{CubeFrame}    // Use the frame containing the cube.
AnimationKey {
2;             // Position keys
9;             // 9 keys
10; 3; -100.000000, 0.000000, 0.000000;;,
20; 3; -75.000000, 0.000000, 0.000000;;,
30; 3; -50.000000, 0.000000, 0.000000;;,
40; 3; -25.500000, 0.000000, 0.000000;;,
50; 3; 0.000000, 0.000000, 0.000000;;,
60; 3; 25.500000, 0.000000, 0.000000;;,
70; 3; 50.000000, 0.000000, 0.000000;;,
80; 3; 75.500000, 0.000000, 0.000000;;,
90; 3; 100.000000, 0.000000, 0.000000;;;
}
}
}
```



Weitere Informationen finden Sie in den Vorlagen [**Animation**](animation.md) und [**animationset**](animationset.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateien (Legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



