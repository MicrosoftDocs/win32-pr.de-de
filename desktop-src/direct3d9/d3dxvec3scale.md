---
description: Skaliert einen 3D-Vektor.
ms.assetid: b2483d6e-56e4-4557-a603-d59c0767774d
title: D3DXVec3Scale-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5357b862b9cf82e458429edea27001163eb9635
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361248"
---
# <a name="d3dxvec3scale-function"></a><span data-ttu-id="a38b3-103">D3DXVec3Scale-Funktion</span><span class="sxs-lookup"><span data-stu-id="a38b3-103">D3DXVec3Scale function</span></span>

<span data-ttu-id="a38b3-104">Skaliert einen 3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="a38b3-104">Scales a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a38b3-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Scale(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="a38b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a38b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38b3-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a38b3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a38b3-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a38b3-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a38b3-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="a38b3-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a38b3-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a38b3-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38b3-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a38b3-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a38b3-112">Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a38b3-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a38b3-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a38b3-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a38b3-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a38b3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a38b3-115">Skalierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="a38b3-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38b3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a38b3-116">Return value</span></span>

<span data-ttu-id="a38b3-117">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a38b3-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a38b3-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die der skalierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="a38b3-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a38b3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a38b3-119">Remarks</span></span>

<span data-ttu-id="a38b3-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a38b3-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a38b3-121">Auf diese Weise kann die **D3DXVec3Scale** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a38b3-121">In this way, the **D3DXVec3Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38b3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a38b3-122">Requirements</span></span>



| <span data-ttu-id="a38b3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a38b3-123">Requirement</span></span> | <span data-ttu-id="a38b3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a38b3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a38b3-125">Header</span><span class="sxs-lookup"><span data-stu-id="a38b3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a38b3-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a38b3-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a38b3-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a38b3-127">Library</span></span><br/> | <dl> <span data-ttu-id="a38b3-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a38b3-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a38b3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a38b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38b3-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a38b3-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a38b3-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="a38b3-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="a38b3-132">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="a38b3-132">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> </dl>

 

 
