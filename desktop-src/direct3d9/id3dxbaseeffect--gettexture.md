---
description: Ruft eine Textur ab.
ms.assetid: e009ccc2-4491-4976-9460-7478b2bd34c2
title: 'ID3DXBaseEffect:: GetTexture-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 25ef71df1f9dcd84bbe6726fd3a13f9ec09eff17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761943"
---
# <a name="id3dxbaseeffectgettexture-method"></a><span data-ttu-id="6b99e-103">ID3DXBaseEffect:: GetTexture-Methode</span><span class="sxs-lookup"><span data-stu-id="6b99e-103">ID3DXBaseEffect::GetTexture method</span></span>

<span data-ttu-id="6b99e-104">Ruft eine Textur ab.</span><span class="sxs-lookup"><span data-stu-id="6b99e-104">Gets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b99e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b99e-105">Syntax</span></span>


```C++
HRESULT GetTexture(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DBASETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="6b99e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b99e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b99e-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b99e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b99e-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6b99e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6b99e-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6b99e-109">Unique identifier.</span></span> <span data-ttu-id="6b99e-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6b99e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b99e-111">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b99e-111">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b99e-112">Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="6b99e-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="6b99e-113">Gibt ein Textur Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6b99e-113">Returns a texture object.</span></span> <span data-ttu-id="6b99e-114">Siehe [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="6b99e-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b99e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b99e-115">Return value</span></span>

<span data-ttu-id="6b99e-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b99e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b99e-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b99e-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6b99e-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="6b99e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b99e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b99e-119">Requirements</span></span>



| <span data-ttu-id="6b99e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b99e-120">Requirement</span></span> | <span data-ttu-id="6b99e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6b99e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b99e-122">Header</span><span class="sxs-lookup"><span data-stu-id="6b99e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6b99e-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b99e-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6b99e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b99e-124">Library</span></span><br/> | <dl> <span data-ttu-id="6b99e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b99e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6b99e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b99e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b99e-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6b99e-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="6b99e-128">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="6b99e-128">**SetTexture**</span></span>](id3dxbaseeffect--settexture.md)
</dt> </dl>

 

 
