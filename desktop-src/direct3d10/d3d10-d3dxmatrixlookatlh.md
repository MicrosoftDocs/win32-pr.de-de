---
description: Erstellt eine Links bündige Matrix.
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: D3DXMatrixLookAtLH-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a5a7ffa8750fb08174f45b1069f103bfe08be1f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531040"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="87f75-103">D3DXMatrixLookAtLH-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="87f75-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="87f75-104">Erstellt eine Links bündige Matrix.</span><span class="sxs-lookup"><span data-stu-id="87f75-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87f75-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="87f75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87f75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f75-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="87f75-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87f75-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87f75-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87f75-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="87f75-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87f75-110">*Peer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f75-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f75-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87f75-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="87f75-112">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das den Augen Punkt definiert.</span><span class="sxs-lookup"><span data-stu-id="87f75-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="87f75-113">Dieser Wert wird bei der Übersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="87f75-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="87f75-114">*pAt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f75-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f75-115">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87f75-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="87f75-116">Ein Zeiger auf die D3DXVECTOR3-Struktur, die das Erscheinungsbild der Kamera definiert.</span><span class="sxs-lookup"><span data-stu-id="87f75-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="87f75-117">*PUP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87f75-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87f75-118">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="87f75-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="87f75-119">Ein Zeiger auf die D3DXVECTOR3-Struktur, die den aktuellen Globus definiert, normalerweise \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="87f75-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f75-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87f75-120">Return value</span></span>

<span data-ttu-id="87f75-121">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87f75-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87f75-122">Zeiger auf eine D3DXMATRIX-Struktur, bei der es sich um eine Links übergebene Matrix handelt.</span><span class="sxs-lookup"><span data-stu-id="87f75-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f75-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87f75-123">Remarks</span></span>

<span data-ttu-id="87f75-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="87f75-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="87f75-125">Auf diese Weise kann die D3DXMatrixLookAtLH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87f75-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="87f75-126">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="87f75-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="87f75-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87f75-127">Requirements</span></span>



| <span data-ttu-id="87f75-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87f75-128">Requirement</span></span> | <span data-ttu-id="87f75-129">Wert</span><span class="sxs-lookup"><span data-stu-id="87f75-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87f75-130">Header</span><span class="sxs-lookup"><span data-stu-id="87f75-130">Header</span></span><br/>  | <dl> <span data-ttu-id="87f75-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87f75-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="87f75-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87f75-132">Library</span></span><br/> | <dl> <span data-ttu-id="87f75-133"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87f75-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87f75-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87f75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f75-135">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="87f75-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
