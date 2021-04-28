---
description: 'D3DXMatrixDeterminant-Funktion (D3DX10Math.h): Gibt die Determinante einer Matrix zurück.'
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: D3DXMatrixDeterminant-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 894db23a3079c1344c97cab00642cbbc0953450d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103458"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="deb4e-103">D3DXMatrixDeterminant-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="deb4e-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="deb4e-104">Gibt die Determinante einer Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="deb4e-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="deb4e-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="deb4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="deb4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb4e-107">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="deb4e-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb4e-108">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="deb4e-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="deb4e-109">Zeiger auf die D3DXMATRIX-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="deb4e-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb4e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="deb4e-110">Return value</span></span>

<span data-ttu-id="deb4e-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deb4e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deb4e-112">Gibt die Determinante der Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="deb4e-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb4e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deb4e-113">Requirements</span></span>



| <span data-ttu-id="deb4e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deb4e-114">Requirement</span></span> | <span data-ttu-id="deb4e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="deb4e-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="deb4e-116">Header</span><span class="sxs-lookup"><span data-stu-id="deb4e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="deb4e-117"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="deb4e-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="deb4e-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="deb4e-118">Library</span></span><br/> | <dl> <span data-ttu-id="deb4e-119"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="deb4e-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="deb4e-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="deb4e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb4e-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="deb4e-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
