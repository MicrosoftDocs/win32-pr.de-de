---
description: 'D3DXQuaternionToAxisAngle-Funktion (D3dx9math.h): Berechnet die Achse und den Drehwinkel einer Quaternion.'
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: D3DXQuaternionToAxisAngle-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8613a9d14c5e33b0f9f4e719a02ac9a6d70d1119
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117978"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="218ae-103">D3DXQuaternionToAxisAngle-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="218ae-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="218ae-104">Berechnet die Achse und den Drehwinkel einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="218ae-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="218ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="218ae-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="218ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="218ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="218ae-107">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="218ae-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218ae-108">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="218ae-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="218ae-109">Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="218ae-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="218ae-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="218ae-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="218ae-111">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="218ae-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="218ae-112">Diese Funktion gibt einen Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) zurück, die die Drehachse der Quaternion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="218ae-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="218ae-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="218ae-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="218ae-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="218ae-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="218ae-115">Diese Funktion gibt einen Zeiger auf einen FLOAT-Wert zurück, der den Drehwinkel der Quaternion im Bogenmaß identifiziert.</span><span class="sxs-lookup"><span data-stu-id="218ae-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="218ae-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="218ae-116">Return value</span></span>

<span data-ttu-id="218ae-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="218ae-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="218ae-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="218ae-118">Remarks</span></span>

<span data-ttu-id="218ae-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="218ae-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="218ae-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="218ae-120">Requirements</span></span>



| <span data-ttu-id="218ae-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="218ae-121">Requirement</span></span> | <span data-ttu-id="218ae-122">Wert</span><span class="sxs-lookup"><span data-stu-id="218ae-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="218ae-123">Header</span><span class="sxs-lookup"><span data-stu-id="218ae-123">Header</span></span><br/>  | <dl> <span data-ttu-id="218ae-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="218ae-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="218ae-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="218ae-125">Library</span></span><br/> | <dl> <span data-ttu-id="218ae-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="218ae-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="218ae-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="218ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218ae-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="218ae-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
