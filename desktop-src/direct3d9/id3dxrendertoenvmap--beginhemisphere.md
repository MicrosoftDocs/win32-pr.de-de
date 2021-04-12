---
description: Initiieren Sie das Rendering einer Hemispheric-Umgebungs Zuordnung.
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: 'ID3DXRenderToEnvMap:: beginhemisphäre-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96eb4bbf4cfc6cac952368337456b946f64cf711
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219485"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a><span data-ttu-id="6514c-103">ID3DXRenderToEnvMap:: beginhemisphäre-Methode</span><span class="sxs-lookup"><span data-stu-id="6514c-103">ID3DXRenderToEnvMap::BeginHemisphere method</span></span>

<span data-ttu-id="6514c-104">Initiieren Sie das Rendering einer Hemispheric-Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6514c-104">Initiate the rendering of a hemispheric environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="6514c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6514c-105">Syntax</span></span>


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="6514c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6514c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6514c-107">*ptexzpos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6514c-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6514c-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="6514c-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="6514c-109">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die positive Textur Renderoberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="6514c-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive texture render surface.</span></span>

</dd> <dt>

<span data-ttu-id="6514c-110">*ptexznetg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6514c-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6514c-111">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="6514c-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="6514c-112">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die negative Textur Renderoberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="6514c-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative texture render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6514c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6514c-113">Return value</span></span>

<span data-ttu-id="6514c-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6514c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6514c-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6514c-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6514c-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall. E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="6514c-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="6514c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6514c-117">Remarks</span></span>

<span data-ttu-id="6514c-118">Siehe [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) , um das Gesicht zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6514c-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="6514c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6514c-119">Requirements</span></span>



| <span data-ttu-id="6514c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6514c-120">Requirement</span></span> | <span data-ttu-id="6514c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6514c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6514c-122">Header</span><span class="sxs-lookup"><span data-stu-id="6514c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6514c-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6514c-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="6514c-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6514c-124">Library</span></span><br/> | <dl> <span data-ttu-id="6514c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6514c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6514c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6514c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6514c-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="6514c-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="6514c-128">**ID3DXRenderToEnvMap:: End**</span><span class="sxs-lookup"><span data-stu-id="6514c-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
