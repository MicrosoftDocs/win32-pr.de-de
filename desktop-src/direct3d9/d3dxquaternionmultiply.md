---
description: 'D3DXQuaternionMultiply-Funktion (D3dx9math.h): Multipliziert zwei Quaternionen.'
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: D3DXQuaternionMultiply-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118038"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="6dd06-103">D3DXQuaternionMultiply-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6dd06-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="6dd06-104">Multipliziert zwei Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="6dd06-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd06-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dd06-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="6dd06-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dd06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd06-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6dd06-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd06-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6dd06-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6dd06-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6dd06-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6dd06-110">*pQ1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6dd06-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd06-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6dd06-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6dd06-112">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="6dd06-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6dd06-113">*pQ2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6dd06-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd06-114">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6dd06-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6dd06-115">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="6dd06-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd06-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dd06-116">Return value</span></span>

<span data-ttu-id="6dd06-117">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6dd06-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6dd06-118">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Produkt zweier Quaternionen ist.</span><span class="sxs-lookup"><span data-stu-id="6dd06-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dd06-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dd06-119">Remarks</span></span>

<span data-ttu-id="6dd06-120">Das Ergebnis stellt die Drehung Q1 gefolgt von der Drehung Q2 (Out = Q2 \* Q1) dar.</span><span class="sxs-lookup"><span data-stu-id="6dd06-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="6dd06-121">Dies erfolgt so, dass **D3DXQuaternionMultiply** die gleiche Semantik wie [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) beibehält, da Einheitenquaternionen als eine andere Möglichkeit zur Darstellung von Rotationsmatrizen betrachtet werden können.</span><span class="sxs-lookup"><span data-stu-id="6dd06-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="6dd06-122">Transformationen werden für die Funktionen **D3DXQuaternionMultiply** und [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) in der gleichen Reihenfolge verkettet.</span><span class="sxs-lookup"><span data-stu-id="6dd06-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="6dd06-123">Angenommen, mX und mY stellen die gleichen Drehungen wie qX und qY dar, stellen sowohl m als auch q die gleichen Drehungen dar.</span><span class="sxs-lookup"><span data-stu-id="6dd06-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="6dd06-124">Die Multiplikation von Quaternionen ist nicht kommutativ.</span><span class="sxs-lookup"><span data-stu-id="6dd06-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="6dd06-125">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="6dd06-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6dd06-126">Auf diese Weise kann die **D3DXQuaternionMultiply-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6dd06-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6dd06-127">Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="6dd06-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dd06-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dd06-128">Requirements</span></span>



| <span data-ttu-id="6dd06-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dd06-129">Requirement</span></span> | <span data-ttu-id="6dd06-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6dd06-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd06-131">Header</span><span class="sxs-lookup"><span data-stu-id="6dd06-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6dd06-132"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6dd06-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6dd06-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6dd06-133">Library</span></span><br/> | <dl> <span data-ttu-id="6dd06-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6dd06-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6dd06-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6dd06-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd06-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6dd06-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6dd06-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="6dd06-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




