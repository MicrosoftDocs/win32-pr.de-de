---
description: Skaliert einen 4D-Vektor.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: D3DXVec4Scale-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a29ee7b8519c802deb0542b6b7ba3ea22692f36d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355198"
---
# <a name="d3dxvec4scale-function"></a><span data-ttu-id="8b9f7-103">D3DXVec4Scale-Funktion</span><span class="sxs-lookup"><span data-stu-id="8b9f7-103">D3DXVec4Scale function</span></span>

<span data-ttu-id="8b9f7-104">Skaliert einen 4D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="8b9f7-104">Scales a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b9f7-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="8b9f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b9f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b9f7-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8b9f7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b9f7-108">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b9f7-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8b9f7-109">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8b9f7-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8b9f7-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b9f7-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b9f7-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8b9f7-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8b9f7-112">Ein Zeiger auf die Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8b9f7-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b9f7-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b9f7-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b9f7-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8b9f7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8b9f7-115">Skalierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="8b9f7-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b9f7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b9f7-116">Return value</span></span>

<span data-ttu-id="8b9f7-117">Typ: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8b9f7-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="8b9f7-118">Ein Zeiger auf die [**D3DXVECTOR4**](d3dxvector4.md) -Struktur, die der skalierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="8b9f7-118">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b9f7-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b9f7-119">Remarks</span></span>

<span data-ttu-id="8b9f7-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8b9f7-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8b9f7-121">Auf diese Weise kann die **D3DXVec4Scale** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b9f7-121">In this way, the **D3DXVec4Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9f7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b9f7-122">Requirements</span></span>



| <span data-ttu-id="8b9f7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b9f7-123">Requirement</span></span> | <span data-ttu-id="8b9f7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8b9f7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9f7-125">Header</span><span class="sxs-lookup"><span data-stu-id="8b9f7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8b9f7-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b9f7-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8b9f7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b9f7-127">Library</span></span><br/> | <dl> <span data-ttu-id="8b9f7-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b9f7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b9f7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b9f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9f7-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8b9f7-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8b9f7-131">**D3DXVec4Add**</span><span class="sxs-lookup"><span data-stu-id="8b9f7-131">**D3DXVec4Add**</span></span>](d3dxvec4add.md)
</dt> <dt>

[<span data-ttu-id="8b9f7-132">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="8b9f7-132">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> </dl>

 

 
