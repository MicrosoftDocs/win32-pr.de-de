---
description: 'D3DXVec4Normalize-Funktion (D3dx9math.h): Gibt die normalisierte Version eines 4D-Vektors zurück.'
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: D3DXVec4Normalize-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78984c393d7caf259b4c310a31e01ed8fcbd4d47
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097658"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="bc784-103">D3DXVec4Normalize-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="bc784-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="bc784-104">Gibt die normalisierte Version eines 4D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="bc784-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc784-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc784-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="bc784-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc784-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc784-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc784-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc784-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc784-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="bc784-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="bc784-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bc784-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bc784-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc784-111">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc784-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="bc784-112">Zeiger auf die [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="bc784-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc784-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc784-113">Return value</span></span>

<span data-ttu-id="bc784-114">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc784-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="bc784-115">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die die normalisierte Version des Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="bc784-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc784-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc784-116">Remarks</span></span>

<span data-ttu-id="bc784-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="bc784-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bc784-118">Auf diese Weise kann die **D3DXVec4Normalize-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc784-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc784-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc784-119">Requirements</span></span>



| <span data-ttu-id="bc784-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc784-120">Requirement</span></span> | <span data-ttu-id="bc784-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bc784-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc784-122">Header</span><span class="sxs-lookup"><span data-stu-id="bc784-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bc784-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bc784-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bc784-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc784-124">Library</span></span><br/> | <dl> <span data-ttu-id="bc784-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc784-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc784-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bc784-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc784-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bc784-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




