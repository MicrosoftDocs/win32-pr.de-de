---
description: Initiieren Sie das Rendering einer kubischen Umgebungs Zuordnung.
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'ID3DXRenderToEnvMap:: begincube-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bff6c8f3bdc49dfe0c1b677c6805cb332c05007d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354576"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a><span data-ttu-id="e5a70-103">ID3DXRenderToEnvMap:: begincube-Methode</span><span class="sxs-lookup"><span data-stu-id="e5a70-103">ID3DXRenderToEnvMap::BeginCube method</span></span>

<span data-ttu-id="e5a70-104">Initiieren Sie das Rendering einer kubischen Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="e5a70-104">Initiate the rendering of a cubic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5a70-105">Syntax</span></span>


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a><span data-ttu-id="e5a70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5a70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a70-107">*pcubetex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5a70-107">*pCubeTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a70-108">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="e5a70-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="e5a70-109">Ein Zeiger auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die die zu Rendering Ende Cubestruktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="e5a70-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface that represents the cube texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a70-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5a70-110">Return value</span></span>

<span data-ttu-id="e5a70-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5a70-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5a70-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5a70-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e5a70-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e5a70-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5a70-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5a70-114">Remarks</span></span>

<span data-ttu-id="e5a70-115">Weitere Informationen finden Sie unter [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a70-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw each of the 6 faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a70-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5a70-116">Requirements</span></span>



| <span data-ttu-id="e5a70-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5a70-117">Requirement</span></span> | <span data-ttu-id="e5a70-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e5a70-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a70-119">Header</span><span class="sxs-lookup"><span data-stu-id="e5a70-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e5a70-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5a70-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e5a70-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e5a70-121">Library</span></span><br/> | <dl> <span data-ttu-id="e5a70-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5a70-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5a70-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5a70-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a70-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="e5a70-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="e5a70-125">**ID3DXRenderToEnvMap:: End**</span><span class="sxs-lookup"><span data-stu-id="e5a70-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
