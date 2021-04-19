---
description: Ruft einen PixelShader ab.
ms.assetid: 173a20a5-dda0-493f-a161-2dc2881e71f2
title: 'ID3DXBaseEffect:: getpixelshader-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e555bac2e20ebab1cb0aec3d313cab8ad05e833e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364007"
---
# <a name="id3dxbaseeffectgetpixelshader-method"></a><span data-ttu-id="25c3d-103">ID3DXBaseEffect:: getpixelshader-Methode</span><span class="sxs-lookup"><span data-stu-id="25c3d-103">ID3DXBaseEffect::GetPixelShader method</span></span>

<span data-ttu-id="25c3d-104">Ruft einen PixelShader ab.</span><span class="sxs-lookup"><span data-stu-id="25c3d-104">Gets a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25c3d-105">Syntax</span></span>


```C++
HRESULT GetPixelShader(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DPIXELSHADER9 *ppPShader
);
```



## <a name="parameters"></a><span data-ttu-id="25c3d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25c3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c3d-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25c3d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c3d-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="25c3d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="25c3d-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="25c3d-109">Unique identifier.</span></span> <span data-ttu-id="25c3d-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="25c3d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="25c3d-111">*pppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="25c3d-111">*ppPShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25c3d-112">Typ: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span><span class="sxs-lookup"><span data-stu-id="25c3d-112">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span></span>

<span data-ttu-id="25c3d-113">Gibt ein Pixel-Shader-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="25c3d-113">Returns a pixel shader object.</span></span> <span data-ttu-id="25c3d-114">Siehe [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="25c3d-114">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c3d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25c3d-115">Return value</span></span>

<span data-ttu-id="25c3d-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25c3d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25c3d-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25c3d-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25c3d-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="25c3d-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c3d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25c3d-119">Requirements</span></span>



| <span data-ttu-id="25c3d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25c3d-120">Requirement</span></span> | <span data-ttu-id="25c3d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="25c3d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25c3d-122">Header</span><span class="sxs-lookup"><span data-stu-id="25c3d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="25c3d-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="25c3d-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="25c3d-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25c3d-124">Library</span></span><br/> | <dl> <span data-ttu-id="25c3d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25c3d-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="25c3d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25c3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c3d-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="25c3d-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
