---
description: 'ID3DXTextureShader::SetMatrix-Methode: Legt eine nicht transponierte Matrix fest.'
ms.assetid: 891441ea-09d5-43b6-a080-578d7f8e4586
title: ID3DXTextureShader::SetMatrix-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15ba6b289ad106a8fad4a932b9c5d01e0a52dc18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090218"
---
# <a name="id3dxtextureshadersetmatrix-method"></a><span data-ttu-id="bceed-103">ID3DXTextureShader::SetMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="bceed-103">ID3DXTextureShader::SetMatrix method</span></span>

<span data-ttu-id="bceed-104">Legt eine nicht transponierte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="bceed-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="bceed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bceed-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hConstant,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="bceed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bceed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bceed-107">*hConstant* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bceed-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bceed-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bceed-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bceed-109">Eindeutiger Bezeichner für die Matrix der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="bceed-109">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="bceed-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="bceed-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="bceed-111">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bceed-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bceed-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bceed-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bceed-113">Zeiger auf eine nicht transponierte Matrix.</span><span class="sxs-lookup"><span data-stu-id="bceed-113">Pointer to a non-transposed matrix.</span></span> <span data-ttu-id="bceed-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="bceed-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bceed-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bceed-115">Return value</span></span>

<span data-ttu-id="bceed-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bceed-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bceed-117">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bceed-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bceed-118">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="bceed-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bceed-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bceed-119">Remarks</span></span>

<span data-ttu-id="bceed-120">Eine nicht transponierte Matrix enthält Zeilen-Hauptdaten. Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="bceed-120">A non-transposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="bceed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bceed-121">Requirements</span></span>



| <span data-ttu-id="bceed-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bceed-122">Requirement</span></span> | <span data-ttu-id="bceed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bceed-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bceed-124">Header</span><span class="sxs-lookup"><span data-stu-id="bceed-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bceed-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="bceed-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bceed-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bceed-126">Library</span></span><br/> | <dl> <span data-ttu-id="bceed-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bceed-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bceed-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bceed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bceed-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="bceed-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




