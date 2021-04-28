---
description: 'D3DXQuaternionLn-Funktion (D3dx9math.h): Berechnet den natürlichen Logarithmus.'
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: D3DXQuaternionLn-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1a529c1c6ca4d7f81bf4d41fcdb4a7c7179874b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094058"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="bbe8c-103">D3DXQuaternionLn-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="bbe8c-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="bbe8c-104">Berechnet den natürlichen Logarithmus.</span><span class="sxs-lookup"><span data-stu-id="bbe8c-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbe8c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="bbe8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbe8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbe8c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bbe8c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe8c-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbe8c-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bbe8c-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="bbe8c-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bbe8c-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bbe8c-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbe8c-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bbe8c-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bbe8c-112">Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="bbe8c-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbe8c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbe8c-113">Return value</span></span>

<span data-ttu-id="bbe8c-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbe8c-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bbe8c-115">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) bei der es sich um den natürlichen Logarithmus handelt.</span><span class="sxs-lookup"><span data-stu-id="bbe8c-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe8c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbe8c-116">Remarks</span></span>

<span data-ttu-id="bbe8c-117">Die **D3DXQuaternionLn-Funktion** funktioniert nur für Einheitenquaternionen.</span><span class="sxs-lookup"><span data-stu-id="bbe8c-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="bbe8c-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="bbe8c-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bbe8c-119">Auf diese Weise kann die **D3DXQuaternionLn-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbe8c-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bbe8c-120">Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="bbe8c-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbe8c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbe8c-121">Requirements</span></span>



| <span data-ttu-id="bbe8c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbe8c-122">Requirement</span></span> | <span data-ttu-id="bbe8c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bbe8c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe8c-124">Header</span><span class="sxs-lookup"><span data-stu-id="bbe8c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bbe8c-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe8c-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bbe8c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bbe8c-126">Library</span></span><br/> | <dl> <span data-ttu-id="bbe8c-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bbe8c-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bbe8c-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bbe8c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe8c-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bbe8c-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bbe8c-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="bbe8c-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="bbe8c-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="bbe8c-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




