---
description: 'D3DXVec2Transform-Funktion (D3dx9math.h): Transformiert einen 2D-Vektor durch eine bestimmte Matrix.'
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: D3DXVec2Transform-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097948"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="28297-103">D3DXVec2Transform-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="28297-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="28297-104">Transformiert einen 2D-Vektor durch eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="28297-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="28297-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28297-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="28297-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28297-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28297-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28297-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="28297-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="28297-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="28297-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="28297-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="28297-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28297-111">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="28297-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="28297-112">Zeiger auf die [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="28297-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28297-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="28297-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28297-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="28297-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28297-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="28297-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28297-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28297-116">Return value</span></span>

<span data-ttu-id="28297-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="28297-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="28297-118">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="28297-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="28297-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28297-119">Remarks</span></span>

<span data-ttu-id="28297-120">Diese Funktion transformiert den *Vektor pV* (x, y, 0, 1) durch die *Matrix pM.*</span><span class="sxs-lookup"><span data-stu-id="28297-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="28297-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="28297-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="28297-122">Auf diese Weise kann die **D3DXVec2Transform-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28297-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28297-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28297-123">Requirements</span></span>



| <span data-ttu-id="28297-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28297-124">Requirement</span></span> | <span data-ttu-id="28297-125">Wert</span><span class="sxs-lookup"><span data-stu-id="28297-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28297-126">Header</span><span class="sxs-lookup"><span data-stu-id="28297-126">Header</span></span><br/>  | <dl> <span data-ttu-id="28297-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="28297-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="28297-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28297-128">Library</span></span><br/> | <dl> <span data-ttu-id="28297-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="28297-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28297-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="28297-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28297-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="28297-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="28297-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="28297-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="28297-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="28297-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




