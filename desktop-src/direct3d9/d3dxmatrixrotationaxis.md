---
description: Erstellt eine Matrix, die um eine beliebige Achse rotiert.
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: D3DXMatrixRotationAxis-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fffc4a5bdd287c79352beb3ee0eeaf97b0573753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363118"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="40aaa-103">D3DXMatrixRotationAxis-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="40aaa-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="40aaa-104">Erstellt eine Matrix, die um eine beliebige Achse rotiert.</span><span class="sxs-lookup"><span data-stu-id="40aaa-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="40aaa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40aaa-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="40aaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40aaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40aaa-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="40aaa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="40aaa-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="40aaa-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="40aaa-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="40aaa-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="40aaa-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40aaa-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40aaa-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="40aaa-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="40aaa-112">Zeiger auf die beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="40aaa-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="40aaa-113">Siehe [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="40aaa-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="40aaa-114">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40aaa-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40aaa-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="40aaa-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="40aaa-116">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="40aaa-116">Angle of rotation in radians.</span></span> <span data-ttu-id="40aaa-117">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="40aaa-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40aaa-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40aaa-118">Return value</span></span>

<span data-ttu-id="40aaa-119">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="40aaa-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="40aaa-120">Ein Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, gedreht um die angegebene Achse.</span><span class="sxs-lookup"><span data-stu-id="40aaa-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="40aaa-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40aaa-121">Remarks</span></span>

<span data-ttu-id="40aaa-122">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="40aaa-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="40aaa-123">Auf diese Weise kann die **D3DXMatrixRotationAxis** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40aaa-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="40aaa-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40aaa-124">Requirements</span></span>



| <span data-ttu-id="40aaa-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40aaa-125">Requirement</span></span> | <span data-ttu-id="40aaa-126">Wert</span><span class="sxs-lookup"><span data-stu-id="40aaa-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40aaa-127">Header</span><span class="sxs-lookup"><span data-stu-id="40aaa-127">Header</span></span><br/>  | <dl> <span data-ttu-id="40aaa-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="40aaa-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="40aaa-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40aaa-129">Library</span></span><br/> | <dl> <span data-ttu-id="40aaa-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40aaa-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="40aaa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40aaa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40aaa-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="40aaa-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="40aaa-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="40aaa-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="40aaa-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="40aaa-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="40aaa-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="40aaa-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="40aaa-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="40aaa-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="40aaa-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="40aaa-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
