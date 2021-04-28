---
description: 'D3DXVec2TransformCoord-Funktion (D3dx9math.h): Transformiert einen 2D-Vektor durch eine bestimmte Matrix und projektiert das Ergebnis zurück in w = 1.'
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: D3DXVec2TransformCoord-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 717af9eed2c7cedae7ac292a19239e13521dfa74
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115668"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a><span data-ttu-id="6b39f-103">D3DXVec2TransformCoord-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6b39f-103">D3DXVec2TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="6b39f-104">Transformiert einen 2D-Vektor durch eine bestimmte Matrix und projektiert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="6b39f-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b39f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b39f-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6b39f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b39f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b39f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6b39f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b39f-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b39f-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6b39f-109">Zeiger auf die [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6b39f-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6b39f-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6b39f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b39f-111">Typ: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b39f-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6b39f-112">Zeiger auf die [**D3DXVECTOR2-Quellstruktur.**](d3dxvector2.md)</span><span class="sxs-lookup"><span data-stu-id="6b39f-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6b39f-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6b39f-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b39f-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b39f-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6b39f-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="6b39f-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b39f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b39f-116">Return value</span></span>

<span data-ttu-id="6b39f-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b39f-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6b39f-118">Zeiger auf eine [**D3DXVECTOR2-Struktur,**](d3dxvector2.md) die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="6b39f-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b39f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b39f-119">Remarks</span></span>

<span data-ttu-id="6b39f-120">Diese Funktion transformiert den Vektor *pV* (x, y, 0, 1) durch die Matrix *pM* und pro projectiert das Ergebnis wieder in w=1.</span><span class="sxs-lookup"><span data-stu-id="6b39f-120">This function transforms the vector, *pV* (x, y, 0, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="6b39f-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="6b39f-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6b39f-122">Auf diese Weise kann die **D3DXVec2TransformCoord-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b39f-122">In this way, the **D3DXVec2TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b39f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b39f-123">Requirements</span></span>



| <span data-ttu-id="6b39f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b39f-124">Requirement</span></span> | <span data-ttu-id="6b39f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6b39f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b39f-126">Header</span><span class="sxs-lookup"><span data-stu-id="6b39f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6b39f-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6b39f-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6b39f-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b39f-128">Library</span></span><br/> | <dl> <span data-ttu-id="6b39f-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b39f-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b39f-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b39f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b39f-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6b39f-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6b39f-132">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="6b39f-132">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="6b39f-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="6b39f-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




