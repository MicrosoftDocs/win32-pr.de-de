---
description: Erstellt eine Links bündige Matrix.
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: D3DXMatrixLookAtLH-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fa7acdf467761bd3b3cfbc023662e9b3368b98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363167"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="0957f-103">D3DXMatrixLookAtLH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0957f-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="0957f-104">Erstellt eine Links bündige Matrix.</span><span class="sxs-lookup"><span data-stu-id="0957f-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0957f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0957f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="0957f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0957f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0957f-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0957f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0957f-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0957f-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0957f-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="0957f-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0957f-110">*Peer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0957f-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0957f-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0957f-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0957f-112">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den Augen Punkt definiert.</span><span class="sxs-lookup"><span data-stu-id="0957f-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="0957f-113">Dieser Wert wird bei der Übersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0957f-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="0957f-114">*pAt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0957f-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0957f-115">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0957f-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0957f-116">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Erscheinungsbild der Kamera definiert.</span><span class="sxs-lookup"><span data-stu-id="0957f-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="0957f-117">*PUP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0957f-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0957f-118">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0957f-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0957f-119">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den aktuellen Globus definiert, normalerweise \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="0957f-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0957f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0957f-120">Return value</span></span>

<span data-ttu-id="0957f-121">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0957f-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0957f-122">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, bei der es sich um eine Links übergebene Matrix handelt.</span><span class="sxs-lookup"><span data-stu-id="0957f-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0957f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0957f-123">Remarks</span></span>

<span data-ttu-id="0957f-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0957f-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0957f-125">Auf diese Weise kann die **D3DXMatrixLookAtLH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0957f-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0957f-126">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="0957f-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="0957f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0957f-127">Requirements</span></span>



| <span data-ttu-id="0957f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0957f-128">Requirement</span></span> | <span data-ttu-id="0957f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0957f-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0957f-130">Header</span><span class="sxs-lookup"><span data-stu-id="0957f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0957f-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0957f-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0957f-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0957f-132">Library</span></span><br/> | <dl> <span data-ttu-id="0957f-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0957f-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0957f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0957f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0957f-135">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0957f-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0957f-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="0957f-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




