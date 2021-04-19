---
description: Transformiert einen 4D-Vektor durch eine angegebene Matrix.
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: D3DXVec4Transform-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 20192cf51a6096bbbce1f009d91d96551aec12d8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361885"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="73214-103">D3DXVec4Transform-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="73214-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="73214-104">Transformiert einen 4D-Vektor durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="73214-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="73214-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73214-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="73214-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73214-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="73214-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73214-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="73214-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="73214-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="73214-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="73214-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73214-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73214-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="73214-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="73214-112">Ein Zeiger auf die Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="73214-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="73214-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73214-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73214-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="73214-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="73214-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="73214-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73214-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73214-116">Return value</span></span>

<span data-ttu-id="73214-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="73214-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="73214-118">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die der transformierte 4D-Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="73214-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="73214-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73214-119">Remarks</span></span>

<span data-ttu-id="73214-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="73214-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="73214-121">Auf diese Weise kann die **D3DXVec4Transform** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73214-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="73214-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73214-122">Requirements</span></span>



| <span data-ttu-id="73214-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73214-123">Requirement</span></span> | <span data-ttu-id="73214-124">Wert</span><span class="sxs-lookup"><span data-stu-id="73214-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73214-125">Header</span><span class="sxs-lookup"><span data-stu-id="73214-125">Header</span></span><br/>  | <dl> <span data-ttu-id="73214-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="73214-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="73214-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73214-127">Library</span></span><br/> | <dl> <span data-ttu-id="73214-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73214-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73214-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73214-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73214-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="73214-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




