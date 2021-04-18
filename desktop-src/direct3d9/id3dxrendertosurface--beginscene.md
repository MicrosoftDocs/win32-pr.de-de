---
description: Beginnt eine Szene.
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface:: BeginScene-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364392"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a><span data-ttu-id="4471f-103">ID3DXRenderToSurface:: BeginScene-Methode</span><span class="sxs-lookup"><span data-stu-id="4471f-103">ID3DXRenderToSurface::BeginScene method</span></span>

<span data-ttu-id="4471f-104">Beginnt eine Szene.</span><span class="sxs-lookup"><span data-stu-id="4471f-104">Begins a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="4471f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4471f-105">Syntax</span></span>


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a><span data-ttu-id="4471f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4471f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4471f-107">*pSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4471f-107">*pSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4471f-108">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="4471f-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="4471f-109">Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die die Renderoberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="4471f-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="4471f-110">*pviewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4471f-110">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4471f-111">Typ: **Konstanten [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4471f-111">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="4471f-112">Zeiger auf eine [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, die den Viewport für die Szene beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4471f-112">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, describing the viewport for the scene.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4471f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4471f-113">Return value</span></span>

<span data-ttu-id="4471f-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4471f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4471f-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4471f-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4471f-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall. D3DERR \_ outo-videomemory D3DXERR \_ InvalidData E \_ outoken-Speicher</span><span class="sxs-lookup"><span data-stu-id="4471f-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.D3DERR\_OUTOFVIDEOMEMORY D3DXERR\_INVALIDDATA E\_OUTOFMEMORY</span></span>

## <a name="requirements"></a><span data-ttu-id="4471f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4471f-117">Requirements</span></span>



| <span data-ttu-id="4471f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4471f-118">Requirement</span></span> | <span data-ttu-id="4471f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4471f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4471f-120">Header</span><span class="sxs-lookup"><span data-stu-id="4471f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4471f-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4471f-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4471f-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4471f-122">Library</span></span><br/> | <dl> <span data-ttu-id="4471f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4471f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4471f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4471f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4471f-125">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="4471f-125">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="4471f-126">**ID3DXRenderToSurface:: EndScene**</span><span class="sxs-lookup"><span data-stu-id="4471f-126">**ID3DXRenderToSurface::EndScene**</span></span>](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
