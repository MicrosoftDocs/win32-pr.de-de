---
description: Mosaik (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Mosaik (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746936"
---
# <a name="tessellation-direct3d-9"></a>Mosaik (Direct3D 9)

## <a name="tessellator-unit"></a>Mosaik Einheit

Die Mosaik Einheit wurde erweitert. Sie können es jetzt für Folgendes verwenden:

-   Führen Sie ein adaptives Mosaik aller höherwertigen primitiven aus.
-   Suchen Sie nach Vertex-Verschiebungs Werten aus einer Verschiebungs Zuordnung, und übergeben Sie Sie an einen Scheitelpunkt-Shader.
-   Unterstützen von Rechteck-Patch-Mosaik. Dies wird durch eine Scheitelpunkt Deklaration mithilfe von D3DDECLMETHOD \_ partialu oder D3DDECLMETHOD \_ partialv angegeben. Wenn eine Scheitelpunkt Deklaration, die diese Methoden enthält, zum Zeichnen eines Dreiecks Patches verwendet wird, schlägt [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) fehl. Weitere Informationen zu Vertex-Deklarationen finden Sie unter [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

In DirectX 8. x war die Bezeichnung Order tatsächlich der Grad. In Direct3D 9 wird der Grad jetzt durch [**D3DDEGREETYPE**](./d3ddegreetype.md)angegeben.


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



Die Änderung des Grad Typs hat sich auf zwei andere Strukturen ausgewirkt.


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



Treiber müssen Kompilierungsfehler beheben, die durch diese Änderung entstehen, wenn Sie mit den neuen Headern kompiliert werden. Es müssen keine Funktionen geändert werden.

## <a name="adaptive-tessellation"></a>Adaptive Mosaik

Das Adaptive Mosaik kann auf hochwertige primitive, einschließlich N-Patches, Rechteck Patches und Dreiecks Patches, angewendet werden. Diese Funktion wird durch die D3DRS \_ enableadaptivetess-Funktion aktiviert, und es wird ein Patch basierend auf dem tiefen Wert des Steuerelement Scheitel Punkts im Augenbereich angepasst.

Die z-Koordinaten (Zi) der Steuerungs Scheitel Punkte (VI), die in den Augenblick (zieye) transformiert werden, indem Sie ein Punktprodukt mit einem 4-Vektor ausführen, werden als tiefen Werte verwendet. Der 4D-Vektor (MDM) wird von der Anwendung mit vier gerenderzuständen (D3DRS \_ adaptivetess \_ X, D3DRS \_ adaptivetess \_ Y, D3DRS \_ adaptivetess \_ Z und D3DRS \_ adaptivetess \_ W) angegeben. Dieser 4-Vektor kann die dritte Spalte der verketteten Welt-und Ansichts Matrizen sein. Sie kann auch verwendet werden, um eine Skalierung auf zieye anzuwenden.

Es wird angenommen, dass es sich bei der Funktion zum Berechnen eines Mosaik Ebenen-TI aus zieye um (maxtmeellationlevel/zieye) handelt, was bedeutet, dass maxtess Board ationlevel die Mosaik Ebene bei Z = 1 im Augenbereich ist. Maxtmeellationlevel ist gleich einem Wert, der von [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) für N-Patches festgelegt wird, und bei RT-Patches gleich pnumsegs. Die Mosaik Ebene wird dann an die Werte gebunden, die durch die beiden zusätzlichen Rendering-Zustände definiert werden D3DRS \_ mintmeellationlevel und D3DRS \_ maxtmeellationlevel, die die minimalen und maximalen Mosaik Ebenen definieren, an die gebunden werden soll. Der Wert der TI-Datei für jeden Scheitelpunkt an einem Rand eines Patches wird als Mittelwert verwendet, um eine Mosaik Ebene für diesen Edge zu erhalten. Der Algorithmus für die Berechnung von ti für Rechtecke, Dreiecks Patches und N-Patches unterscheidet sich darin, welche Steuerungs Scheitel Punkte zum Berechnen der Mosaik Ebene verwendet werden.

Bei den rechtepatches mit einer B-Spline-Basis werden die vier äußersten Steuerungs Scheitel Punkte verwendet. Mit der D3DORDER-kubischen Reihenfolge werden z. b. Scheitel Punkte \_ (1, 1) und (1, Width-2) mit pnumabgs \[ 0 \] , Vertices (1, Width-2) und (Height-2, Height-2) werden mit pnumabgs \[ 1 \] , Vertices (Height-2, Width-2) und (1, Width-2) mit pnumabgs \[ 2 verwendet \] , und Vertices (2, 1) und (1, 1) werden mit pnumabgs \[ 3 verwendet \] .

Bei den Dreiecks Patches werden die eckpatchvertices verwendet. Mit der D3DORDER- \_ kubischen Reihenfolge: Vertices (0) und (9) werden mit pnumabgs \[ 0 verwendet \] , Vertices (9) und (6) werden mit pnumabgs 1 und Scheitel Punkten \[ \] (6) und (0) mit pnumsek \[ . 3 verwendet \] .

Bei N-Patches werden die Dreiecks Scheitel Punkte verwendet.

Die ecksteuerungs Scheitel Punkte für die Rechteck-und Dreiecks Patches mit der Bezier-Basis werden verwendet.

Pro-Vertex-Mosaik Raten Steuerung. Eine Anwendung kann optional einen einzelnen positiven Gleit Komma Wert pro Scheitelpunkt angeben, der zum Steuern der Geschwindigkeit des Mosaik Werts verwendet werden kann. Dies wird mithilfe \_ von D3DDECLUSAGE Tess Factor bereitgestellt, für den der Verwendungs Index den Wert 0 und der Eingabetyp D3DDECLTYPE FLOAT1 lauten muss \_ . Dies wird mit der pro-Vertex-Mosaik Ebene multipliziert.

### <a name="math"></a>Mathematik

Die Mosaik Ebene (TE) für eine Edge e, die durch zwei Steuerelement Vertices (VE1, Ve2) dargestellt wird, wird wie unten dargestellt berechnet:


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



Wenn D3DRS \_ enableadaptivetess auf **true** festgelegt ist, werden Dreiecks primitive (Dreiecks Listen, Lüfter, Striche) als N-Patches gezeichnet, [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) hat einen Wert kleiner als 1,0.

### <a name="api-changes"></a>API-Änderungen

Neue Rendering-Zustände:


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



Neue Hardware Obergrenzen:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunkt Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 
