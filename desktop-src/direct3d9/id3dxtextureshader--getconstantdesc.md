---
description: Ruft einen Zeiger auf das Array von Konstanten in der Konstanten Tabelle ab.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'ID3DXTextureShader:: getconstantdesc-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364384"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a><span data-ttu-id="e69fa-103">ID3DXTextureShader:: getconstantdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="e69fa-103">ID3DXTextureShader::GetConstantDesc method</span></span>

<span data-ttu-id="e69fa-104">Ruft einen Zeiger auf das Array von Konstanten in der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="e69fa-104">Gets a pointer to the array of constants in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e69fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e69fa-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="e69fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e69fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e69fa-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e69fa-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e69fa-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e69fa-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e69fa-109">Eindeutiger Bezeichner für eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="e69fa-109">Unique identifier to a constant.</span></span> <span data-ttu-id="e69fa-110">Siehe [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e69fa-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e69fa-111">*PDE SC* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e69fa-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e69fa-112">Typ: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="e69fa-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="e69fa-113">Gibt einen Zeiger auf ein Array von Beschreibungen zurück.</span><span class="sxs-lookup"><span data-stu-id="e69fa-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="e69fa-114">Weitere Informationen finden Sie unter [**D3DXCONSTANT \_**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="e69fa-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="e69fa-115">*pcount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e69fa-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e69fa-116">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e69fa-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e69fa-117">Die angegebene Eingabe muss die maximale Größe des Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="e69fa-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="e69fa-118">Bei der Ausgabe handelt es sich um die Anzahl der Elemente, die im Array aufgefüllt werden, wenn die Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e69fa-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e69fa-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e69fa-119">Return value</span></span>

<span data-ttu-id="e69fa-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e69fa-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e69fa-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e69fa-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e69fa-122">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="e69fa-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e69fa-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e69fa-123">Remarks</span></span>

<span data-ttu-id="e69fa-124">Samplers können mehr als einmal in einer Konstanten Tabelle vorkommen. Daher kann diese Methode ein Array von Beschreibungen mit jeweils einem anderen Register Index zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e69fa-124">Samplers can appear more than once in a constant table, therefore, this method can return an array of descriptions each with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="e69fa-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e69fa-125">Requirements</span></span>



| <span data-ttu-id="e69fa-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e69fa-126">Requirement</span></span> | <span data-ttu-id="e69fa-127">Wert</span><span class="sxs-lookup"><span data-stu-id="e69fa-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69fa-128">Header</span><span class="sxs-lookup"><span data-stu-id="e69fa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e69fa-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e69fa-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e69fa-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e69fa-130">Library</span></span><br/> | <dl> <span data-ttu-id="e69fa-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e69fa-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e69fa-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e69fa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69fa-133">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e69fa-133">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> <dt>

[<span data-ttu-id="e69fa-134">**ID3DXTextureShader:: getdebug**</span><span class="sxs-lookup"><span data-stu-id="e69fa-134">**ID3DXTextureShader::GetDesc**</span></span>](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
