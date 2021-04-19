---
description: Normalisiert die ebenenkoeffizienten, sodass die Ebene normal über eine Einheitslänge verfügt.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: D3DXPlaneNormalize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366434"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="75167-103">D3DXPlaneNormalize-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="75167-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="75167-104">Normalisiert die ebenenkoeffizienten, sodass die Ebene normal über eine Einheitslänge verfügt.</span><span class="sxs-lookup"><span data-stu-id="75167-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="75167-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75167-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="75167-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75167-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75167-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="75167-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75167-108">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="75167-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="75167-109">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="75167-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="75167-110">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75167-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75167-111">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="75167-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="75167-112">Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="75167-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75167-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75167-113">Return value</span></span>

<span data-ttu-id="75167-114">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="75167-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="75167-115">Zeiger auf eine [**D3DXPLANE**](d3dxplane.md) -Struktur, die die normale der Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="75167-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="75167-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75167-116">Remarks</span></span>

<span data-ttu-id="75167-117">Diese Funktion normalisiert eine Ebene, sodass \| a, b, c \| = = 1 ist.</span><span class="sxs-lookup"><span data-stu-id="75167-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="75167-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="75167-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="75167-119">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75167-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="75167-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75167-120">Requirements</span></span>



| <span data-ttu-id="75167-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75167-121">Requirement</span></span> | <span data-ttu-id="75167-122">Wert</span><span class="sxs-lookup"><span data-stu-id="75167-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75167-123">Header</span><span class="sxs-lookup"><span data-stu-id="75167-123">Header</span></span><br/>  | <dl> <span data-ttu-id="75167-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="75167-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="75167-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75167-125">Library</span></span><br/> | <dl> <span data-ttu-id="75167-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75167-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75167-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75167-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75167-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="75167-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




