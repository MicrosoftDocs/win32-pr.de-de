---
description: Die folgende benutzerdefinierte Struktur kann für Vertices verwendet werden, die zwischen zwei Matrizen gemischt werden.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Verwenden von Geometrie Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343934"
---
# <a name="using-geometry-blending-direct3d-9"></a>Verwenden von Geometrie Mischung (Direct3D 9)

Die folgende benutzerdefinierte Struktur kann für Vertices verwendet werden, die zwischen zwei Matrizen gemischt werden.


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



Die Blend-Gewichtung muss nach der Position und den Rhw-Daten in der SVF und vor der Vertex-Norm angezeigt werden.

Beachten Sie, dass das vorangehende Vertex-Format nur einen Mischungs Gewichtungswert enthält. Dies liegt daran, dass es zwei Welt Matrizen gibt, die in den Transformations Zuständen [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md)(0) und **D3DTS \_ worldmatrix**(1) definiert werden. Das System mischt jeden Scheitelpunkt zwischen diesen beiden Matrizen mithilfe des einzelnen Gewichtungs Werts. Bei drei Matrizen sind nur zwei Gewichtungen erforderlich, usw.

> [!Note]
>
> Das Definieren von Skin-Gewichtungen ist einfach. Die Verwendung einer linearen Funktion der Entfernung zwischen den Gelenken ist ein guter Einstieg, aber eine reibungslosere SIG-ID-Funktion sieht besser aus. Die Auswahl einer Skin-Gewichtungs-Verteilungsfunktion kann bei Bedarf zu Sharp-shases bei den Gelenken führen, indem eine große Variation der Skin-Gewichtung über eine kurze Entfernung verwendet wird.

 

## <a name="setting-blending-matrices"></a>Festlegen von Mischungs Matrizen

Sie legen die Transformations Matrizen fest, zwischen denen das System durch Aufrufen der [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode vermischt wird. Legen Sie den ersten Parameter auf einen Wert fest, der durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro definiert ist, und legen Sie den zweiten Parameter auf die Adresse der festzulegenden Matrix fest.

Im folgenden C++-Codebeispiel werden zwei World-Matrizen festgelegt, zwischen denen die Geometrie gemischt wird, um die Illusion eines verbundenen Arm zu erzeugen.


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



Das Festlegen einer Mischungs Matrix bewirkt lediglich, dass das System die Matrix für die spätere Verwendung zwischenspeichert. Das System weist nicht an, mit dem Mischen von Vertices zu beginnen.

## <a name="enabling-geometry-blending"></a>Aktivieren der Geometrie Mischung

Geometry-Blending ist standardmäßig deaktiviert. Um die Geometrie Mischung zu aktivieren, müssen Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/desktop/api) -Methode aufrufen, um den D3DRS \_ vertexblend-renderzustand auf einen Wert aus dem [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -enumerierten Typ festzulegen. Im folgenden Codebeispiel wird veranschaulicht, wie dieser-Befehl aussehen könnte, wenn der Rendering-Zustand für eine Blend zwischen zwei Welt Matrizen festgelegt wird.


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



Wenn D3DRS \_ vertexblend auf einen anderen Wert als D3DVBF deaktivieren festgelegt ist \_ , geht das System davon aus, dass die entsprechende Anzahl von Mischungs Gewichtungen im Scheitelpunkt Format enthalten ist. Es liegt in ihrer Verantwortung, ein kompatibles Vertex-Format bereitzustellen und eine ordnungsgemäße Beschreibung dieses Formats für die Direct3D-Renderingmethoden bereitzustellen.

Wenn diese Option aktiviert ist, führt das System eine Geometrie Mischung für alle Objekte aus, die von den drawprimitive-Renderingmethoden

## <a name="see-also"></a>Weitere Informationen

[Code der Fixed-Funktion (Direct3D 9)](fixed-function-fvf-codes.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometrie Mischung](geometry-blending.md)
</dt> </dl>

 

 
