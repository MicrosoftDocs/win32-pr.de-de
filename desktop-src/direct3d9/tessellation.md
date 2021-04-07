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
# <a name="tessellation-direct3d-9"></a><span data-ttu-id="23623-103">Mosaik (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23623-103">Tessellation (Direct3D 9)</span></span>

## <a name="tessellator-unit"></a><span data-ttu-id="23623-104">Mosaik Einheit</span><span class="sxs-lookup"><span data-stu-id="23623-104">Tessellator Unit</span></span>

<span data-ttu-id="23623-105">Die Mosaik Einheit wurde erweitert.</span><span class="sxs-lookup"><span data-stu-id="23623-105">The tessellator unit has been enhanced.</span></span> <span data-ttu-id="23623-106">Sie können es jetzt für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="23623-106">You can now use it to:</span></span>

-   <span data-ttu-id="23623-107">Führen Sie ein adaptives Mosaik aller höherwertigen primitiven aus.</span><span class="sxs-lookup"><span data-stu-id="23623-107">Perform adaptive tessellation of all higher-order primitives.</span></span>
-   <span data-ttu-id="23623-108">Suchen Sie nach Vertex-Verschiebungs Werten aus einer Verschiebungs Zuordnung, und übergeben Sie Sie an einen Scheitelpunkt-Shader.</span><span class="sxs-lookup"><span data-stu-id="23623-108">Look up per-vertex displacement values from a displacement map and pass them on to a vertex shader.</span></span>
-   <span data-ttu-id="23623-109">Unterstützen von Rechteck-Patch-Mosaik.</span><span class="sxs-lookup"><span data-stu-id="23623-109">Support rectangle-patch tessellation.</span></span> <span data-ttu-id="23623-110">Dies wird durch eine Scheitelpunkt Deklaration mithilfe von D3DDECLMETHOD \_ partialu oder D3DDECLMETHOD \_ partialv angegeben.</span><span class="sxs-lookup"><span data-stu-id="23623-110">This is specified through a vertex declaration using D3DDECLMETHOD\_PARTIALU or D3DDECLMETHOD\_PARTIALV.</span></span> <span data-ttu-id="23623-111">Wenn eine Scheitelpunkt Deklaration, die diese Methoden enthält, zum Zeichnen eines Dreiecks Patches verwendet wird, schlägt [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) fehl.</span><span class="sxs-lookup"><span data-stu-id="23623-111">If a vertex declaration containing these methods is used to draw a triangle patch, [**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) will fail.</span></span> <span data-ttu-id="23623-112">Weitere Informationen zu Vertex-Deklarationen finden Sie unter [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="23623-112">For more information about vertex declarations, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="23623-113">In DirectX 8. x war die Bezeichnung Order tatsächlich der Grad.</span><span class="sxs-lookup"><span data-stu-id="23623-113">In DirectX 8.x, what was called ORDER was really the degree.</span></span> <span data-ttu-id="23623-114">In Direct3D 9 wird der Grad jetzt durch [**D3DDEGREETYPE**](./d3ddegreetype.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="23623-114">In Direct3D 9, the degree is now specified by [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>


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



<span data-ttu-id="23623-115">Die Änderung des Grad Typs hat sich auf zwei andere Strukturen ausgewirkt.</span><span class="sxs-lookup"><span data-stu-id="23623-115">The change in degree type affected two other structures.</span></span>


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



<span data-ttu-id="23623-116">Treiber müssen Kompilierungsfehler beheben, die durch diese Änderung entstehen, wenn Sie mit den neuen Headern kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="23623-116">Drivers need to fix compilation errors that will result from this change when they compile with the new headers.</span></span> <span data-ttu-id="23623-117">Es müssen keine Funktionen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="23623-117">No functionality has to be changed.</span></span>

## <a name="adaptive-tessellation"></a><span data-ttu-id="23623-118">Adaptive Mosaik</span><span class="sxs-lookup"><span data-stu-id="23623-118">Adaptive Tessellation</span></span>

<span data-ttu-id="23623-119">Das Adaptive Mosaik kann auf hochwertige primitive, einschließlich N-Patches, Rechteck Patches und Dreiecks Patches, angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="23623-119">Adaptive tessellation can be applied to high-order primitives including N-patches, rectangle patches, and triangle patches.</span></span> <span data-ttu-id="23623-120">Diese Funktion wird durch die D3DRS \_ enableadaptivetess-Funktion aktiviert, und es wird ein Patch basierend auf dem tiefen Wert des Steuerelement Scheitel Punkts im Augenbereich angepasst.</span><span class="sxs-lookup"><span data-stu-id="23623-120">This feature is enabled by the D3DRS\_ENABLEADAPTIVETESSELLATION and adaptively tessellates a patch, based on the depth value of the control vertex in eye space.</span></span>

<span data-ttu-id="23623-121">Die z-Koordinaten (Zi) der Steuerungs Scheitel Punkte (VI), die in den Augenblick (zieye) transformiert werden, indem Sie ein Punktprodukt mit einem 4-Vektor ausführen, werden als tiefen Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="23623-121">The z-coordinates (Zi) of control vertices (Vi), which are transformed into eye space (Zieye) by performing a dot product with a 4-vector, are used as the depth values.</span></span> <span data-ttu-id="23623-122">Der 4D-Vektor (MDM) wird von der Anwendung mit vier gerenderzuständen (D3DRS \_ adaptivetess \_ X, D3DRS \_ adaptivetess \_ Y, D3DRS \_ adaptivetess \_ Z und D3DRS \_ adaptivetess \_ W) angegeben.</span><span class="sxs-lookup"><span data-stu-id="23623-122">The 4D vector (Mdm) is specified by the application using four render states (D3DRS\_ADAPTIVETESS\_X, D3DRS\_ADAPTIVETESS\_Y, D3DRS\_ADAPTIVETESS\_Z, and D3DRS\_ADAPTIVETESS\_W).</span></span> <span data-ttu-id="23623-123">Dieser 4-Vektor kann die dritte Spalte der verketteten Welt-und Ansichts Matrizen sein.</span><span class="sxs-lookup"><span data-stu-id="23623-123">This 4-vector could be the third column of the concatenated world and view matrices.</span></span> <span data-ttu-id="23623-124">Sie kann auch verwendet werden, um eine Skalierung auf zieye anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="23623-124">It also could be used to apply a scale to Zieye.</span></span>

<span data-ttu-id="23623-125">Es wird angenommen, dass es sich bei der Funktion zum Berechnen eines Mosaik Ebenen-TI aus zieye um (maxtmeellationlevel/zieye) handelt, was bedeutet, dass maxtess Board ationlevel die Mosaik Ebene bei Z = 1 im Augenbereich ist.</span><span class="sxs-lookup"><span data-stu-id="23623-125">The function to compute a tessellation level Ti from Zieye is assumed to be (MaxTessellationLevel/Zieye), which means that the MaxTessellationLevel is the tessellation level at Z = 1 in eye space.</span></span> <span data-ttu-id="23623-126">Maxtmeellationlevel ist gleich einem Wert, der von [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) für N-Patches festgelegt wird, und bei RT-Patches gleich pnumsegs.</span><span class="sxs-lookup"><span data-stu-id="23623-126">The MaxTessellationLevel is equal to a value set by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) for N-patches and, for RT-patches, it is equal to pNumSegs.</span></span> <span data-ttu-id="23623-127">Die Mosaik Ebene wird dann an die Werte gebunden, die durch die beiden zusätzlichen Rendering-Zustände definiert werden D3DRS \_ mintmeellationlevel und D3DRS \_ maxtmeellationlevel, die die minimalen und maximalen Mosaik Ebenen definieren, an die gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="23623-127">The tessellation level is then clamped to values, defined by the two additional render states D3DRS\_MINTESSELLATIONLEVEL and D3DRS\_MAXTESSELLATIONLEVEL, which define the minimum and maximum tessellation levels to be clamped to.</span></span> <span data-ttu-id="23623-128">Der Wert der TI-Datei für jeden Scheitelpunkt an einem Rand eines Patches wird als Mittelwert verwendet, um eine Mosaik Ebene für diesen Edge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="23623-128">The Ti's for each vertex along an edge of a patch are averaged to obtain a tessellation level for that edge.</span></span> <span data-ttu-id="23623-129">Der Algorithmus für die Berechnung von ti für Rechtecke, Dreiecks Patches und N-Patches unterscheidet sich darin, welche Steuerungs Scheitel Punkte zum Berechnen der Mosaik Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23623-129">The algorithm for computing Ti for rectangle patches, triangle patches, and N-patches differs in what control vertices are used to compute the tessellation level.</span></span>

<span data-ttu-id="23623-130">Bei den rechtepatches mit einer B-Spline-Basis werden die vier äußersten Steuerungs Scheitel Punkte verwendet.</span><span class="sxs-lookup"><span data-stu-id="23623-130">For the rectangle patches with a B-spline basis, the four outermost control vertices are used.</span></span> <span data-ttu-id="23623-131">Mit der D3DORDER-kubischen Reihenfolge werden z. b. Scheitel Punkte \_ (1, 1) und (1, Width-2) mit pnumabgs \[ 0 \] , Vertices (1, Width-2) und (Height-2, Height-2) werden mit pnumabgs \[ 1 \] , Vertices (Height-2, Width-2) und (1, Width-2) mit pnumabgs \[ 2 verwendet \] , und Vertices (2, 1) und (1, 1) werden mit pnumabgs \[ 3 verwendet \] .</span><span class="sxs-lookup"><span data-stu-id="23623-131">For example, with D3DORDER\_CUBIC order: vertices (1,1) and (1,width-2) are used with pNumSegs\[0\], vertices (1,width-2) and (height-2,height-2) are used with pNumSegs\[1\], vertices (height-2,width-2) and (1,width-2) are used with pNumSegs\[2\], and vertices (2,1) and (1,1) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="23623-132">Bei den Dreiecks Patches werden die eckpatchvertices verwendet.</span><span class="sxs-lookup"><span data-stu-id="23623-132">For the triangle patches, the corner patch vertices are used.</span></span> <span data-ttu-id="23623-133">Mit der D3DORDER- \_ kubischen Reihenfolge: Vertices (0) und (9) werden mit pnumabgs \[ 0 verwendet \] , Vertices (9) und (6) werden mit pnumabgs 1 und Scheitel Punkten \[ \] (6) und (0) mit pnumsek \[ . 3 verwendet \] .</span><span class="sxs-lookup"><span data-stu-id="23623-133">With D3DORDER\_CUBIC order: vertices (0) and (9) are used with pNumSegs\[0\], vertices (9) and (6) are used with pNumSegs\[1\] and vertices (6) and (0) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="23623-134">Bei N-Patches werden die Dreiecks Scheitel Punkte verwendet.</span><span class="sxs-lookup"><span data-stu-id="23623-134">For N-patches the triangle vertices are used.</span></span>

<span data-ttu-id="23623-135">Die ecksteuerungs Scheitel Punkte für die Rechteck-und Dreiecks Patches mit der Bezier-Basis werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="23623-135">For the rectangle and triangle patches with a Bezier basis, the corner-control vertices are used.</span></span>

<span data-ttu-id="23623-136">Pro-Vertex-Mosaik Raten Steuerung.</span><span class="sxs-lookup"><span data-stu-id="23623-136">Per-vertex tessellation rate control.</span></span> <span data-ttu-id="23623-137">Eine Anwendung kann optional einen einzelnen positiven Gleit Komma Wert pro Scheitelpunkt angeben, der zum Steuern der Geschwindigkeit des Mosaik Werts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="23623-137">An application can optionally supply a single positive floating-point value per vertex, which can be used to control the rate of tessellation.</span></span> <span data-ttu-id="23623-138">Dies wird mithilfe \_ von D3DDECLUSAGE Tess Factor bereitgestellt, für den der Verwendungs Index den Wert 0 und der Eingabetyp D3DDECLTYPE FLOAT1 lauten muss \_ .</span><span class="sxs-lookup"><span data-stu-id="23623-138">This is supplied using the D3DDECLUSAGE\_TESSFACTOR, for which usage index must be 0 and input type must be D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="23623-139">Dies wird mit der pro-Vertex-Mosaik Ebene multipliziert.</span><span class="sxs-lookup"><span data-stu-id="23623-139">This is multiplied to the per-vertex tessellation level.</span></span>

### <a name="math"></a><span data-ttu-id="23623-140">Mathematik</span><span class="sxs-lookup"><span data-stu-id="23623-140">Math</span></span>

<span data-ttu-id="23623-141">Die Mosaik Ebene (TE) für eine Edge e, die durch zwei Steuerelement Vertices (VE1, Ve2) dargestellt wird, wird wie unten dargestellt berechnet:</span><span class="sxs-lookup"><span data-stu-id="23623-141">The tessellation level (Te) for an edge e, represented by two control vertices (Ve1, Ve2), is computed as shown below :</span></span>


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



<span data-ttu-id="23623-142">Wenn D3DRS \_ enableadaptivetess auf **true** festgelegt ist, werden Dreiecks primitive (Dreiecks Listen, Lüfter, Striche) als N-Patches gezeichnet, [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) hat einen Wert kleiner als 1,0.</span><span class="sxs-lookup"><span data-stu-id="23623-142">When D3DRS\_ENABLEADAPTIVETESSELLATION is **TRUE**, triangle primitives (triangle lists, fans, strips) are drawn as N-patches, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) has set value less than 1.0.</span></span>

### <a name="api-changes"></a><span data-ttu-id="23623-143">API-Änderungen</span><span class="sxs-lookup"><span data-stu-id="23623-143">API Changes</span></span>

<span data-ttu-id="23623-144">Neue Rendering-Zustände:</span><span class="sxs-lookup"><span data-stu-id="23623-144">New render states:</span></span>


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



<span data-ttu-id="23623-145">Und ihre Standardwerte:</span><span class="sxs-lookup"><span data-stu-id="23623-145">And their default values:</span></span>


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



<span data-ttu-id="23623-146">Neue Hardware Obergrenzen:</span><span class="sxs-lookup"><span data-stu-id="23623-146">New hardware caps:</span></span>


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a><span data-ttu-id="23623-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23623-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23623-148">Scheitelpunkt Pipeline</span><span class="sxs-lookup"><span data-stu-id="23623-148">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
