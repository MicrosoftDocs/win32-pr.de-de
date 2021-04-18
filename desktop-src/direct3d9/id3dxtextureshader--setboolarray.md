---
description: Legt ein Array von booleschen Werten fest.
ms.assetid: d168d362-86b3-4db4-bc52-748a640ebc18
title: 'ID3DXTextureShader:: setboolarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0799e4ef9d35a886e59fae44c37a841bcda3aed6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351979"
---
# <a name="id3dxtextureshadersetboolarray-method"></a><span data-ttu-id="026cb-103">ID3DXTextureShader:: setboolarray-Methode</span><span class="sxs-lookup"><span data-stu-id="026cb-103">ID3DXTextureShader::SetBoolArray method</span></span>

<span data-ttu-id="026cb-104">Legt ein Array von booleschen Werten fest.</span><span class="sxs-lookup"><span data-stu-id="026cb-104">Sets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="026cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="026cb-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       D3DXHANDLE hConstant,
  [in] const BOOL       *pB,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="026cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="026cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="026cb-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="026cb-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026cb-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="026cb-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="026cb-109">Eindeutiger Bezeichner für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="026cb-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="026cb-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="026cb-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="026cb-111">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="026cb-111">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026cb-112">Typ: Konstante **[**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="026cb-112">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="026cb-113">Array von booleschen Werten.</span><span class="sxs-lookup"><span data-stu-id="026cb-113">Array of BOOL values.</span></span>

</dd> <dt>

<span data-ttu-id="026cb-114">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="026cb-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="026cb-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="026cb-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="026cb-116">Anzahl von booleschen Werten im Array.</span><span class="sxs-lookup"><span data-stu-id="026cb-116">Number of BOOL values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="026cb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="026cb-117">Return value</span></span>

<span data-ttu-id="026cb-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="026cb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="026cb-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="026cb-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="026cb-120">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="026cb-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="026cb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="026cb-121">Requirements</span></span>



| <span data-ttu-id="026cb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="026cb-122">Requirement</span></span> | <span data-ttu-id="026cb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="026cb-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="026cb-124">Header</span><span class="sxs-lookup"><span data-stu-id="026cb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="026cb-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="026cb-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="026cb-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="026cb-126">Library</span></span><br/> | <dl> <span data-ttu-id="026cb-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="026cb-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="026cb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="026cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026cb-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="026cb-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
