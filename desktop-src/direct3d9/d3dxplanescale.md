---
description: Skalieren Sie die Ebene mit dem angegebenen Skalierungsfaktor.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: D3DXPlaneScale-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354980"
---
# <a name="d3dxplanescale-function"></a><span data-ttu-id="b12c7-103">D3DXPlaneScale-Funktion</span><span class="sxs-lookup"><span data-stu-id="b12c7-103">D3DXPlaneScale function</span></span>

<span data-ttu-id="b12c7-104">Skalieren Sie die Ebene mit dem angegebenen Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="b12c7-104">Scale the plane with the given scaling factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b12c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b12c7-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="b12c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b12c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b12c7-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b12c7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b12c7-108">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="b12c7-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="b12c7-109">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="b12c7-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b12c7-110">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b12c7-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b12c7-111">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="b12c7-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="b12c7-112">Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b12c7-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b12c7-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b12c7-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b12c7-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b12c7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b12c7-115">Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="b12c7-115">Scale factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b12c7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b12c7-116">Return value</span></span>

<span data-ttu-id="b12c7-117">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="b12c7-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="b12c7-118">Zeiger auf eine [**D3DXPLANE**](d3dxplane.md) -Struktur, die die skalierte Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="b12c7-118">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the scaled plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="b12c7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b12c7-119">Remarks</span></span>

<span data-ttu-id="b12c7-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b12c7-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b12c7-121">Daher kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b12c7-121">Therefore, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12c7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b12c7-122">Requirements</span></span>



| <span data-ttu-id="b12c7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b12c7-123">Requirement</span></span> | <span data-ttu-id="b12c7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b12c7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b12c7-125">Header</span><span class="sxs-lookup"><span data-stu-id="b12c7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b12c7-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b12c7-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b12c7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b12c7-127">Library</span></span><br/> | <dl> <span data-ttu-id="b12c7-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b12c7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b12c7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b12c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b12c7-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b12c7-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
