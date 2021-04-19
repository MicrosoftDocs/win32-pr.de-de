---
description: Multipliziert zwei Quaternionen.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: D3DXQuaternionMultiply-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 74e10117bf27d922480418e5aa0b8ea60a13528c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353756"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="7550b-103">D3DXQuaternionMultiply-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="7550b-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="7550b-104">Multipliziert zwei Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="7550b-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7550b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7550b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="7550b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7550b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7550b-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7550b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7550b-108">Typ: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7550b-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7550b-109">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="7550b-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7550b-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7550b-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7550b-111">Typ: **Konstanten [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7550b-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7550b-112">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7550b-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7550b-113">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7550b-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7550b-114">Typ: **Konstanten [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7550b-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7550b-115">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7550b-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7550b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7550b-116">Return value</span></span>

<span data-ttu-id="7550b-117">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7550b-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7550b-118">Zeiger auf eine [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) -Struktur, die das Produkt aus zwei Quaternionen ist.</span><span class="sxs-lookup"><span data-stu-id="7550b-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="7550b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7550b-119">Remarks</span></span>

<span data-ttu-id="7550b-120">Das Ergebnis stellt die Drehung Q1, gefolgt von der Drehung Q2 (out = Q2 \* Q1) dar.</span><span class="sxs-lookup"><span data-stu-id="7550b-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="7550b-121">Dies geschieht, damit **D3DXQuaternionMultiply** dieselbe Semantik wie [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) beibehält, da Einheiten Quaternionen als eine andere Möglichkeit zur Darstellung von Rotations Matrizen angesehen werden können.</span><span class="sxs-lookup"><span data-stu-id="7550b-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="7550b-122">Transformationen werden in derselben Reihenfolge für die **D3DXQuaternionMultiply** -Funktion und die [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) -Funktion verkettet.</span><span class="sxs-lookup"><span data-stu-id="7550b-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="7550b-123">Wenn z. b. MX und My die gleichen Drehungen wie QX und qY darstellen, stellen sowohl m als auch q die gleichen Drehungen dar.</span><span class="sxs-lookup"><span data-stu-id="7550b-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="7550b-124">Die Multiplikation von Quaternionen ist nicht kommutativ.</span><span class="sxs-lookup"><span data-stu-id="7550b-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="7550b-125">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7550b-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7550b-126">Auf diese Weise kann die **D3DXQuaternionMultiply** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7550b-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7550b-127">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="7550b-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7550b-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7550b-128">Requirements</span></span>



| <span data-ttu-id="7550b-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7550b-129">Requirement</span></span> | <span data-ttu-id="7550b-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7550b-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7550b-131">Header</span><span class="sxs-lookup"><span data-stu-id="7550b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7550b-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7550b-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7550b-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7550b-133">Library</span></span><br/> | <dl> <span data-ttu-id="7550b-134"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7550b-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7550b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7550b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7550b-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7550b-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
