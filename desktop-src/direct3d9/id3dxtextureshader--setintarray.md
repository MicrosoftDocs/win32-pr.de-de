---
description: Legt ein Array von ganzen Zahlen fest.
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: 'ID3DXTextureShader:: tartintarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2e43ac1451ec776339d7aba1a4b0288e948f43d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365315"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="c3201-103">ID3DXTextureShader:: tartintarray-Methode</span><span class="sxs-lookup"><span data-stu-id="c3201-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="c3201-104">Legt ein Array von ganzen Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="c3201-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3201-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3201-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="c3201-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3201-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3201-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3201-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c3201-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c3201-109">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="c3201-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="c3201-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="c3201-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3201-111">*PN* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3201-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3201-112">Typ: Konstante **[**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c3201-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3201-113">Array von ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="c3201-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="c3201-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3201-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3201-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3201-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3201-116">Anzahl von ganzen Zahlen im Array.</span><span class="sxs-lookup"><span data-stu-id="c3201-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3201-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3201-117">Return value</span></span>

<span data-ttu-id="c3201-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3201-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3201-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3201-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3201-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c3201-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3201-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3201-121">Requirements</span></span>



| <span data-ttu-id="c3201-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3201-122">Requirement</span></span> | <span data-ttu-id="c3201-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c3201-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3201-124">Header</span><span class="sxs-lookup"><span data-stu-id="c3201-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c3201-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3201-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c3201-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3201-126">Library</span></span><br/> | <dl> <span data-ttu-id="c3201-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3201-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c3201-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3201-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3201-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="c3201-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
