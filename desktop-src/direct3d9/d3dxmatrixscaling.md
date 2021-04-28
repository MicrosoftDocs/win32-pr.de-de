---
description: 'D3DXMatrixScaling-Funktion (D3dx9math.h): Erstellt eine Matrix, die entlang der X-Achse, der y-Achse und der Z-Achse skaliert wird.'
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: D3DXMatrixScaling-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ccd4cc6207bb211259833d163793c3499b51a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118068"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a><span data-ttu-id="c1d42-103">D3DXMatrixScaling-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c1d42-103">D3DXMatrixScaling function (D3dx9math.h)</span></span>

<span data-ttu-id="c1d42-104">Erstellt eine Matrix, die entlang der x-Achse, der y-Achse und der Z-Achse skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="c1d42-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1d42-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="c1d42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1d42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d42-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c1d42-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d42-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1d42-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1d42-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c1d42-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c1d42-110">*sx* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c1d42-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d42-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1d42-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1d42-112">Skalierungsfaktor, der entlang der X-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1d42-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c1d42-113">*sy* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c1d42-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d42-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1d42-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1d42-115">Skalierungsfaktor, der entlang der y-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1d42-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c1d42-116">*sz* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c1d42-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d42-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1d42-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1d42-118">Skalierungsfaktor, der entlang der Z-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1d42-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d42-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1d42-119">Return value</span></span>

<span data-ttu-id="c1d42-120">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c1d42-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c1d42-121">Zeiger auf die Skalierungstransformation [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c1d42-121">Pointer to the scaling transformation [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1d42-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1d42-122">Remarks</span></span>

<span data-ttu-id="c1d42-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="c1d42-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c1d42-124">Auf diese Weise kann die **D3DXMatrixScaling-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1d42-124">In this way, the **D3DXMatrixScaling** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d42-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1d42-125">Requirements</span></span>



| <span data-ttu-id="c1d42-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1d42-126">Requirement</span></span> | <span data-ttu-id="c1d42-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c1d42-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d42-128">Header</span><span class="sxs-lookup"><span data-stu-id="c1d42-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c1d42-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c1d42-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c1d42-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1d42-130">Library</span></span><br/> | <dl> <span data-ttu-id="c1d42-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1d42-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1d42-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c1d42-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d42-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c1d42-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
