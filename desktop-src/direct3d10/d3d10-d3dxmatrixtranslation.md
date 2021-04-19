---
description: Erstellen Sie eine Übersetzungs Matrix.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: D3DXMatrixTranslation-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363176"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a><span data-ttu-id="6125b-103">D3DXMatrixTranslation-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6125b-103">D3DXMatrixTranslation function (D3DX10Math.h)</span></span>

<span data-ttu-id="6125b-104">Erstellen Sie eine Übersetzungs Matrix.</span><span class="sxs-lookup"><span data-stu-id="6125b-104">Create a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6125b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6125b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="6125b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6125b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6125b-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6125b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6125b-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6125b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6125b-109">Die Matrix, die zu einer Übersetzungs Matrix wird.</span><span class="sxs-lookup"><span data-stu-id="6125b-109">The matrix that will become a translation matrix.</span></span> <span data-ttu-id="6125b-110">Siehe [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="6125b-110">See [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="6125b-111">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6125b-111">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6125b-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6125b-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6125b-113">Die x-Komponente der Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="6125b-113">The x-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="6125b-114">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6125b-114">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6125b-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6125b-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6125b-116">Die y-Komponente der Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="6125b-116">The y-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="6125b-117">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6125b-117">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6125b-118">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6125b-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6125b-119">Die z-Komponente der Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="6125b-119">The z-component of the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6125b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6125b-120">Return value</span></span>

<span data-ttu-id="6125b-121">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6125b-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6125b-122">Die Translationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="6125b-122">The translation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="6125b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6125b-123">Requirements</span></span>



| <span data-ttu-id="6125b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6125b-124">Requirement</span></span> | <span data-ttu-id="6125b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6125b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6125b-126">Header</span><span class="sxs-lookup"><span data-stu-id="6125b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6125b-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6125b-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6125b-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6125b-128">Library</span></span><br/> | <dl> <span data-ttu-id="6125b-129"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6125b-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6125b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6125b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6125b-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6125b-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
