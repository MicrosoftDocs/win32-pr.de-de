---
description: 'D3DXVec3TransformCoord-Funktion (D3dx9math.h): Transformiert einen 3D-Vektor durch eine bestimmte Matrix und projektiert das Ergebnis zurück in w = 1.'
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: D3DXVec3TransformCoord-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4e3514d4717262a7afab7ae808d747de3a1b635
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115628"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="6e52a-103">D3DXVec3TransformCoord-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6e52a-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="6e52a-104">Transformiert einen 3D-Vektor durch eine bestimmte Matrix und projektiert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="6e52a-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e52a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e52a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6e52a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e52a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e52a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6e52a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e52a-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e52a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e52a-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6e52a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6e52a-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6e52a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e52a-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e52a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e52a-112">Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="6e52a-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6e52a-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6e52a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e52a-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e52a-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6e52a-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="6e52a-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e52a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e52a-116">Return value</span></span>

<span data-ttu-id="6e52a-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e52a-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e52a-118">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="6e52a-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e52a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e52a-119">Remarks</span></span>

<span data-ttu-id="6e52a-120">Diese Funktion transformiert den Vektor *pV* (x, y, z, 1) durch die Matrix *pM* und projektiert das Ergebnis wieder in w=1.</span><span class="sxs-lookup"><span data-stu-id="6e52a-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="6e52a-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="6e52a-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6e52a-122">Auf diese Weise kann die **D3DXVec3TransformCoord-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e52a-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e52a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e52a-123">Requirements</span></span>



| <span data-ttu-id="6e52a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e52a-124">Requirement</span></span> | <span data-ttu-id="6e52a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6e52a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e52a-126">Header</span><span class="sxs-lookup"><span data-stu-id="6e52a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6e52a-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6e52a-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6e52a-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6e52a-128">Library</span></span><br/> | <dl> <span data-ttu-id="6e52a-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e52a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e52a-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6e52a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e52a-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6e52a-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6e52a-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="6e52a-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="6e52a-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="6e52a-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




