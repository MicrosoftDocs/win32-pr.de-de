---
description: 'D3DXQuaternionLn-Funktion (D3DX10Math.h): Berechnet den natürlichen Logarithmus.'
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: D3DXQuaternionLn-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9abaaa231e424e55e496b7901882e9da17c59786
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103208"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="47b7b-103">D3DXQuaternionLn-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="47b7b-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="47b7b-104">Berechnet den natürlichen Logarithmus.</span><span class="sxs-lookup"><span data-stu-id="47b7b-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="47b7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47b7b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="47b7b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47b7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47b7b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="47b7b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47b7b-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="47b7b-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="47b7b-109">Zeiger auf das [**D3DXQUATERNION-Steuerelement,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="47b7b-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="47b7b-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="47b7b-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47b7b-111">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="47b7b-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="47b7b-112">Zeiger auf die D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="47b7b-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47b7b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47b7b-113">Return value</span></span>

<span data-ttu-id="47b7b-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="47b7b-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="47b7b-115">Zeiger auf eine D3DXQUATERNION-Struktur, bei der es sich um den natürlichen Logarithmus handelt.</span><span class="sxs-lookup"><span data-stu-id="47b7b-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="47b7b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47b7b-116">Remarks</span></span>

<span data-ttu-id="47b7b-117">Die D3DXQuaternionLn-Funktion funktioniert nur für Einheitenquaternionen.</span><span class="sxs-lookup"><span data-stu-id="47b7b-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="47b7b-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="47b7b-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="47b7b-119">Auf diese Weise kann die D3DXQuaternionLn-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47b7b-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="47b7b-120">Verwenden [**Sie D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="47b7b-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="47b7b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47b7b-121">Requirements</span></span>



| <span data-ttu-id="47b7b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47b7b-122">Requirement</span></span> | <span data-ttu-id="47b7b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="47b7b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47b7b-124">Header</span><span class="sxs-lookup"><span data-stu-id="47b7b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="47b7b-125"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="47b7b-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="47b7b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47b7b-126">Library</span></span><br/> | <dl> <span data-ttu-id="47b7b-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="47b7b-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47b7b-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="47b7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47b7b-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="47b7b-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
