---
description: 'D3DXQuaternionRotationMatrix-Funktion (D3DX10Math.h): Erstellt eine Quaternion aus einer Rotationsmatrix.'
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: D3DXQuaternionRotationMatrix-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cb923c135d436b36fe032d344366fdee687d27a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103148"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="ef48a-103">D3DXQuaternionRotationMatrix-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="ef48a-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="ef48a-104">Erstellt eine Quaternion aus einer Rotationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="ef48a-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef48a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef48a-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="ef48a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef48a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef48a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ef48a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef48a-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef48a-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ef48a-109">Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ef48a-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ef48a-110">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ef48a-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef48a-111">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef48a-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ef48a-112">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="ef48a-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef48a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef48a-113">Return value</span></span>

<span data-ttu-id="ef48a-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef48a-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ef48a-115">Zeiger auf die D3DXQUATERNION-Struktur, die aus einer Rotationsmatrix erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef48a-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef48a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef48a-116">Remarks</span></span>

<span data-ttu-id="ef48a-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ef48a-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ef48a-118">Auf diese Weise kann die D3DXQuaternionRotationMatrix-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef48a-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ef48a-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="ef48a-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef48a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef48a-120">Requirements</span></span>



| <span data-ttu-id="ef48a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef48a-121">Requirement</span></span> | <span data-ttu-id="ef48a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ef48a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef48a-123">Header</span><span class="sxs-lookup"><span data-stu-id="ef48a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ef48a-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ef48a-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ef48a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef48a-125">Library</span></span><br/> | <dl> <span data-ttu-id="ef48a-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef48a-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef48a-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ef48a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef48a-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ef48a-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
