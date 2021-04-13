---
description: Initiieren des Renderings einer kugelförmigen Umgebungs Zuordnung.
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap:: beginsphere-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354567"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a><span data-ttu-id="1a2f1-103">ID3DXRenderToEnvMap:: beginsphere-Methode</span><span class="sxs-lookup"><span data-stu-id="1a2f1-103">ID3DXRenderToEnvMap::BeginSphere method</span></span>

<span data-ttu-id="1a2f1-104">Initiieren des Renderings einer kugelförmigen Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1a2f1-104">Initiate the rendering of a spherical environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a2f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a2f1-105">Syntax</span></span>


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a><span data-ttu-id="1a2f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a2f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a2f1-107">*ptex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a2f1-107">*pTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a2f1-108">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="1a2f1-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="1a2f1-109">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die Textur darstellt, in die gerbt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a2f1-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a2f1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a2f1-110">Return value</span></span>

<span data-ttu-id="1a2f1-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1a2f1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1a2f1-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1a2f1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1a2f1-113">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall. E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="1a2f1-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="1a2f1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a2f1-114">Remarks</span></span>

<span data-ttu-id="1a2f1-115">Siehe [**ID3DXRenderToEnvMap:: Face**](id3dxrendertoenvmap--face.md) , um das Gesicht zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1a2f1-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a2f1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a2f1-116">Requirements</span></span>



| <span data-ttu-id="1a2f1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a2f1-117">Requirement</span></span> | <span data-ttu-id="1a2f1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1a2f1-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a2f1-119">Header</span><span class="sxs-lookup"><span data-stu-id="1a2f1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1a2f1-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a2f1-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1a2f1-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a2f1-121">Library</span></span><br/> | <dl> <span data-ttu-id="1a2f1-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a2f1-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a2f1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a2f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a2f1-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="1a2f1-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="1a2f1-125">**ID3DXRenderToEnvMap:: End**</span><span class="sxs-lookup"><span data-stu-id="1a2f1-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
