---
description: Transformiert den Vektor (x, y, z, 1) durch eine angegebene Matrix.
ms.assetid: 5b290c4c-22f1-4086-8e5e-f995757ef193
title: D3DXVec3Transform-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b653eeb7ea3797a3c385efda73ac974e2f4fbd97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355967"
---
# <a name="d3dxvec3transform-function-d3dx9mathh"></a><span data-ttu-id="9155a-103">D3DXVec3Transform-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9155a-103">D3DXVec3Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="9155a-104">Transformiert den Vektor (x, y, z, 1) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="9155a-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9155a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9155a-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="9155a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9155a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9155a-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9155a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9155a-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="9155a-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="9155a-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="9155a-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9155a-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9155a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9155a-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9155a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="9155a-112">Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9155a-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9155a-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9155a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9155a-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9155a-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9155a-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9155a-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9155a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9155a-116">Return value</span></span>

<span data-ttu-id="9155a-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="9155a-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="9155a-118">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="9155a-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="9155a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9155a-119">Remarks</span></span>

<span data-ttu-id="9155a-120">Diese Funktion wandelt den Vektor, *PV* (x, y, z, 1), durch die Matrix *pm* um.</span><span class="sxs-lookup"><span data-stu-id="9155a-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix *pM*.</span></span>

<span data-ttu-id="9155a-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9155a-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9155a-122">Auf diese Weise kann die **D3DXVec3Transform** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9155a-122">In this way, the **D3DXVec3Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9155a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9155a-123">Requirements</span></span>



| <span data-ttu-id="9155a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9155a-124">Requirement</span></span> | <span data-ttu-id="9155a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9155a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9155a-126">Header</span><span class="sxs-lookup"><span data-stu-id="9155a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9155a-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9155a-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9155a-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9155a-128">Library</span></span><br/> | <dl> <span data-ttu-id="9155a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9155a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9155a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9155a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9155a-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9155a-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




