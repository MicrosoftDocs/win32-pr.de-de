---
description: Generiert eine Ausgabe-Scheitelpunkt Deklaration aus der Eingabe Deklaration. Die Ausgabe Deklaration ist für die Verwendung durch die Gitter Mosaik Funktionen vorgesehen.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: D3DXGenerateOutputDecl-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355010"
---
# <a name="d3dxgenerateoutputdecl-function"></a><span data-ttu-id="30e32-104">D3DXGenerateOutputDecl-Funktion</span><span class="sxs-lookup"><span data-stu-id="30e32-104">D3DXGenerateOutputDecl function</span></span>

<span data-ttu-id="30e32-105">Generiert eine Ausgabe-Scheitelpunkt Deklaration aus der Eingabe Deklaration.</span><span class="sxs-lookup"><span data-stu-id="30e32-105">Generates an output vertex declaration from the input declaration.</span></span> <span data-ttu-id="30e32-106">Die Ausgabe Deklaration ist für die Verwendung durch die Gitter Mosaik Funktionen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="30e32-106">The output declaration is intended for use by the mesh tessellation functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="30e32-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30e32-107">Syntax</span></span>


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="30e32-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="30e32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e32-109">*poutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="30e32-109">*pOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30e32-110">Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span><span class="sxs-lookup"><span data-stu-id="30e32-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="30e32-111">Zeiger zur Ausgabe Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="30e32-111">Pointer to the output vertex declaration.</span></span> <span data-ttu-id="30e32-112">Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="30e32-112">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="30e32-113">*pinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30e32-113">*pInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30e32-114">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="30e32-114">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="30e32-115">Ein Zeiger auf die Deklaration der Eingabe Vertex.</span><span class="sxs-lookup"><span data-stu-id="30e32-115">Pointer to the input vertex declaration.</span></span> <span data-ttu-id="30e32-116">Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="30e32-116">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e32-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30e32-117">Return value</span></span>

<span data-ttu-id="30e32-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30e32-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30e32-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30e32-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30e32-120">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="30e32-120">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e32-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30e32-121">Requirements</span></span>



| <span data-ttu-id="30e32-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30e32-122">Requirement</span></span> | <span data-ttu-id="30e32-123">Wert</span><span class="sxs-lookup"><span data-stu-id="30e32-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30e32-124">Header</span><span class="sxs-lookup"><span data-stu-id="30e32-124">Header</span></span><br/>  | <dl> <span data-ttu-id="30e32-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="30e32-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="30e32-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30e32-126">Library</span></span><br/> | <dl> <span data-ttu-id="30e32-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30e32-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30e32-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30e32-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e32-129">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="30e32-129">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




