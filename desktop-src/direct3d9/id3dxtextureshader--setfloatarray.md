---
description: Legt ein Array von Gleit Komma Zahlen fest.
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: 'ID3DXTextureShader:: setfloatarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dbd39e8a4acfa004fb623d578e5922d477884fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219539"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="c40ed-103">ID3DXTextureShader:: setfloatarray-Methode</span><span class="sxs-lookup"><span data-stu-id="c40ed-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="c40ed-104">Legt ein Array von Gleit Komma Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="c40ed-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c40ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c40ed-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c40ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c40ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c40ed-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c40ed-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c40ed-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c40ed-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c40ed-109">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="c40ed-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="c40ed-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c40ed-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c40ed-111">*PF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c40ed-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c40ed-112">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c40ed-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c40ed-113">Array von Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="c40ed-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="c40ed-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c40ed-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c40ed-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c40ed-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c40ed-116">Anzahl von Gleit Komma Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="c40ed-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c40ed-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c40ed-117">Return value</span></span>

<span data-ttu-id="c40ed-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c40ed-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c40ed-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c40ed-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c40ed-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c40ed-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c40ed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c40ed-121">Requirements</span></span>



| <span data-ttu-id="c40ed-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c40ed-122">Requirement</span></span> | <span data-ttu-id="c40ed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c40ed-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c40ed-124">Header</span><span class="sxs-lookup"><span data-stu-id="c40ed-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c40ed-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c40ed-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c40ed-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c40ed-126">Library</span></span><br/> | <dl> <span data-ttu-id="c40ed-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c40ed-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c40ed-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c40ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c40ed-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c40ed-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
