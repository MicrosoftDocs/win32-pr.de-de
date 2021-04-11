---
description: Ruft einen Scheitelpunkt-Shader ab.
ms.assetid: ab58b465-7b10-46eb-88c0-c5229cb09481
title: 'ID3DXBaseEffect:: getvertexshader-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ad6bb7cbf7c483ccaffa83b0e828c867026957fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132288"
---
# <a name="id3dxbaseeffectgetvertexshader-method"></a><span data-ttu-id="e923e-103">ID3DXBaseEffect:: getvertexshader-Methode</span><span class="sxs-lookup"><span data-stu-id="e923e-103">ID3DXBaseEffect::GetVertexShader method</span></span>

<span data-ttu-id="e923e-104">Ruft einen Scheitelpunkt-Shader ab.</span><span class="sxs-lookup"><span data-stu-id="e923e-104">Gets a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e923e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e923e-105">Syntax</span></span>


```C++
HRESULT GetVertexShader(
  [in]  D3DXHANDLE              hParameter,
  [out] LPDIRECT3DVERTEXSHADER9 *ppVShader
);
```



## <a name="parameters"></a><span data-ttu-id="e923e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e923e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e923e-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e923e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e923e-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e923e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e923e-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e923e-109">Unique identifier.</span></span> <span data-ttu-id="e923e-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e923e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e923e-111">*ppvshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e923e-111">*ppVShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e923e-112">Typ: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span><span class="sxs-lookup"><span data-stu-id="e923e-112">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span></span>

<span data-ttu-id="e923e-113">Gibt ein Vertex-Shader-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e923e-113">Returns a vertex shader object.</span></span> <span data-ttu-id="e923e-114">Siehe [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="e923e-114">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e923e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e923e-115">Return value</span></span>

<span data-ttu-id="e923e-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e923e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e923e-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e923e-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e923e-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e923e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e923e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e923e-119">Requirements</span></span>



| <span data-ttu-id="e923e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e923e-120">Requirement</span></span> | <span data-ttu-id="e923e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e923e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e923e-122">Header</span><span class="sxs-lookup"><span data-stu-id="e923e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e923e-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e923e-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e923e-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e923e-124">Library</span></span><br/> | <dl> <span data-ttu-id="e923e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e923e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e923e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e923e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e923e-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e923e-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
