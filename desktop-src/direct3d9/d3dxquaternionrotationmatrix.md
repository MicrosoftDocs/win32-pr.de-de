---
description: 'D3DXQuaternionRotationMatrix-Funktion (D3dx9math.h): Erstellt eine Quaternion aus einer Rotationsmatrix.'
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: D3DXQuaternionRotationMatrix-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b0ff8529f32d398ac208cff3214fccfdb2ade81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094008"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a><span data-ttu-id="d3e4d-103">D3DXQuaternionRotationMatrix-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d3e4d-103">D3DXQuaternionRotationMatrix function (D3dx9math.h)</span></span>

<span data-ttu-id="d3e4d-104">Erstellt eine Quaternion aus einer Rotationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e4d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3e4d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d3e4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3e4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3e4d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d3e4d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e4d-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3e4d-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d3e4d-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d3e4d-110">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d3e4d-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3e4d-111">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3e4d-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d3e4d-112">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="d3e4d-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3e4d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3e4d-113">Return value</span></span>

<span data-ttu-id="d3e4d-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3e4d-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="d3e4d-115">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die aus einer Rotationsmatrix erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-115">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e4d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3e4d-116">Remarks</span></span>

<span data-ttu-id="d3e4d-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d3e4d-118">Auf diese Weise kann die **D3DXQuaternionRotationMatrix-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-118">In this way, the **D3DXQuaternionRotationMatrix** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d3e4d-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="d3e4d-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e4d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3e4d-120">Requirements</span></span>



| <span data-ttu-id="d3e4d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3e4d-121">Requirement</span></span> | <span data-ttu-id="d3e4d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d3e4d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e4d-123">Header</span><span class="sxs-lookup"><span data-stu-id="d3e4d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d3e4d-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e4d-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d3e4d-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d3e4d-125">Library</span></span><br/> | <dl> <span data-ttu-id="d3e4d-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3e4d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3e4d-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d3e4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e4d-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d3e4d-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d3e4d-129">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="d3e4d-129">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="d3e4d-130">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="d3e4d-130">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




