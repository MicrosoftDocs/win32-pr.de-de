---
description: Gibt einen Deklarator aus einem flexiblen Scheitelpunkt Formatierungs Code (FVF) zurück.
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: D3DXDeclaratorFromFVF-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366466"
---
# <a name="d3dxdeclaratorfromfvf-function"></a><span data-ttu-id="623d4-103">D3DXDeclaratorFromFVF-Funktion</span><span class="sxs-lookup"><span data-stu-id="623d4-103">D3DXDeclaratorFromFVF function</span></span>

<span data-ttu-id="623d4-104">Gibt einen Deklarator aus einem flexiblen Scheitelpunkt Formatierungs Code (FVF) zurück.</span><span class="sxs-lookup"><span data-stu-id="623d4-104">Returns a declarator from a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="623d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="623d4-105">Syntax</span></span>


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="623d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="623d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="623d4-107">*F-VF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="623d4-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="623d4-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="623d4-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="623d4-109">Eine Kombination aus [D3DFVF](d3dfvf.md) , die die FVF beschreibt, aus der das zurückgegebene deklaratorarray generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="623d4-109">Combination of [D3DFVF](d3dfvf.md) that describes the FVF from which to generate the returned declarator array.</span></span>

</dd> <dt>

<span data-ttu-id="623d4-110">*Deklaration* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="623d4-110">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="623d4-111">Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="623d4-111">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="623d4-112">Ein Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format der Mesh-Scheitel Punkte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="623d4-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="623d4-113">Die Obergrenze dieses deklaratorarrays ist [**Max \_ \_ \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="623d4-113">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="623d4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="623d4-114">Return value</span></span>

<span data-ttu-id="623d4-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="623d4-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="623d4-116">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="623d4-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="623d4-117">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXERR \_ invalidmesh.</span><span class="sxs-lookup"><span data-stu-id="623d4-117">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="623d4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="623d4-118">Requirements</span></span>



| <span data-ttu-id="623d4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="623d4-119">Requirement</span></span> | <span data-ttu-id="623d4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="623d4-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="623d4-121">Header</span><span class="sxs-lookup"><span data-stu-id="623d4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="623d4-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="623d4-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="623d4-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="623d4-123">Library</span></span><br/> | <dl> <span data-ttu-id="623d4-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="623d4-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="623d4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="623d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="623d4-126">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="623d4-126">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="623d4-127">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="623d4-127">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
