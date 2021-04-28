---
description: 'D3DXVec4Transform-Funktion (D3dx9math.h): Transformiert einen 4D-Vektor durch eine bestimmte Matrix.'
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: D3DXVec4Transform-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e5a9fdd92a2d978c746543fbbbeec6503d07404
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115508"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="22a5a-103">D3DXVec4Transform-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="22a5a-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="22a5a-104">Transformiert einen 4D-Vektor durch eine bestimmte Matrix.</span><span class="sxs-lookup"><span data-stu-id="22a5a-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a5a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22a5a-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="22a5a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22a5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a5a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="22a5a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22a5a-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="22a5a-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="22a5a-109">Zeiger auf die [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="22a5a-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="22a5a-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22a5a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22a5a-111">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="22a5a-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="22a5a-112">Zeiger auf die [**D3DXVECTOR4-Quellstruktur.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="22a5a-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="22a5a-113">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="22a5a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22a5a-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="22a5a-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="22a5a-115">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="22a5a-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a5a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22a5a-116">Return value</span></span>

<span data-ttu-id="22a5a-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="22a5a-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="22a5a-118">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die der transformierte 4D-Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="22a5a-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="22a5a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22a5a-119">Remarks</span></span>

<span data-ttu-id="22a5a-120">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="22a5a-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="22a5a-121">Auf diese Weise kann die **D3DXVec4Transform-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22a5a-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a5a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22a5a-122">Requirements</span></span>



| <span data-ttu-id="22a5a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22a5a-123">Requirement</span></span> | <span data-ttu-id="22a5a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="22a5a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22a5a-125">Header</span><span class="sxs-lookup"><span data-stu-id="22a5a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="22a5a-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="22a5a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="22a5a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22a5a-127">Library</span></span><br/> | <dl> <span data-ttu-id="22a5a-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="22a5a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22a5a-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="22a5a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a5a-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="22a5a-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




