---
description: Ruft eine Konstante ab, indem ihr Index gesucht wird.
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: 'ID3DXTextureShader:: getconstant-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 24f3f78d5970d5e3beda119ca40a565f45d0d950
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365335"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="34916-103">ID3DXTextureShader:: getconstant-Methode</span><span class="sxs-lookup"><span data-stu-id="34916-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="34916-104">Ruft eine Konstante ab, indem ihr Index gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="34916-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="34916-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34916-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="34916-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34916-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34916-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34916-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34916-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="34916-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="34916-109">Ein [handle](handles.md) für die übergeordnete Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="34916-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="34916-110">Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **null**.</span><span class="sxs-lookup"><span data-stu-id="34916-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34916-111">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34916-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34916-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34916-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="34916-113">NULL basierter Index der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="34916-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34916-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34916-114">Return value</span></span>

<span data-ttu-id="34916-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="34916-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="34916-116">Gibt einen eindeutigen Bezeichner für die Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="34916-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="34916-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34916-117">Remarks</span></span>

<span data-ttu-id="34916-118">Um eine Konstante von einem Array von Konstanten zu erhalten, verwenden Sie [**ID3DXTextureShader:: getconstantelements**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="34916-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34916-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34916-119">Requirements</span></span>



| <span data-ttu-id="34916-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34916-120">Requirement</span></span> | <span data-ttu-id="34916-121">Wert</span><span class="sxs-lookup"><span data-stu-id="34916-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34916-122">Header</span><span class="sxs-lookup"><span data-stu-id="34916-122">Header</span></span><br/>  | <dl> <span data-ttu-id="34916-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="34916-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="34916-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34916-124">Library</span></span><br/> | <dl> <span data-ttu-id="34916-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34916-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="34916-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34916-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34916-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="34916-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
