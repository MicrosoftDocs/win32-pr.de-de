---
description: Multipliziert zwei Quaternionen.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: D3DXQuaternionMultiply-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 753fd206e2b970182ed44c216f1339d56973c416
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132381"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="aa039-103">D3DXQuaternionMultiply-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="aa039-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="aa039-104">Multipliziert zwei Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="aa039-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa039-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa039-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="aa039-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa039-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa039-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aa039-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa039-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="aa039-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="aa039-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="aa039-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="aa039-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa039-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa039-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="aa039-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="aa039-112">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="aa039-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa039-113">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa039-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa039-114">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="aa039-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="aa039-115">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="aa039-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa039-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa039-116">Return value</span></span>

<span data-ttu-id="aa039-117">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="aa039-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="aa039-118">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Produkt aus zwei Quaternionen ist.</span><span class="sxs-lookup"><span data-stu-id="aa039-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa039-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa039-119">Remarks</span></span>

<span data-ttu-id="aa039-120">Das Ergebnis stellt die Drehung Q1, gefolgt von der Drehung Q2 (out = Q2 \* Q1) dar.</span><span class="sxs-lookup"><span data-stu-id="aa039-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="aa039-121">Dies geschieht, damit **D3DXQuaternionMultiply** dieselbe Semantik wie [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) beibehält, da Einheiten Quaternionen als eine andere Möglichkeit zur Darstellung von Rotations Matrizen angesehen werden können.</span><span class="sxs-lookup"><span data-stu-id="aa039-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="aa039-122">Transformationen werden in derselben Reihenfolge für die **D3DXQuaternionMultiply** -Funktion und die [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) -Funktion verkettet.</span><span class="sxs-lookup"><span data-stu-id="aa039-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="aa039-123">Wenn z. b. MX und My die gleichen Drehungen wie QX und qY darstellen, stellen sowohl m als auch q die gleichen Drehungen dar.</span><span class="sxs-lookup"><span data-stu-id="aa039-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="aa039-124">Die Multiplikation von Quaternionen ist nicht kommutativ.</span><span class="sxs-lookup"><span data-stu-id="aa039-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="aa039-125">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa039-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="aa039-126">Auf diese Weise kann die **D3DXQuaternionMultiply** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa039-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="aa039-127">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="aa039-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa039-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa039-128">Requirements</span></span>



| <span data-ttu-id="aa039-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa039-129">Requirement</span></span> | <span data-ttu-id="aa039-130">Wert</span><span class="sxs-lookup"><span data-stu-id="aa039-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa039-131">Header</span><span class="sxs-lookup"><span data-stu-id="aa039-131">Header</span></span><br/>  | <dl> <span data-ttu-id="aa039-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa039-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="aa039-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa039-133">Library</span></span><br/> | <dl> <span data-ttu-id="aa039-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa039-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aa039-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa039-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa039-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="aa039-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="aa039-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="aa039-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




