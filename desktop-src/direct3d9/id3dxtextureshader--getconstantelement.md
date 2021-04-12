---
description: Eine Konstante aus der Konstanten Tabelle erhalten.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'ID3DXTextureShader:: getconstantelements-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219541"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a><span data-ttu-id="d95fa-103">ID3DXTextureShader:: getconstantelements-Methode</span><span class="sxs-lookup"><span data-stu-id="d95fa-103">ID3DXTextureShader::GetConstantElement method</span></span>

<span data-ttu-id="d95fa-104">Eine Konstante aus der Konstanten Tabelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="d95fa-104">Get a constant from the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d95fa-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="d95fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d95fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d95fa-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d95fa-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95fa-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d95fa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d95fa-109">Ein [handle](handles.md) für das Array von Konstanten.</span><span class="sxs-lookup"><span data-stu-id="d95fa-109">A [handle](handles.md) to the array of constants.</span></span> <span data-ttu-id="d95fa-110">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d95fa-110">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d95fa-111">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d95fa-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d95fa-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d95fa-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d95fa-113">NULL basierter Index des Elements in der Konstanten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d95fa-113">Zero-based index of the element in the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d95fa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d95fa-114">Return value</span></span>

<span data-ttu-id="d95fa-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d95fa-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d95fa-116">Gibt einen eindeutigen Bezeichner für die Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="d95fa-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="d95fa-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d95fa-117">Remarks</span></span>

<span data-ttu-id="d95fa-118">Verwenden Sie [**ID3DXTextureShader:: getconstant**](id3dxtextureshader--getconstant.md) oder [**ID3DXTextureShader:: getconstantbyname**](id3dxtextureshader--getconstantbyname.md), um eine Konstante zu erhalten, die nicht Teil eines Arrays ist.</span><span class="sxs-lookup"><span data-stu-id="d95fa-118">To get a constant that is not part of an array, use [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) or [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d95fa-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d95fa-119">Requirements</span></span>



| <span data-ttu-id="d95fa-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d95fa-120">Requirement</span></span> | <span data-ttu-id="d95fa-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d95fa-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d95fa-122">Header</span><span class="sxs-lookup"><span data-stu-id="d95fa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d95fa-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d95fa-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d95fa-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d95fa-124">Library</span></span><br/> | <dl> <span data-ttu-id="d95fa-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d95fa-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d95fa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d95fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95fa-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d95fa-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
