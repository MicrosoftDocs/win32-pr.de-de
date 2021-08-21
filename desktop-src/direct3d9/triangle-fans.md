---
description: Ein Dreiecksfächer ähnelt einem Dreiecksstreifen, mit der Ausnahme, dass sich alle Dreiecke einen Scheitelpunkt teilen, wie in der folgenden Abbildung dargestellt.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Dreiecksfächer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806dc57545f4cb8341eee2b586aa062ba93d98568e6269e209dbf616fbb081d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044176"
---
# <a name="triangle-fans-direct3d-9"></a>Dreiecksfächer (Direct3D 9)

Ein Dreiecksfächer ähnelt einem Dreiecksstreifen, mit der Ausnahme, dass sich alle Dreiecke einen Scheitelpunkt teilen, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Dreiecksfächers](images/trifan.gif)

Das System verwendet die Scheitelpunkte v2, v3 und v1, um das erste Dreieck zu zeichnen. v3, v4 und v1, um das zweite Dreieck zu zeichnen; v4, v5 und v1, um das dritte Dreieck zu zeichnen; Und so weiter. Wenn die flache Schattierung aktiviert ist, schattiert das System das Dreieck mit der Farbe des ersten Scheitelpunkts.

Die folgende Abbildung zeigt einen gerenderten Dreiecksfächer.

![Abbildung eines gerenderten Dreiecksfächers](images/tfan2.gif)

Der folgende Code zeigt, wie Scheitelpunkte für diesen Dreiecksfächer erstellt werden.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



Das folgende Codebeispiel zeigt, wie dieser Dreiecksfächer in Direct3D 9 mithilfe von [**IDirect3DDevice9::D rawPrimitive gerendert wird.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



Dreiecksfächer werden in Direct3D 10 oder höher nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitive](primitives.md)
</dt> </dl>

 

 
