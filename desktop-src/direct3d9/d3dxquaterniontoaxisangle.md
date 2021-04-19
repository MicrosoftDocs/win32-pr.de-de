---
description: Berechnet die Achse und den Drehwinkel einer Quaternion.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: D3DXQuaternionToAxisAngle-Funktion (D3dx9math. h)
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
ms.openlocfilehash: ecf8e6d1b1383a6e698f742351ee19ae75fd5bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373504"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="8cc02-103">D3DXQuaternionToAxisAngle-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8cc02-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="8cc02-104">Berechnet die Achse und den Drehwinkel einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="8cc02-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc02-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="8cc02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cc02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc02-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8cc02-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc02-108">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8cc02-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8cc02-109">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8cc02-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8cc02-110">ein-.  \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8cc02-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc02-111">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc02-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8cc02-112">Diese Funktion gibt einen Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur zurück, die die Achse der Drehung der Quaternion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cc02-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="8cc02-113">*Schwenken* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8cc02-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cc02-114">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc02-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8cc02-115">Diese Funktion gibt einen Zeiger auf einen float-Wert zurück, der den Drehwinkel der Quaternion im Bogenmaße identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cc02-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc02-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cc02-116">Return value</span></span>

<span data-ttu-id="8cc02-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8cc02-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc02-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cc02-118">Remarks</span></span>

<span data-ttu-id="8cc02-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="8cc02-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc02-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cc02-120">Requirements</span></span>



| <span data-ttu-id="8cc02-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cc02-121">Requirement</span></span> | <span data-ttu-id="8cc02-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8cc02-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc02-123">Header</span><span class="sxs-lookup"><span data-stu-id="8cc02-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8cc02-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc02-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8cc02-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8cc02-125">Library</span></span><br/> | <dl> <span data-ttu-id="8cc02-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8cc02-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8cc02-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cc02-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc02-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8cc02-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
