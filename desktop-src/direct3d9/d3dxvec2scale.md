---
description: Skaliert einen 2D-Vektor.
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: D3DXVec2Scale-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354597"
---
# <a name="d3dxvec2scale-function"></a><span data-ttu-id="de4c1-103">D3DXVec2Scale-Funktion</span><span class="sxs-lookup"><span data-stu-id="de4c1-103">D3DXVec2Scale function</span></span>

<span data-ttu-id="de4c1-104">Skaliert einen 2D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="de4c1-104">Scales a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de4c1-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="de4c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de4c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4c1-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="de4c1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de4c1-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="de4c1-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="de4c1-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="de4c1-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="de4c1-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de4c1-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de4c1-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="de4c1-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="de4c1-112">Ein Zeiger auf die Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="de4c1-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="de4c1-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de4c1-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de4c1-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de4c1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de4c1-115">Skalierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="de4c1-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4c1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de4c1-116">Return value</span></span>

<span data-ttu-id="de4c1-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="de4c1-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="de4c1-118">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die der skalierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="de4c1-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="de4c1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de4c1-119">Remarks</span></span>

<span data-ttu-id="de4c1-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="de4c1-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="de4c1-121">Auf diese Weise kann die **D3DXVec2Scale** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de4c1-121">In this way, the **D3DXVec2Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4c1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de4c1-122">Requirements</span></span>



| <span data-ttu-id="de4c1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de4c1-123">Requirement</span></span> | <span data-ttu-id="de4c1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="de4c1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de4c1-125">Header</span><span class="sxs-lookup"><span data-stu-id="de4c1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="de4c1-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="de4c1-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="de4c1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de4c1-127">Library</span></span><br/> | <dl> <span data-ttu-id="de4c1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de4c1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de4c1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de4c1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4c1-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="de4c1-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="de4c1-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="de4c1-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="de4c1-132">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="de4c1-132">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> </dl>

 

 
