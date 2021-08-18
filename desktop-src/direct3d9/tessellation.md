---
description: Mosaik (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Mosaik (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aedc6b435c2993e213e8a4445682725ddb4d460c146afbe420da996e3dbb887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984830"
---
# <a name="tessellation-direct3d-9"></a>Mosaik (Direct3D 9)

## <a name="tessellator-unit"></a>Tessellator-Einheit

Die Mosaikeinheit wurde verbessert. Sie können es jetzt für:

-   Führen Sie ein adaptives Mosaik aller Primitive höherer Ordnung durch.
-   Suchen Sie werte für vertexbezogene Verschiebungen aus einer Verschiebungszuordnung, und übergeben Sie sie an einen Vertex-Shader.
-   Unterstützung für Rechteck-Patch-Mosaik. Dies wird durch eine Scheitelpunktdeklaration mit D3DDECLMETHOD \_ PARTIALU oder D3DDECLMETHOD \_ PARTIALV angegeben. Wenn eine Scheitelpunktdeklaration, die diese Methoden enthält, zum Zeichnen eines Dreieckspatches verwendet wird, schlägt [**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api) fehl. Weitere Informationen zu Scheitelpunktdeklarationen finden Sie unter [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

In DirectX 8.x war das, was als ORDER bezeichnet wurde, tatsächlich der Grad. In Direct3D 9 wird der Grad jetzt durch [**D3DDEGREETYPE**](./d3ddegreetype.md)angegeben.


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



Die Änderung des Gradtyps wirkte sich auf zwei andere Strukturen aus.


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



Treiber müssen Kompilierungsfehler beheben, die sich aus dieser Änderung ergeben, wenn sie mit den neuen Headern kompilieren. Die Funktionalität muss nicht geändert werden.

## <a name="adaptive-tessellation"></a>Adaptive Mosaik

Adaptive Mosaike können auf primitive Typen hoher Ordnung angewendet werden, einschließlich N-Patches, Rechteckpatches und Dreieckspatches. Dieses Feature wird von D3DRS \_ ENABLEADAPTIVETESSELLATION aktiviert und setzt einen Patch auf Der Grundlage des Tiefenwerts des Steuerpunkts im Augenbereich adaptiver Mosaik.

Die Z-Koordinaten (Zi) von Steuervertices (Vi), die durch Ausführen eines Punktprodukts mit einem 4-Vektor in den Augenbereich (Zieye) transformiert werden, werden als Tiefenwerte verwendet. Der 4D-Vektor (Mdm) wird von der Anwendung mit vier Renderzuständen (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z und D3DRS \_ ADAPTIVETESS \_ W) angegeben. Dieser 4-Vektor kann die dritte Spalte der verketteten Welt und der Ansichtsmatrizen sein. Sie kann auch verwendet werden, um eine Skala auf Zieye anzuwenden.

Die Funktion zum Berechnen der Mosaikebene Ti von Zieye wird als (MaxTessellationLevel/Zieye) angenommen. Dies bedeutet, dass MaxTessellationLevel die Mosaikebene bei Z = 1 im Augenbereich ist. MaxTessellationLevel ist gleich einem Wert, der von [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) für N-Patches und bei RT-Patches gleich pNumSegs festgelegt wird. Die Mosaikebene wird dann an Werte gebunden, die durch die beiden zusätzlichen Renderzustände D3DRS \_ MINTESSELLATIONLEVEL und D3DRS \_ MAXTESSELLATIONLEVEL definiert werden, die die minimalen und maximalen Mosaikebenen definieren, an die gebunden werden soll. Die Tis für jeden Scheitelpunkt entlang einer Kante eines Patches werden gemittelt, um eine Mosaikebene für diesen Rand zu erhalten. Der Algorithmus zum Berechnen von Ti für Rechteckpatches, Dreieckspatches und N-Patches unterscheidet sich darin, welche Steuervertices zum Berechnen der Mosaikebene verwendet werden.

Für rechteckige Patches mit B-Spline-Basis werden die vier äußersten Steuervertices verwendet. Beispiel: mit D3DORDER \_ CUBIC-Reihenfolge: Scheitelpunkte (1,1) und (1,Breite-2) werden mit pNumSegs \[ 0 \] verwendet, Vertices (1, Width-2) und (height-2, height-2) werden mit pNumSeg verwendet. Die \[ Vertices 1 \] , Vertices (height-2, width-2) und (1,width-2) werden mit pNumSegs \[ 2 \] verwendet, und Scheitelpunkte (2,1) und (1,1) werden mit pNumSegs \[ 3 \] verwendet.

Für die Dreieckspatches werden die Eckpatchvertices verwendet. Bei D3DORDER \_ CUBIC-Reihenfolge: Scheitelpunkte (0) und (9) werden mit pNumSegs \[ 0 \] verwendet, Scheitelpunkte (9) und (6) werden mit pNumSegs \[ 1 \] und Scheitelpunkte (6) und (0) mit pNumSegs \[ 3 \] verwendet.

Für N-Patches werden die Dreiecksvertices verwendet.

Für die Rechteck- und Dreieckspatches mit einer Bézierbasis werden die Ecksteuerpunkte verwendet.

Steuerung der Mosaikrate pro Scheitelpunkt. Eine Anwendung kann optional einen einzelnen positiven Gleitkommawert pro Scheitelpunkt bereitstellen, der zum Steuern der Mosaikrate verwendet werden kann. Dies wird mithilfe des D3DDECLUSAGE \_ TESSFACTOR bereitgestellt, für den der Nutzungsindex 0 und der Eingabetyp D3DDECLTYPE FLOAT1 sein \_ muss. Dies wird mit der Mosaikebene pro Scheitelpunkt multipliziert.

### <a name="math"></a>Mathematik

Die Mosaikebene (Te) für einen Rand e, dargestellt durch zwei Steuervertices (Ve1, Ve2), wird wie unten dargestellt berechnet:


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



Wenn D3DRS \_ ENABLEADAPTIVETESSELLATION **AUF TRUE** festgelegt ist, werden Dreiecksprimitive (Dreieckslisten, Lüfter, Strips) als N-Patches gezeichnet. [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) hat einen festgelegten Wert kleiner als 1,0.

### <a name="api-changes"></a>API-Änderungen

Neue Renderzustände:


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



Und ihre Standardwerte:


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



Neue Hardwareobergrenzen:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 
