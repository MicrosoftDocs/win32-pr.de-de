---
description: 'D3DXSHRotateZ-Funktion (D3DX10.h): Rotiert den SH-Vektor (Pherical Rotation) in der Z-Achse um den angegebenen Winkel.'
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: D3DXSHRotateZ-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55e4663057bd25ac9768a5913963a5511b662f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108528"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="3eba4-103">D3DXSHRotateZ-Funktion (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="3eba4-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="3eba4-104">Dreht den SH-Vektor (Pherical Rotation) in der Z-Achse um den angegebenen Winkel.</span><span class="sxs-lookup"><span data-stu-id="3eba4-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eba4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3eba4-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="3eba4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3eba4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eba4-107">*pOut* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3eba4-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eba4-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3eba4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3eba4-109">Zeiger auf SH-Ausgabekoeffizienten (Spherical- oder Pherical-Rumpf).</span><span class="sxs-lookup"><span data-stu-id="3eba4-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="3eba4-110">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3eba4-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3eba4-111">Dieser Zeiger sollte keinen Alias mit pIn verwenden.</span><span class="sxs-lookup"><span data-stu-id="3eba4-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="3eba4-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="3eba4-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3eba4-113">*Bestellung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3eba4-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eba4-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eba4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3eba4-115">Reihenfolge der SH-Auswertung.</span><span class="sxs-lookup"><span data-stu-id="3eba4-115">Order of the SH evaluation.</span></span> <span data-ttu-id="3eba4-116">Muss im Bereich von D3DXSH \_ MINORDER bis D3DXSH \_ MAXORDER (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="3eba4-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3eba4-117">Die Auswertung generiert Order Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3eba4-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3eba4-118">Der Grad der Auswertung ist Order - 1.</span><span class="sxs-lookup"><span data-stu-id="3eba4-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3eba4-119">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3eba4-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eba4-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eba4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3eba4-121">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="3eba4-121">Rotation angle in radians.</span></span> <span data-ttu-id="3eba4-122">Die Drehung erfolgt um die Z-Achse.</span><span class="sxs-lookup"><span data-stu-id="3eba4-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="3eba4-123">*pIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3eba4-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eba4-124">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3eba4-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3eba4-125">Zeiger auf gedrehte SH-Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3eba4-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eba4-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3eba4-126">Return value</span></span>

<span data-ttu-id="3eba4-127">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3eba4-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3eba4-128">Zeiger auf SH-Ausgabekoeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3eba4-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eba4-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3eba4-129">Remarks</span></span>

<span data-ttu-id="3eba4-130">Jeder Koeffizient der Basisfunktion "Ylm" wird an der Speicherposition ljs + m + l gespeichert, wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="3eba4-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="3eba4-131">l ist der Grad der Basisfunktion.</span><span class="sxs-lookup"><span data-stu-id="3eba4-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="3eba4-132">m ist der Basisfunktionsindex für den angegebenen l-Wert und reicht von -l bis l einschließlich.</span><span class="sxs-lookup"><span data-stu-id="3eba4-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eba4-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3eba4-133">Requirements</span></span>



| <span data-ttu-id="3eba4-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3eba4-134">Requirement</span></span> | <span data-ttu-id="3eba4-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3eba4-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3eba4-136">Header</span><span class="sxs-lookup"><span data-stu-id="3eba4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3eba4-137"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="3eba4-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3eba4-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3eba4-138">Library</span></span><br/> | <dl> <span data-ttu-id="3eba4-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3eba4-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eba4-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3eba4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eba4-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3eba4-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
