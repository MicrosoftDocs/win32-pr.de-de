---
description: Legt eine Textur fest.
ms.assetid: edf5bf61-508a-4417-bdf8-c36e6ba7ab30
title: 'ID3DXBaseEffect:: SetTexture-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 398dcc2f3d61ad32c08b67735a9ec7ed1a192acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366614"
---
# <a name="id3dxbaseeffectsettexture-method"></a><span data-ttu-id="5bfd6-103">ID3DXBaseEffect:: SetTexture-Methode</span><span class="sxs-lookup"><span data-stu-id="5bfd6-103">ID3DXBaseEffect::SetTexture method</span></span>

<span data-ttu-id="5bfd6-104">Legt eine Textur fest.</span><span class="sxs-lookup"><span data-stu-id="5bfd6-104">Sets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bfd6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bfd6-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] D3DXHANDLE             hParameter,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="5bfd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bfd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bfd6-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bfd6-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bfd6-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5bfd6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5bfd6-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5bfd6-109">Unique identifier.</span></span> <span data-ttu-id="5bfd6-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5bfd6-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bfd6-111">*ptexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bfd6-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bfd6-112">Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="5bfd6-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="5bfd6-113">Textur Objekt.</span><span class="sxs-lookup"><span data-stu-id="5bfd6-113">Texture object.</span></span> <span data-ttu-id="5bfd6-114">Siehe [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="5bfd6-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bfd6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bfd6-115">Return value</span></span>

<span data-ttu-id="5bfd6-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5bfd6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5bfd6-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5bfd6-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5bfd6-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="5bfd6-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bfd6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bfd6-119">Requirements</span></span>



| <span data-ttu-id="5bfd6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bfd6-120">Requirement</span></span> | <span data-ttu-id="5bfd6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5bfd6-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bfd6-122">Header</span><span class="sxs-lookup"><span data-stu-id="5bfd6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5bfd6-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bfd6-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5bfd6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5bfd6-124">Library</span></span><br/> | <dl> <span data-ttu-id="5bfd6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bfd6-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5bfd6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bfd6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bfd6-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5bfd6-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="5bfd6-128">**GetTexture**</span><span class="sxs-lookup"><span data-stu-id="5bfd6-128">**GetTexture**</span></span>](id3dxbaseeffect--gettexture.md)
</dt> </dl>

 

 
