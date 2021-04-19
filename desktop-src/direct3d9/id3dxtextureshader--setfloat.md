---
description: Legt eine Gleit Komma Zahl fest.
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: 'ID3DXTextureShader:: SetFloat-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85923fe20731b4482f70c439cb9df75712ab09f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367476"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="1ef63-103">ID3DXTextureShader:: SetFloat-Methode</span><span class="sxs-lookup"><span data-stu-id="1ef63-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="1ef63-104">Legt eine Gleit Komma Zahl fest.</span><span class="sxs-lookup"><span data-stu-id="1ef63-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ef63-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="1ef63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ef63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef63-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ef63-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef63-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1ef63-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1ef63-109">Eindeutiger Bezeichner für die Konstante.</span><span class="sxs-lookup"><span data-stu-id="1ef63-109">Unique identifier to the constant.</span></span> <span data-ttu-id="1ef63-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="1ef63-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ef63-111">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ef63-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef63-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ef63-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ef63-113">Gleit Komma Zahl.</span><span class="sxs-lookup"><span data-stu-id="1ef63-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef63-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ef63-114">Return value</span></span>

<span data-ttu-id="1ef63-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ef63-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ef63-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ef63-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ef63-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="1ef63-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef63-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ef63-118">Requirements</span></span>



| <span data-ttu-id="1ef63-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ef63-119">Requirement</span></span> | <span data-ttu-id="1ef63-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1ef63-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef63-121">Header</span><span class="sxs-lookup"><span data-stu-id="1ef63-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1ef63-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ef63-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1ef63-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ef63-123">Library</span></span><br/> | <dl> <span data-ttu-id="1ef63-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ef63-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1ef63-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ef63-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef63-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="1ef63-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
