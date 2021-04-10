---
description: Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstanten Tabelle ab.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'ID3DXConstantTable:: getconstantdesc-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961624"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a><span data-ttu-id="c1a0d-103">ID3DXConstantTable:: getconstantdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="c1a0d-103">ID3DXConstantTable::GetConstantDesc method</span></span>

<span data-ttu-id="c1a0d-104">Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-104">Gets a pointer to an array of constant descriptions in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1a0d-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="c1a0d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a0d-107">*hconstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1a0d-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a0d-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c1a0d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c1a0d-109">Eindeutiger Bezeichner für eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-109">Unique identifier to a constant.</span></span> <span data-ttu-id="c1a0d-110">Siehe [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c1a0d-110">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1a0d-111">*PDE SC* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c1a0d-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a0d-112">Typ: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1a0d-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="c1a0d-113">Gibt einen Zeiger auf ein Array von Beschreibungen zurück.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="c1a0d-114">Weitere Informationen finden Sie unter [**D3DXCONSTANT \_**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="c1a0d-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1a0d-115">*pcount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c1a0d-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a0d-116">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1a0d-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c1a0d-117">Die angegebene Eingabe muss die maximale Größe des Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="c1a0d-118">Bei der Ausgabe handelt es sich um die Anzahl der Elemente, die im Array aufgefüllt werden, wenn die Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a0d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1a0d-119">Return value</span></span>

<span data-ttu-id="c1a0d-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1a0d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1a0d-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1a0d-122">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a0d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1a0d-123">Remarks</span></span>

<span data-ttu-id="c1a0d-124">**ID3DXConstantTable:: getconstantdesc** gibt manchmal einen [**D3DXCONSTANT- \_**](d3dxconstant-desc.md) Wert mit \_ der Register Anzahl 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-124">**ID3DXConstantTable::GetConstantDesc** will sometimes return a [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md) with a Register\_Count of 0.</span></span> <span data-ttu-id="c1a0d-125">Dies geschieht, wenn eine Konstante in mehr als einem Register \_ Satz enthalten ist, aber keinen Platz in diesem zugeordneten Register Satz hat.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-125">This will happen with a constant appears in more than one Register\_Set but does not have space in that register set allocated.</span></span>

<span data-ttu-id="c1a0d-126">Da ein Sampler mehrmals in einer Konstanten Tabelle vorkommen kann, kann diese Methode ein Array von Beschreibungen zurückgeben, von denen jedes einen anderen Registrierungs Index hat.</span><span class="sxs-lookup"><span data-stu-id="c1a0d-126">Because a sampler can appear more than once in a constant table, this method can return an array of descriptions, each one with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1a0d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1a0d-127">Requirements</span></span>



| <span data-ttu-id="c1a0d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1a0d-128">Requirement</span></span> | <span data-ttu-id="c1a0d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c1a0d-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a0d-130">Header</span><span class="sxs-lookup"><span data-stu-id="c1a0d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c1a0d-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a0d-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c1a0d-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1a0d-132">Library</span></span><br/> | <dl> <span data-ttu-id="c1a0d-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1a0d-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c1a0d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1a0d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a0d-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="c1a0d-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="c1a0d-136">**ID3DXConstantTable:: getdebug**</span><span class="sxs-lookup"><span data-stu-id="c1a0d-136">**ID3DXConstantTable::GetDesc**</span></span>](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
