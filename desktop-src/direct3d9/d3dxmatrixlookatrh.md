---
description: 'D3DXMatrixLookAtRH-Funktion (D3dx9math.h): Erstellt eine rechtshändige Look-at-Matrix.'
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: D3DXMatrixLookAtRH-Funktion (D3dx9math.h)
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
ms.openlocfilehash: c9c98c0e8e0722b0b79fa12d4742cb328195d133
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107578"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="031c1-103">D3DXMatrixLookAtRH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="031c1-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="031c1-104">Erstellt eine rechtshändige Look-at-Matrix.</span><span class="sxs-lookup"><span data-stu-id="031c1-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="031c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="031c1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="031c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="031c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031c1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="031c1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="031c1-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="031c1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="031c1-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="031c1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="031c1-110">*pEye* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="031c1-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031c1-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="031c1-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="031c1-112">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Augenpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="031c1-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="031c1-113">Dieser Wert wird bei der Übersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="031c1-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="031c1-114">*pAt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="031c1-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031c1-115">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="031c1-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="031c1-116">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Kamera-Look-At-Ziel definiert.</span><span class="sxs-lookup"><span data-stu-id="031c1-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="031c1-117">*pUp* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="031c1-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031c1-118">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="031c1-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="031c1-119">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die aktuelle Welt definiert, in der Regel \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="031c1-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031c1-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="031c1-120">Return value</span></span>

<span data-ttu-id="031c1-121">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="031c1-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="031c1-122">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die eine rechtshändige Look-At-Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="031c1-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="031c1-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="031c1-123">Remarks</span></span>

<span data-ttu-id="031c1-124">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="031c1-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="031c1-125">Auf diese Weise kann die **D3DXMatrixLookAtRH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="031c1-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="031c1-126">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="031c1-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
 dot(xaxis, eye)   dot(yaxis, eye)   dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="031c1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="031c1-127">Requirements</span></span>



| <span data-ttu-id="031c1-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="031c1-128">Requirement</span></span> | <span data-ttu-id="031c1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="031c1-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="031c1-130">Header</span><span class="sxs-lookup"><span data-stu-id="031c1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="031c1-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="031c1-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="031c1-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="031c1-132">Library</span></span><br/> | <dl> <span data-ttu-id="031c1-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="031c1-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="031c1-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="031c1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031c1-135">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="031c1-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="031c1-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="031c1-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




