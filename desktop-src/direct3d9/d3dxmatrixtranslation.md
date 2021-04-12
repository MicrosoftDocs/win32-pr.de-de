---
description: Erstellt eine Matrix mithilfe der angegebenen Offsets.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: D3DXMatrixTranslation-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354786"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a><span data-ttu-id="dab09-103">D3DXMatrixTranslation-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="dab09-103">D3DXMatrixTranslation function (D3dx9math.h)</span></span>

<span data-ttu-id="dab09-104">Erstellt eine Matrix mithilfe der angegebenen Offsets.</span><span class="sxs-lookup"><span data-stu-id="dab09-104">Builds a matrix using the specified offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dab09-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="dab09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dab09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab09-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dab09-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dab09-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dab09-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dab09-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="dab09-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dab09-110">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab09-110">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab09-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dab09-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dab09-112">Offset der X-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="dab09-112">X-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="dab09-113">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab09-113">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab09-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dab09-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dab09-115">Offset der Y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="dab09-115">Y-coordinate offset.</span></span>

</dd> <dt>

<span data-ttu-id="dab09-116">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab09-116">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab09-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dab09-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dab09-118">Der Z-Koordinaten Offset.</span><span class="sxs-lookup"><span data-stu-id="dab09-118">Z-coordinate offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab09-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dab09-119">Return value</span></span>

<span data-ttu-id="dab09-120">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dab09-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dab09-121">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die eine übersetzte Transformationsmatrix enthält.</span><span class="sxs-lookup"><span data-stu-id="dab09-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that contains a translated transformation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab09-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dab09-122">Remarks</span></span>

<span data-ttu-id="dab09-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dab09-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="dab09-124">Auf diese Weise kann D3DXMATRIXTranslation als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dab09-124">In this way, the D3DXMATRIXTranslation can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dab09-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dab09-125">Requirements</span></span>



| <span data-ttu-id="dab09-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dab09-126">Requirement</span></span> | <span data-ttu-id="dab09-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dab09-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dab09-128">Header</span><span class="sxs-lookup"><span data-stu-id="dab09-128">Header</span></span><br/>  | <dl> <span data-ttu-id="dab09-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dab09-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dab09-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dab09-130">Library</span></span><br/> | <dl> <span data-ttu-id="dab09-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dab09-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dab09-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dab09-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab09-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="dab09-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
