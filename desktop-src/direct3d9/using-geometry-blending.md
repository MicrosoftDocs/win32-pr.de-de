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
# <a name="using-geometry-blending-direct3d-9"></a><span data-ttu-id="ec93b-103">Verwenden von Geometrie Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ec93b-103">Using Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="ec93b-104">Die folgende benutzerdefinierte Struktur kann für Vertices verwendet werden, die zwischen zwei Matrizen gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="ec93b-104">The following user-defined structure can be used for vertices that will be blended between two matrices.</span></span>


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



<span data-ttu-id="ec93b-105">Die Blend-Gewichtung muss nach der Position und den Rhw-Daten in der SVF und vor der Vertex-Norm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec93b-105">The blend weight must appear after the position and RHW data in the FVF, and before the vertex normal.</span></span>

<span data-ttu-id="ec93b-106">Beachten Sie, dass das vorangehende Vertex-Format nur einen Mischungs Gewichtungswert enthält.</span><span class="sxs-lookup"><span data-stu-id="ec93b-106">Notice that the preceding vertex format contains only one blending weight value.</span></span> <span data-ttu-id="ec93b-107">Dies liegt daran, dass es zwei Welt Matrizen gibt, die in den Transformations Zuständen [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md)(0) und **D3DTS \_ worldmatrix**(1) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec93b-107">This is because there will be two world matrices, defined in the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md)(0) and **D3DTS\_WORLDMATRIX**(1) transform states.</span></span> <span data-ttu-id="ec93b-108">Das System mischt jeden Scheitelpunkt zwischen diesen beiden Matrizen mithilfe des einzelnen Gewichtungs Werts.</span><span class="sxs-lookup"><span data-stu-id="ec93b-108">The system blends each vertex between these two matrices using the single weight value.</span></span> <span data-ttu-id="ec93b-109">Bei drei Matrizen sind nur zwei Gewichtungen erforderlich, usw.</span><span class="sxs-lookup"><span data-stu-id="ec93b-109">For three matrices, only two weights are required, and so on.</span></span>

> [!Note]
>
> <span data-ttu-id="ec93b-110">Das Definieren von Skin-Gewichtungen ist einfach.</span><span class="sxs-lookup"><span data-stu-id="ec93b-110">Defining skin weights is easy.</span></span> <span data-ttu-id="ec93b-111">Die Verwendung einer linearen Funktion der Entfernung zwischen den Gelenken ist ein guter Einstieg, aber eine reibungslosere SIG-ID-Funktion sieht besser aus.</span><span class="sxs-lookup"><span data-stu-id="ec93b-111">Using a linear function of the distance between joints is good start, but a smoother sigmoid function looks better.</span></span> <span data-ttu-id="ec93b-112">Die Auswahl einer Skin-Gewichtungs-Verteilungsfunktion kann bei Bedarf zu Sharp-shases bei den Gelenken führen, indem eine große Variation der Skin-Gewichtung über eine kurze Entfernung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ec93b-112">Choosing a skin-weight distribution function can result in sharp creases at joints, if desired, by using a large variation in skin weight over a short distance.</span></span>

 

## <a name="setting-blending-matrices"></a><span data-ttu-id="ec93b-113">Festlegen von Mischungs Matrizen</span><span class="sxs-lookup"><span data-stu-id="ec93b-113">Setting Blending Matrices</span></span>

<span data-ttu-id="ec93b-114">Sie legen die Transformations Matrizen fest, zwischen denen das System durch Aufrufen der [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode vermischt wird.</span><span class="sxs-lookup"><span data-stu-id="ec93b-114">You set the transformation matrices between which the system blends by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ec93b-115">Legen Sie den ersten Parameter auf einen Wert fest, der durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro definiert ist, und legen Sie den zweiten Parameter auf die Adresse der festzulegenden Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="ec93b-115">Set the first parameter to a value defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, and set the second parameter to the address of the matrix to be set.</span></span>

<span data-ttu-id="ec93b-116">Im folgenden C++-Codebeispiel werden zwei World-Matrizen festgelegt, zwischen denen die Geometrie gemischt wird, um die Illusion eines verbundenen Arm zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="ec93b-116">The following C++ code example sets two world matrices, between which geometry is blended to create the illusion of a jointed arm.</span></span>


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



<span data-ttu-id="ec93b-117">Das Festlegen einer Mischungs Matrix bewirkt lediglich, dass das System die Matrix für die spätere Verwendung zwischenspeichert. Das System weist nicht an, mit dem Mischen von Vertices zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ec93b-117">Setting a blending matrix merely causes the system to cache the matrix for later use; it doesn't instruct the system to begin blending vertices.</span></span>

## <a name="enabling-geometry-blending"></a><span data-ttu-id="ec93b-118">Aktivieren der Geometrie Mischung</span><span class="sxs-lookup"><span data-stu-id="ec93b-118">Enabling Geometry Blending</span></span>

<span data-ttu-id="ec93b-119">Geometry-Blending ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ec93b-119">Geometry blending is disabled by default.</span></span> <span data-ttu-id="ec93b-120">Um die Geometrie Mischung zu aktivieren, müssen Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/desktop/api) -Methode aufrufen, um den D3DRS \_ vertexblend-renderzustand auf einen Wert aus dem [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -enumerierten Typ festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ec93b-120">To enable geometry blending, call the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method to set the D3DRS\_VERTEXBLEND render state to a value from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="ec93b-121">Im folgenden Codebeispiel wird veranschaulicht, wie dieser-Befehl aussehen könnte, wenn der Rendering-Zustand für eine Blend zwischen zwei Welt Matrizen festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ec93b-121">The following code example shows what this call might look like when setting the render state for a blend between two world matrices.</span></span>


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



<span data-ttu-id="ec93b-122">Wenn D3DRS \_ vertexblend auf einen anderen Wert als D3DVBF deaktivieren festgelegt ist \_ , geht das System davon aus, dass die entsprechende Anzahl von Mischungs Gewichtungen im Scheitelpunkt Format enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ec93b-122">When D3DRS\_VERTEXBLEND is set to any value other than D3DVBF\_DISABLE, the system assumes that the appropriate number of blending weights will be included in the vertex format.</span></span> <span data-ttu-id="ec93b-123">Es liegt in ihrer Verantwortung, ein kompatibles Vertex-Format bereitzustellen und eine ordnungsgemäße Beschreibung dieses Formats für die Direct3D-Renderingmethoden bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ec93b-123">It is your responsibility to provide a compliant vertex format, and to provide a proper description of that format to the Direct3D rendering methods.</span></span>

<span data-ttu-id="ec93b-124">Wenn diese Option aktiviert ist, führt das System eine Geometrie Mischung für alle Objekte aus, die von den drawprimitive-Renderingmethoden</span><span class="sxs-lookup"><span data-stu-id="ec93b-124">When enabled, the system performs geometry blending for all objects rendered by the DrawPrimitive rendering methods.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec93b-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ec93b-125">See Also</span></span>

[<span data-ttu-id="ec93b-126">Code der Fixed-Funktion (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ec93b-126">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)


## <a name="related-topics"></a><span data-ttu-id="ec93b-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec93b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec93b-128">Geometrie Mischung</span><span class="sxs-lookup"><span data-stu-id="ec93b-128">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 
