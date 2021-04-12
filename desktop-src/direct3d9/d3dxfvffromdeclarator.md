---
description: Gibt einen FVF-Code (Flexible Vertex-Format) aus einem Deklarator zurück.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: D3DXFVFFromDeclarator-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354837"
---
# <a name="d3dxfvffromdeclarator-function"></a><span data-ttu-id="7618c-103">D3DXFVFFromDeclarator-Funktion</span><span class="sxs-lookup"><span data-stu-id="7618c-103">D3DXFVFFromDeclarator function</span></span>

<span data-ttu-id="7618c-104">Gibt einen FVF-Code (Flexible Vertex-Format) aus einem Deklarator zurück.</span><span class="sxs-lookup"><span data-stu-id="7618c-104">Returns a flexible vertex format (FVF) code from a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="7618c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7618c-105">Syntax</span></span>


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a><span data-ttu-id="7618c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7618c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7618c-107">*pdeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7618c-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7618c-108">Typ: **Konstanten [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="7618c-108">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="7618c-109">Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das den Code für den Code von Code beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7618c-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the FVF code.</span></span>

</dd> <dt>

<span data-ttu-id="7618c-110">*pfvf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7618c-110">*pFVF* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7618c-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7618c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7618c-112">Ein Zeiger auf einen DWORD-Wert, der die zurückgegebene Kombination von [D3DFVF](d3dfvf.md) darstellt, die das vom Deklarator zurückgegebene Scheitelpunkt Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7618c-112">Pointer to a DWORD value, representing the returned combination of [D3DFVF](d3dfvf.md) that describes the vertex format returned from the declarator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7618c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7618c-113">Return value</span></span>

<span data-ttu-id="7618c-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7618c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7618c-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7618c-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7618c-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="7618c-116">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7618c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7618c-117">Remarks</span></span>

<span data-ttu-id="7618c-118">Diese Funktion kann für alle Deklaratoren, die nicht direkt einer FVF zugeordnet sind, nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7618c-118">This function will fail for any declarator that does not map directly to an FVF.</span></span>

## <a name="requirements"></a><span data-ttu-id="7618c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7618c-119">Requirements</span></span>



| <span data-ttu-id="7618c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7618c-120">Requirement</span></span> | <span data-ttu-id="7618c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7618c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7618c-122">Header</span><span class="sxs-lookup"><span data-stu-id="7618c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7618c-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7618c-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7618c-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7618c-124">Library</span></span><br/> | <dl> <span data-ttu-id="7618c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7618c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7618c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7618c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7618c-127">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7618c-127">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="7618c-128">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="7618c-128">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
