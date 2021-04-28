---
description: 'D3DXPlaneNormalize-Funktion (D3DX10Math.h): Normalisiert die Ebenenkoeffizienten so, dass die Normalebene die Einheitslänge aufwies.'
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: D3DXPlaneNormalize-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8b3499297a008b0d8f5dc705080bbd1d5bbe3af4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103308"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a><span data-ttu-id="98da0-103">D3DXPlaneNormalize-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="98da0-103">D3DXPlaneNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="98da0-104">Normalisiert die Ebenenkoeffizienten so, dass der Ebenennormar die Einheitslänge aufwies.</span><span class="sxs-lookup"><span data-stu-id="98da0-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="98da0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98da0-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="98da0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98da0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98da0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="98da0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98da0-108">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="98da0-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="98da0-109">Zeiger auf die [**D3DXPLANE,**](d3d10-d3dxplane.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="98da0-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="98da0-110">*pP* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="98da0-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98da0-111">Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="98da0-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="98da0-112">Zeiger auf die D3DXPLANE-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="98da0-112">Pointer to the source D3DXPLANE structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98da0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98da0-113">Return value</span></span>

<span data-ttu-id="98da0-114">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="98da0-114">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="98da0-115">Zeiger auf eine D3DXPLANE-Struktur, die die Normalität der Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="98da0-115">Pointer to a D3DXPLANE structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="98da0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98da0-116">Remarks</span></span>

<span data-ttu-id="98da0-117">Diese Funktion normalisiert eine Ebene so, dass \| a,b,c \| == 1.</span><span class="sxs-lookup"><span data-stu-id="98da0-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="98da0-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98da0-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="98da0-119">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98da0-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="98da0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98da0-120">Requirements</span></span>



| <span data-ttu-id="98da0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98da0-121">Requirement</span></span> | <span data-ttu-id="98da0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="98da0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98da0-123">Header</span><span class="sxs-lookup"><span data-stu-id="98da0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="98da0-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="98da0-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="98da0-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="98da0-125">Library</span></span><br/> | <dl> <span data-ttu-id="98da0-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="98da0-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98da0-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="98da0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98da0-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="98da0-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
