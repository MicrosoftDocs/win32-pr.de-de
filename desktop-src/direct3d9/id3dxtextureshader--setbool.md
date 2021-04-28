---
description: 'ID3DXTextureShader::SetBool-Methode: Legt einen BOOL-Wert fest.'
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: ID3DXTextureShader::SetBool-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 512daf7e770c72fe038622877d1756a5fd3532bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117628"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="e837c-103">ID3DXTextureShader::SetBool-Methode</span><span class="sxs-lookup"><span data-stu-id="e837c-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="e837c-104">Legt einen BOOL-Wert fest.</span><span class="sxs-lookup"><span data-stu-id="e837c-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e837c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e837c-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="e837c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e837c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e837c-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e837c-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e837c-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e837c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e837c-109">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="e837c-109">Unique identifier to the constant.</span></span> <span data-ttu-id="e837c-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e837c-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e837c-111">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e837c-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e837c-112">Typ: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e837c-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e837c-113">BOOL-Wert.</span><span class="sxs-lookup"><span data-stu-id="e837c-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e837c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e837c-114">Return value</span></span>

<span data-ttu-id="e837c-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e837c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e837c-116">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e837c-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e837c-117">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="e837c-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e837c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e837c-118">Requirements</span></span>



| <span data-ttu-id="e837c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e837c-119">Requirement</span></span> | <span data-ttu-id="e837c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e837c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e837c-121">Header</span><span class="sxs-lookup"><span data-stu-id="e837c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e837c-122"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="e837c-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e837c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e837c-123">Library</span></span><br/> | <dl> <span data-ttu-id="e837c-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e837c-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e837c-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e837c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e837c-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e837c-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
