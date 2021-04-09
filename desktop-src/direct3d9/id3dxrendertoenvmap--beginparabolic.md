---
description: Initiieren des Renderings einer paramegigramm-Umgebungs Zuordnung.
ms.assetid: 80456084-f5f5-4dfe-805a-7eaaf7f7cb2a
title: 'ID3DXRenderToEnvMap:: beginsamabolic-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginParabolic
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5a818abb424fa55bc01eca7ce9f64bc5629a7d50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050844"
---
# <a name="id3dxrendertoenvmapbeginparabolic-method"></a><span data-ttu-id="a3471-103">ID3DXRenderToEnvMap:: beginsamabolic-Methode</span><span class="sxs-lookup"><span data-stu-id="a3471-103">ID3DXRenderToEnvMap::BeginParabolic method</span></span>

<span data-ttu-id="a3471-104">Initiieren des Renderings einer paramegigramm-Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a3471-104">Initiate the rendering of a parabolic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3471-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3471-105">Syntax</span></span>


```C++
HRESULT BeginParabolic(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="a3471-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3471-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3471-107">*ptexzpos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3471-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3471-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a3471-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a3471-109">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die positive Rendering-Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3471-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive render texture.</span></span>

</dd> <dt>

<span data-ttu-id="a3471-110">*ptexznetg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3471-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3471-111">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="a3471-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="a3471-112">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die negative Rendering-Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3471-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative render texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3471-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3471-113">Return value</span></span>

<span data-ttu-id="a3471-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3471-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3471-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3471-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3471-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall. E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="a3471-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="a3471-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3471-117">Remarks</span></span>

<span data-ttu-id="a3471-118">Siehe [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) zum Zeichnen der Flächen.</span><span class="sxs-lookup"><span data-stu-id="a3471-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3471-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3471-119">Requirements</span></span>



| <span data-ttu-id="a3471-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3471-120">Requirement</span></span> | <span data-ttu-id="a3471-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a3471-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3471-122">Header</span><span class="sxs-lookup"><span data-stu-id="a3471-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a3471-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3471-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a3471-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3471-124">Library</span></span><br/> | <dl> <span data-ttu-id="a3471-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3471-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3471-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3471-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3471-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a3471-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="a3471-128">**ID3DXRenderToEnvMap:: End**</span><span class="sxs-lookup"><span data-stu-id="a3471-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
