---
description: 'D3DXMatrixMultiply-Funktion (D3dx9math.h): Bestimmt das Produkt von zwei Matrizen.'
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: D3DXMatrixMultiply-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d183fc3c79797bab886d3a40211448ccf57d552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107548"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="7b1f5-103">D3DXMatrixMultiply-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="7b1f5-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="7b1f5-104">Bestimmt das Produkt von zwei Matrizen.</span><span class="sxs-lookup"><span data-stu-id="7b1f5-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b1f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b1f5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="7b1f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b1f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b1f5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7b1f5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1f5-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b1f5-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b1f5-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="7b1f5-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b1f5-110">*pM1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7b1f5-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1f5-111">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b1f5-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b1f5-112">Zeiger auf eine [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="7b1f5-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b1f5-113">*pM2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7b1f5-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b1f5-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b1f5-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b1f5-115">Zeiger auf eine [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="7b1f5-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b1f5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b1f5-116">Return value</span></span>

<span data-ttu-id="7b1f5-117">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b1f5-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b1f5-118">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Produkt zweier Matrizen ist.</span><span class="sxs-lookup"><span data-stu-id="7b1f5-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b1f5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b1f5-119">Remarks</span></span>

<span data-ttu-id="7b1f5-120">Das Ergebnis stellt die Transformation M1 dar, gefolgt von der Transformation M2 (Out = M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="7b1f5-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="7b1f5-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b1f5-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7b1f5-122">Auf diese Weise kann die **D3DXMatrixMultiply-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b1f5-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b1f5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b1f5-123">Requirements</span></span>



| <span data-ttu-id="7b1f5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b1f5-124">Requirement</span></span> | <span data-ttu-id="7b1f5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7b1f5-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1f5-126">Header</span><span class="sxs-lookup"><span data-stu-id="7b1f5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7b1f5-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7b1f5-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7b1f5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b1f5-128">Library</span></span><br/> | <dl> <span data-ttu-id="7b1f5-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b1f5-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b1f5-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7b1f5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1f5-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7b1f5-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7b1f5-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="7b1f5-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




