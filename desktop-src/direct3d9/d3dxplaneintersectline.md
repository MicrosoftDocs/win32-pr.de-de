---
description: 'D3DXPlaneIntersectLine-Funktion (D3dx9math.h): Sucht die Schnittmenge zwischen einer Ebene und einer Linie.'
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: D3DXPlaneIntersectLine-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9b89508079b0b400135f4ae39fd6fdfaed61952
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098068"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a><span data-ttu-id="99b63-103">D3DXPlaneIntersectLine-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="99b63-103">D3DXPlaneIntersectLine function (D3dx9math.h)</span></span>

<span data-ttu-id="99b63-104">Sucht die Schnittmenge zwischen einer Ebene und einer Linie.</span><span class="sxs-lookup"><span data-stu-id="99b63-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99b63-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="99b63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99b63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b63-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="99b63-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b63-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b63-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="99b63-109">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Schnittmenge zwischen der angegebenen Ebene und Linie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="99b63-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="99b63-110">*pP* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="99b63-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b63-111">Typ: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="99b63-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="99b63-112">Zeiger auf die [**D3DXPLANE-Quellstruktur.**](d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="99b63-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="99b63-113">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="99b63-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b63-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="99b63-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="99b63-115">Zeiger auf eine [**D3DXVECTOR3-Quellstruktur,**](d3dxvector3.md) die einen Zeilenstartpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="99b63-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="99b63-116">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="99b63-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b63-117">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="99b63-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="99b63-118">Zeiger auf eine [**D3DXVECTOR3-Quellstruktur,**](d3dxvector3.md) die einen Zeilenendpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="99b63-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b63-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99b63-119">Return value</span></span>

<span data-ttu-id="99b63-120">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b63-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="99b63-121">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Schnittmenge zwischen der angegebenen Ebene und Linie ist.</span><span class="sxs-lookup"><span data-stu-id="99b63-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b63-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99b63-122">Remarks</span></span>

<span data-ttu-id="99b63-123">Wenn die Linie parallel zur Ebene ist, wird **NULL** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99b63-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="99b63-124">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="99b63-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="99b63-125">Auf diese Weise kann die **D3DXPlaneIntersectLine-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99b63-125">In this way, the **D3DXPlaneIntersectLine** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b63-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99b63-126">Requirements</span></span>



| <span data-ttu-id="99b63-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99b63-127">Requirement</span></span> | <span data-ttu-id="99b63-128">Wert</span><span class="sxs-lookup"><span data-stu-id="99b63-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b63-129">Header</span><span class="sxs-lookup"><span data-stu-id="99b63-129">Header</span></span><br/>  | <dl> <span data-ttu-id="99b63-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="99b63-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="99b63-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99b63-131">Library</span></span><br/> | <dl> <span data-ttu-id="99b63-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b63-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99b63-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="99b63-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b63-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="99b63-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




