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
ms.openlocfilehash: 44b3a738de31edf373deb65ea9991e1e1502f47c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335604"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="b3163-103">D3DXMatrixLookAtRH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="b3163-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="b3163-104">Erstellt eine rechtshändige Look-at-Matrix.</span><span class="sxs-lookup"><span data-stu-id="b3163-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3163-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3163-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="b3163-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3163-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3163-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3163-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3163-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3163-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3163-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="b3163-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b3163-110">*pEye* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b3163-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3163-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3163-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b3163-112">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Augenpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="b3163-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="b3163-113">Dieser Wert wird bei der Übersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3163-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="b3163-114">*pAt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b3163-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3163-115">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3163-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b3163-116">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Kamera-Look-At-Ziel definiert.</span><span class="sxs-lookup"><span data-stu-id="b3163-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="b3163-117">*pUp* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b3163-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3163-118">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3163-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b3163-119">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die aktuelle Welt definiert, in der Regel \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="b3163-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3163-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b3163-120">Return value</span></span>

<span data-ttu-id="b3163-121">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3163-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3163-122">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die eine rechtshändige Look-At-Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="b3163-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3163-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3163-123">Remarks</span></span>

<span data-ttu-id="b3163-124">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="b3163-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b3163-125">Auf diese Weise kann die **D3DXMatrixLookAtRH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3163-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b3163-126">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b3163-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x            yaxis.x            zaxis.x           0
 xaxis.y            yaxis.y            zaxis.y           0
 xaxis.z            yaxis.z            zaxis.z           0
 -dot(xaxis, eye)   -dot(yaxis, eye)   -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="b3163-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3163-127">Requirements</span></span>



| <span data-ttu-id="b3163-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3163-128">Requirement</span></span> | <span data-ttu-id="b3163-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b3163-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3163-130">Header</span><span class="sxs-lookup"><span data-stu-id="b3163-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b3163-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b3163-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b3163-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3163-132">Library</span></span><br/> | <dl> <span data-ttu-id="b3163-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3163-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3163-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3163-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3163-135">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b3163-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b3163-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="b3163-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




