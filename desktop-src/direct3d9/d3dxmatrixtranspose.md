---
description: 'D3DXMatrixTranspose-Funktion (D3dx9math.h): Gibt die Matrix transponieren einer Matrix zurück.'
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: D3DXMatrixTranspose-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cb050061b10de963258bcd7527d3c86260d5abc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098108"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="ab146-103">D3DXMatrixTranspose-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="ab146-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="ab146-104">Gibt die Matrix transponieren einer Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="ab146-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab146-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab146-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="ab146-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab146-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab146-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ab146-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab146-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab146-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab146-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ab146-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ab146-110">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ab146-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab146-111">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab146-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab146-112">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="ab146-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab146-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab146-113">Return value</span></span>

<span data-ttu-id="ab146-114">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab146-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab146-115">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Matrix transponiert.</span><span class="sxs-lookup"><span data-stu-id="ab146-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab146-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab146-116">Remarks</span></span>

<span data-ttu-id="ab146-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ab146-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ab146-118">Auf diese Weise kann die **D3DXMatrixTranspose-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab146-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab146-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab146-119">Requirements</span></span>



| <span data-ttu-id="ab146-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab146-120">Requirement</span></span> | <span data-ttu-id="ab146-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ab146-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab146-122">Header</span><span class="sxs-lookup"><span data-stu-id="ab146-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ab146-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ab146-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab146-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab146-124">Library</span></span><br/> | <dl> <span data-ttu-id="ab146-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab146-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab146-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab146-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab146-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ab146-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




