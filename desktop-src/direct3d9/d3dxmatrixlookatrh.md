---
description: Erstellt eine nach rechts gerichtete Matrix.
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: D3DXMatrixLookAtRH-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f09b57d46c6c5dea51c9b55ce6fe507d5bfe415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354206"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="74778-103">D3DXMatrixLookAtRH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="74778-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="74778-104">Erstellt eine nach rechts gerichtete Matrix.</span><span class="sxs-lookup"><span data-stu-id="74778-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="74778-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74778-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="74778-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74778-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74778-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="74778-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74778-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="74778-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="74778-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="74778-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="74778-110">*Peer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74778-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74778-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="74778-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="74778-112">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Augen Punkt definiert.</span><span class="sxs-lookup"><span data-stu-id="74778-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="74778-113">Dieser Wert wird bei der Übersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="74778-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="74778-114">*pAt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74778-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74778-115">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="74778-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="74778-116">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Erscheinungsbild der Kamera definiert.</span><span class="sxs-lookup"><span data-stu-id="74778-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="74778-117">*PUP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74778-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74778-118">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="74778-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="74778-119">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den aktuellen Globus definiert, normalerweise \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="74778-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74778-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74778-120">Return value</span></span>

<span data-ttu-id="74778-121">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="74778-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="74778-122">Ein Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, bei der es sich um eine rechts übergebene, Einsehens Matrix handelt.</span><span class="sxs-lookup"><span data-stu-id="74778-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="74778-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74778-123">Remarks</span></span>

<span data-ttu-id="74778-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="74778-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="74778-125">Auf diese Weise kann die **D3DXMatrixLookAtRH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74778-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="74778-126">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="74778-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
 dot(xaxis, eye)   dot(yaxis, eye)   dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="74778-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74778-127">Requirements</span></span>



| <span data-ttu-id="74778-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74778-128">Requirement</span></span> | <span data-ttu-id="74778-129">Wert</span><span class="sxs-lookup"><span data-stu-id="74778-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74778-130">Header</span><span class="sxs-lookup"><span data-stu-id="74778-130">Header</span></span><br/>  | <dl> <span data-ttu-id="74778-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="74778-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="74778-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74778-132">Library</span></span><br/> | <dl> <span data-ttu-id="74778-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74778-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74778-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74778-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74778-135">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="74778-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="74778-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="74778-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




