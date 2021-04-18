---
description: Gibt die Determinante einer Matrix zurück.
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: D3DXMatrixDeterminant-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11b1092427b12c33d8c34c9f1bbd5e09cf1ccf2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355049"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="d28f2-103">D3DXMatrixDeterminant-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d28f2-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="d28f2-104">Gibt die Determinante einer Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="d28f2-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d28f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d28f2-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d28f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d28f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d28f2-107">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d28f2-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d28f2-108">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d28f2-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d28f2-109">Ein Zeiger auf die Quell-D3DXMATRIX-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d28f2-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d28f2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d28f2-110">Return value</span></span>

<span data-ttu-id="d28f2-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d28f2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d28f2-112">Gibt den Determinanten der Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="d28f2-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d28f2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d28f2-113">Requirements</span></span>



| <span data-ttu-id="d28f2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d28f2-114">Requirement</span></span> | <span data-ttu-id="d28f2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d28f2-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d28f2-116">Header</span><span class="sxs-lookup"><span data-stu-id="d28f2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d28f2-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d28f2-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d28f2-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d28f2-118">Library</span></span><br/> | <dl> <span data-ttu-id="d28f2-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d28f2-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d28f2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d28f2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d28f2-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d28f2-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
