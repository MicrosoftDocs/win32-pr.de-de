---
description: Ein Dreiecks Lüfter ähnelt einem Dreiecks Streifen, mit dem Unterschied, dass alle Dreiecke einen Scheitelpunkt gemeinsam verwenden, wie in der folgenden Abbildung dargestellt.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Dreiecks Lüfter (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555777"
---
# <a name="triangle-fans-direct3d-9"></a>Dreiecks Lüfter (Direct3D 9)

Ein Dreiecks Lüfter ähnelt einem Dreiecks Streifen, mit dem Unterschied, dass alle Dreiecke einen Scheitelpunkt gemeinsam verwenden, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Dreiecks Lüfters](images/trifan.gif)

Das System verwendet Vertices v2, v3 und v1, um das erste Dreieck zu zeichnen. v3, v4 und v1 zum Zeichnen des zweiten Dreiecks V4, V5 und v1 zum Zeichnen des dritten Dreiecks Und so weiter. Wenn die flache Schattierung aktiviert ist, schattiert das System das Dreieck mit der Farbe seines ersten Scheitel Punkts.

Die folgende Abbildung stellt einen gerenderten Dreiecks Lüfter dar.

![Abbildung eines gerenderten Dreiecks Lüfters](images/tfan2.gif)

Der folgende Code zeigt, wie Vertices für diesen Dreiecks Lüfter erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie diesen Dreiecks Lüfter in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)rendernen.


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



Dreiecks Lüfter werden in Direct3D 10 oder höher nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitive](primitives.md)
</dt> </dl>

 

 
