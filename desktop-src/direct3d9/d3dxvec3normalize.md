---
description: 'D3DXVec3Normalize-Funktion (D3dx9math.h): Gibt die normalisierte Version eines 3D-Vektors zurück.'
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: D3DXVec3Normalize-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f39890a92bbff9d27a1150e76092d865dc36c089
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097828"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a><span data-ttu-id="f431a-103">D3DXVec3Normalize-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f431a-103">D3DXVec3Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="f431a-104">Gibt die normalisierte Version eines 3D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="f431a-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f431a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f431a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="f431a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f431a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f431a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f431a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f431a-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f431a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f431a-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f431a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f431a-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f431a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f431a-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f431a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f431a-112">Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="f431a-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f431a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f431a-113">Return value</span></span>

<span data-ttu-id="f431a-114">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f431a-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f431a-115">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die normalisierte Version des angegebenen Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="f431a-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f431a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f431a-116">Remarks</span></span>

<span data-ttu-id="f431a-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f431a-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f431a-118">Auf diese Weise kann die **D3DXVec3Normalize-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f431a-118">In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f431a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f431a-119">Requirements</span></span>



| <span data-ttu-id="f431a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f431a-120">Requirement</span></span> | <span data-ttu-id="f431a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f431a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f431a-122">Header</span><span class="sxs-lookup"><span data-stu-id="f431a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f431a-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f431a-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f431a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f431a-124">Library</span></span><br/> | <dl> <span data-ttu-id="f431a-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f431a-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f431a-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f431a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f431a-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f431a-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




