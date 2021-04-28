---
description: 'ID3DXTextureShader::GetConstant-Methode: Ruft eine Konstante ab, indem ihr Index gesucht wird.'
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: ID3DXTextureShader::GetConstant-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117668"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="f45c5-103">ID3DXTextureShader::GetConstant-Methode</span><span class="sxs-lookup"><span data-stu-id="f45c5-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="f45c5-104">Ruft eine Konstante ab, indem ihr Index gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="f45c5-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f45c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f45c5-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="f45c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f45c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f45c5-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f45c5-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f45c5-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f45c5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f45c5-109">Ein [Handle](handles.md) für die übergeordnete Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="f45c5-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="f45c5-110">Wenn die Konstante ein Parameter der obersten Ebene ist (es gibt keine übergeordnete Datenstruktur), verwenden Sie **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f45c5-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f45c5-111">*Index* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f45c5-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f45c5-112">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f45c5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f45c5-113">Nullbasierter Index der Konstante.</span><span class="sxs-lookup"><span data-stu-id="f45c5-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f45c5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f45c5-114">Return value</span></span>

<span data-ttu-id="f45c5-115">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f45c5-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f45c5-116">Gibt einen eindeutigen Bezeichner an die Konstante zurück.</span><span class="sxs-lookup"><span data-stu-id="f45c5-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="f45c5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f45c5-117">Remarks</span></span>

<span data-ttu-id="f45c5-118">Um eine Konstante aus einem Array von Konstanten zu erhalten, verwenden Sie [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="f45c5-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f45c5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f45c5-119">Requirements</span></span>



| <span data-ttu-id="f45c5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f45c5-120">Requirement</span></span> | <span data-ttu-id="f45c5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f45c5-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f45c5-122">Header</span><span class="sxs-lookup"><span data-stu-id="f45c5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f45c5-123"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="f45c5-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f45c5-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f45c5-124">Library</span></span><br/> | <dl> <span data-ttu-id="f45c5-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f45c5-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f45c5-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f45c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f45c5-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="f45c5-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
