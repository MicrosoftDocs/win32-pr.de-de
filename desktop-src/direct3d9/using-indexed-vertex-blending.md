---
description: Transformations Zustände 256-511 sind zum Speichern von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Verwenden der indizierten vertexmischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860086"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="f36c8-103">Verwenden der indizierten vertexmischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f36c8-103">Using Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="f36c8-104">Transformations Zustände 256-511 sind zum Speichern von bis zu 256 Matrizen reserviert, die mithilfe von 8-Bit-Indizes indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="f36c8-104">Transform states 256-511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span> <span data-ttu-id="f36c8-105">Verwenden Sie das Makro [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) , um die Indizes 0-255 den entsprechenden Transformations Zuständen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f36c8-105">Use the macro [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) to map indices 0-255 to the corresponding transform states.</span></span> <span data-ttu-id="f36c8-106">Im folgenden Codebeispiel wird gezeigt, wie die [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) -Methode verwendet wird, um die Matrix bei der Transformations Zustands Nummer 256 in eine Identitätsmatrix festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f36c8-106">The following code example shows how to use the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the matrix at transform state number 256 to an identity matrix.</span></span>


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



<span data-ttu-id="f36c8-107">Legen Sie zum Aktivieren oder Deaktivieren des indizierten Vertex-Mischungs Zustands den D3DRS \_ indexedvertexblendenable-Rendering-Zustand auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="f36c8-107">To enable or disable indexed vertex blending, set the D3DRS\_INDEXEDVERTEXBLENDENABLE render state to **TRUE**.</span></span> <span data-ttu-id="f36c8-108">Wenn der renderzustand aktiviert ist, müssen Sie Matrix Indizes als gepackte DWords an jeden Scheitelpunkt übergeben.</span><span class="sxs-lookup"><span data-stu-id="f36c8-108">When the render state is enabled ,you must pass matrix indices as packed DWORDs with every vertex.</span></span> <span data-ttu-id="f36c8-109">Wenn dieser renderzustand deaktiviert und die Scheitelpunkt Mischung aktiviert ist, entspricht er den Matrix Indizes 0, 1, 2 und 3 in jedem Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="f36c8-109">When this render state is disabled and vertex blending is enabled, it is equivalent to having the matrix indices 0, 1, 2, and 3 in every vertex.</span></span> <span data-ttu-id="f36c8-110">Im folgenden Codebeispiel wird die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode verwendet, um die indizierte Vertex-Mischung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f36c8-110">The code example below uses the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method to enable indexed vertex blending.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



<span data-ttu-id="f36c8-111">Legen Sie zum Aktivieren oder Deaktivieren der Scheitelpunkt Mischung den [**IDirect3DDevice9:: setrenderstate-renderzustand**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) auf einen anderen Wert als D3DRS \_ deaktiviert aus dem [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -enumerierten Typ fest.</span><span class="sxs-lookup"><span data-stu-id="f36c8-111">To enable or disable vertex blending, set the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) render state to a value other than D3DRS\_DISABLE from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="f36c8-112">Wenn dieser renderzustand nicht auf D3DRS deaktivieren festgelegt ist \_ , müssen Sie die erforderliche Anzahl von Gewichtungen für jeden Scheitelpunkt übergeben.</span><span class="sxs-lookup"><span data-stu-id="f36c8-112">If this render state is not set to D3DRS\_DISABLE, then you must pass the required number of weights for each vertex.</span></span> <span data-ttu-id="f36c8-113">Im folgenden Codebeispiel wird **IDirect3DDevice9:: setrenderstate** verwendet, um die Vertex-Mischung mit drei Gewichtungen für jeden Scheitelpunkt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f36c8-113">The following code example uses **IDirect3DDevice9::SetRenderState** to enable vertex blending with three weights for each vertex.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a><span data-ttu-id="f36c8-114">Festlegen der Unterstützung für indizierte vertexblending</span><span class="sxs-lookup"><span data-stu-id="f36c8-114">Determining Indexed Vertex Blending Support</span></span>

<span data-ttu-id="f36c8-115">Überprüfen Sie den Member "maxvertexblendmatrixindex" der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur, um die maximale Größe für die indizierte Vertex-Mischungs Matrix zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f36c8-115">To determine the maximum size for the indexed vertex blending matrix, check the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxVertexBlendMatrixIndex member.</span></span> <span data-ttu-id="f36c8-116">Im folgenden Codebeispiel wird die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode verwendet, um diese Größe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f36c8-116">The code example below uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to retrieve this size.</span></span>


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



<span data-ttu-id="f36c8-117">Wenn der in maxvertexblendmatrixindex festgelegte Wert 0 ist, unterstützt das Gerät keine indizierten Matrizen.</span><span class="sxs-lookup"><span data-stu-id="f36c8-117">If the value set in MaxVertexBlendMatrixIndex is 0, the device does not support indexed matrices.</span></span>

> [!Note]  
> <span data-ttu-id="f36c8-118">Wenn die Verarbeitung von Software Scheitel Punkten verwendet wird, können 256 Matrizen für indizierte vertexmischungs Vorgänge mit oder ohne normale Vermischung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f36c8-118">When software vertex processing is used, 256 matrices can be used for indexed vertex blending, with or without normal blending.</span></span>

 

## <a name="passing-matrix-indices-to-direct3d"></a><span data-ttu-id="f36c8-119">Übergeben von Matrix Indizes an Direct3D</span><span class="sxs-lookup"><span data-stu-id="f36c8-119">Passing Matrix Indices to Direct3D</span></span>

<span data-ttu-id="f36c8-120">World Matrix-Indizes können mithilfe von Legacy-Vertex-Shader-FVF-oder-Deklarationen an Direct3D übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="f36c8-120">World matrix indices can be passed to Direct3D by using legacy vertex shaders - FVF - or declarations.</span></span>

<span data-ttu-id="f36c8-121">Das folgende Codebeispiel zeigt, wie ältere Scheitelpunkt-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f36c8-121">The code example below shows how to use legacy vertex shaders.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



<span data-ttu-id="f36c8-122">Wenn ein veralteter Scheitelpunkt-Shader verwendet wird, werden Matrix Indizes mithilfe von D3DFVF xyzbn-Flags mit Scheitelpunkt Positionen übermittelt \_ .</span><span class="sxs-lookup"><span data-stu-id="f36c8-122">When a legacy vertex shader is used, matrix indices are passed together with vertex positions using D3DFVF\_XYZBn flags.</span></span> <span data-ttu-id="f36c8-123">Matrix Indizes werden in einem DWORD als Bytes und müssen direkt hinter der letzten Scheitelpunkt Gewichtung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f36c8-123">Matrix indices are passed as bytes inside a DWORD and must be present immediately after the last vertex weight.</span></span> <span data-ttu-id="f36c8-124">Vertex-Gewichtungen werden auch mit D3DFVF \_ xyzbn übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f36c8-124">Vertex weights are also passed using D3DFVF\_XYZBn.</span></span> <span data-ttu-id="f36c8-125">Ein gepacktes DWORD enthält index3, index2, index1 und index0, wobei sich index0 im niedrigsten Byte des DWORD befindet.</span><span class="sxs-lookup"><span data-stu-id="f36c8-125">A packed DWORD contains index3, index2, index1, and index0, where index0 is located in the lowest byte of the DWORD.</span></span> <span data-ttu-id="f36c8-126">Die Anzahl der verwendeten World-Matrix-Indizes ist gleich der Zahl, die an die Anzahl von Matrizen, die für die Mischung verwendet werden, gemäß [**D3DRS \_ vertexblend**](./d3drenderstatetype.md), festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="f36c8-126">The number of used world-matrix indices is equal to the number passed to the number of matrices used for blending as defined by [**D3DRS\_VERTEXBLEND**](./d3drenderstatetype.md).</span></span>

<span data-ttu-id="f36c8-127">Wenn eine Deklaration verwendet wird, \_ definiert D3DVSDE blendindices das Eingabe Vertex-Register, von dem Matrix Indizes abzurufen sind.</span><span class="sxs-lookup"><span data-stu-id="f36c8-127">When a declaration is used, D3DVSDE\_BLENDINDICES defines the input vertex register to get matrix indices from.</span></span> <span data-ttu-id="f36c8-128">Matrix Indizes müssen als D3DVSDT \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="f36c8-128">Matrix indices must be passed as D3DVSDT\_UBYTE4.</span></span>

<span data-ttu-id="f36c8-129">Das folgende Codebeispiel zeigt, wie Deklarationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f36c8-129">The code example below shows how to use declarations.</span></span> <span data-ttu-id="f36c8-130">Beachten Sie, dass die Reihenfolge der Komponenten nicht mehr wichtig ist, es sei denn, Sie verwenden einen Vertex-Shader fester Funktion.</span><span class="sxs-lookup"><span data-stu-id="f36c8-130">Note that the order of the components is no longer important unless using a fixed-function vertex shader.</span></span>

<span data-ttu-id="f36c8-131">Hier ist die Vertex-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="f36c8-131">Here is the vertex declaration.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



<span data-ttu-id="f36c8-132">Hier ist die entsprechende Register-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="f36c8-132">Here is the corresponding register declaration.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a><span data-ttu-id="f36c8-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f36c8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f36c8-134">Indiziertes Vertex-Blending</span><span class="sxs-lookup"><span data-stu-id="f36c8-134">Indexed Vertex Blending</span></span>](indexed-vertex-blending.md)
</dt> </dl>

 

 
