---
description: Multipliziert jeden PRT-Vektor (preberechneten Radiance Transfer) mit dem pro-Vertex-Albedo.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'ID3DXPRTEngine:: multiplyalbedo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350726"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a><span data-ttu-id="4bf75-103">ID3DXPRTEngine:: multiplyalbedo-Methode</span><span class="sxs-lookup"><span data-stu-id="4bf75-103">ID3DXPRTEngine::MultiplyAlbedo method</span></span>

<span data-ttu-id="4bf75-104">Multipliziert jeden PRT-Vektor (preberechneten Radiance Transfer) mit dem pro-Vertex-Albedo.</span><span class="sxs-lookup"><span data-stu-id="4bf75-104">Multiplies each precomputed radiance transfer (PRT) vector by the per-vertex albedo.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bf75-105">Syntax</span></span>


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="4bf75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bf75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf75-107">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4bf75-107">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf75-108">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="4bf75-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="4bf75-109">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das PRT-Vektoren enthält, multipliziert mit der pro-Vertex-Albedo.</span><span class="sxs-lookup"><span data-stu-id="4bf75-109">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will contain PRT vectors multiplied by the per-vertex albedo.</span></span> <span data-ttu-id="4bf75-110">Wenn dieser Ausgabepuffer ein Textur Objekt ist, muss darauf geachtet werden, dass die Albedo-Struktur der Textur mit derselben Auflösung wie der Simulations Puffer gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="4bf75-110">If this output buffer is a texture object, then care must be taken to store the albedo of the texture at the same resolution as the simulation buffer.</span></span> <span data-ttu-id="4bf75-111">Sie können die richtige Auflösung für Albedo mit [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)festlegen und ggf. Textur bundbereiche anwenden.</span><span class="sxs-lookup"><span data-stu-id="4bf75-111">You can set the proper resolution on the albedo with [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applying texture gutter regions if appropriate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf75-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bf75-112">Return value</span></span>

<span data-ttu-id="4bf75-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4bf75-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4bf75-114">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4bf75-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4bf75-115">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="4bf75-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf75-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bf75-116">Remarks</span></span>

<span data-ttu-id="4bf75-117">Die ID3DXPRTEngine:: computexxx-Methoden berechnen Ausgabepuffer, in denen das Lichtsignal nicht mit Albedo multipliziert wurde.</span><span class="sxs-lookup"><span data-stu-id="4bf75-117">The ID3DXPRTEngine::Computexxx methods compute output buffers in which the light signal has not been multiplied by albedo.</span></span> <span data-ttu-id="4bf75-118">Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.</span><span class="sxs-lookup"><span data-stu-id="4bf75-118">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="4bf75-119">Um Albedo im gerenderten lichtmodell einzuschließen, müssen Sie diese Methode nach einer der computexxx-Methoden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4bf75-119">To include albedo in the rendered-light model, call this method after one of the Computexxx methods.</span></span>

<span data-ttu-id="4bf75-120">[**ID3DXPRTEngine:: settmeschmaterials**](id3dxprtengine--setmeshmaterials.md) sollte vor dem Aufruf dieser Methode aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4bf75-120">[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) should be called before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf75-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bf75-121">Requirements</span></span>



| <span data-ttu-id="4bf75-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bf75-122">Requirement</span></span> | <span data-ttu-id="4bf75-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4bf75-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf75-124">Header</span><span class="sxs-lookup"><span data-stu-id="4bf75-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4bf75-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf75-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4bf75-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4bf75-126">Library</span></span><br/> | <dl> <span data-ttu-id="4bf75-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bf75-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bf75-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bf75-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf75-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="4bf75-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="4bf75-130">**ID3DXPRTEngine:: computedirectlightingsh**</span><span class="sxs-lookup"><span data-stu-id="4bf75-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




