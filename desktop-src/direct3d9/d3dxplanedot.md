---
description: Berechnet das Punktprodukt einer Ebene und einen 4D-Vektor.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: D3DXPlaneDot-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357217"
---
# <a name="d3dxplanedot-function"></a><span data-ttu-id="c23fa-103">D3DXPlaneDot-Funktion</span><span class="sxs-lookup"><span data-stu-id="c23fa-103">D3DXPlaneDot function</span></span>

<span data-ttu-id="c23fa-104">Berechnet das Punktprodukt einer Ebene und einen 4D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="c23fa-104">Computes the dot product of a plane and a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c23fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c23fa-105">Syntax</span></span>


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="c23fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c23fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c23fa-107">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c23fa-107">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c23fa-108">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="c23fa-108">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c23fa-109">Zeiger auf eine Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c23fa-109">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c23fa-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c23fa-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c23fa-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="c23fa-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="c23fa-112">Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c23fa-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c23fa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c23fa-113">Return value</span></span>

<span data-ttu-id="c23fa-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c23fa-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c23fa-115">Das Punktprodukt der Ebene und des 4D-Vektors.</span><span class="sxs-lookup"><span data-stu-id="c23fa-115">The dot product of the plane and 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c23fa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c23fa-116">Remarks</span></span>

<span data-ttu-id="c23fa-117">Wenn eine Ebene (a, b, c, d) und ein 4D-Vektor (x, y, z, w) angegeben wird, ist der Rückgabewert dieser Funktion ein \* x + b \* y + c \* z + d \* w.</span><span class="sxs-lookup"><span data-stu-id="c23fa-117">Given a plane (a, b, c, d) and a 4D vector (x, y, z, w) the return value of this function is a\*x + b\*y + c\*z + d\*w.</span></span> <span data-ttu-id="c23fa-118">Die **D3DXPlaneDot** -Funktion ist nützlich, um die Beziehung der Ebene mit einer homogenen Koordinate zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c23fa-118">The **D3DXPlaneDot** function is useful for determining the plane's relationship with a homogeneous coordinate.</span></span> <span data-ttu-id="c23fa-119">Diese Funktion kann z. b. verwendet werden, um zu bestimmen, ob sich eine bestimmte Koordinate auf einer bestimmten Ebene befindet oder auf welcher Seite einer bestimmten Ebene eine bestimmte Koordinate liegt.</span><span class="sxs-lookup"><span data-stu-id="c23fa-119">For example, this function could be used to determine if a particular coordinate is on a particular plane, or on which side of a particular plane a particular coordinate lies.</span></span>

## <a name="requirements"></a><span data-ttu-id="c23fa-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c23fa-120">Requirements</span></span>



| <span data-ttu-id="c23fa-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c23fa-121">Requirement</span></span> | <span data-ttu-id="c23fa-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c23fa-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c23fa-123">Header</span><span class="sxs-lookup"><span data-stu-id="c23fa-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c23fa-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c23fa-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c23fa-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c23fa-125">Library</span></span><br/> | <dl> <span data-ttu-id="c23fa-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c23fa-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c23fa-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c23fa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c23fa-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c23fa-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c23fa-129">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="c23fa-129">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> <dt>

[<span data-ttu-id="c23fa-130">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="c23fa-130">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
