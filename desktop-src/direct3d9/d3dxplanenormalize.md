---
description: 'D3DXPlaneNormalize-Funktion (D3dx9math.h): Normalisiert die Ebenenkoeffizienten so, dass die Normalebene die Einheitslänge hat.'
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: D3DXPlaneNormalize-Funktion (D3dx9math.h)
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
ms.openlocfilehash: d38ccbc3f688ed61779cf48a77e97dfb544c686e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094148"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a><span data-ttu-id="22949-103">D3DXPlaneNormalize-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="22949-103">D3DXPlaneNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="22949-104">Normalisiert die Ebenenkoeffizienten so, dass der Ebenennormar die Einheitslänge aufwies.</span><span class="sxs-lookup"><span data-stu-id="22949-104">Normalizes the plane coefficients so that the plane normal has unit length.</span></span>

## <a name="syntax"></a><span data-ttu-id="22949-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22949-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a><span data-ttu-id="22949-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22949-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="22949-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22949-108">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="22949-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="22949-109">Zeiger auf die [**D3DXPLANE-Struktur,**](d3dxplane.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="22949-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="22949-110">*pP* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22949-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22949-111">Typ: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="22949-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="22949-112">Zeiger auf die [**D3DXPLANE-Quellstruktur.**](d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="22949-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22949-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22949-113">Return value</span></span>

<span data-ttu-id="22949-114">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="22949-114">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="22949-115">Zeiger auf eine [**D3DXPLANE-Struktur,**](d3dxplane.md) die die Normalität der Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="22949-115">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the normal of the plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="22949-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22949-116">Remarks</span></span>

<span data-ttu-id="22949-117">Diese Funktion normalisiert eine Ebene so, dass \| a,b,c \| == 1.</span><span class="sxs-lookup"><span data-stu-id="22949-117">This function normalizes a plane so that \|a,b,c\| == 1.</span></span>

<span data-ttu-id="22949-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="22949-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="22949-119">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22949-119">In this way, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22949-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22949-120">Requirements</span></span>



| <span data-ttu-id="22949-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22949-121">Requirement</span></span> | <span data-ttu-id="22949-122">Wert</span><span class="sxs-lookup"><span data-stu-id="22949-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22949-123">Header</span><span class="sxs-lookup"><span data-stu-id="22949-123">Header</span></span><br/>  | <dl> <span data-ttu-id="22949-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="22949-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="22949-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22949-125">Library</span></span><br/> | <dl> <span data-ttu-id="22949-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="22949-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22949-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22949-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22949-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="22949-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




