---
description: 'D3DXMatrixDeterminant-Funktion (D3dx9math.h): Gibt die Determinante einer Matrix zurück.'
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: D3DXMatrixDeterminant-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d54651e11f1b3de02803d9ea123ca7eff24d7a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098168"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="227b3-103">D3DXMatrixDeterminant-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="227b3-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="227b3-104">Gibt die Determinante einer Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="227b3-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="227b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="227b3-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="227b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="227b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="227b3-107">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="227b3-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="227b3-108">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="227b3-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="227b3-109">Zeiger auf die [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="227b3-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="227b3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="227b3-110">Return value</span></span>

<span data-ttu-id="227b3-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="227b3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="227b3-112">Gibt die Determinante der Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="227b3-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="227b3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="227b3-113">Requirements</span></span>



| <span data-ttu-id="227b3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="227b3-114">Requirement</span></span> | <span data-ttu-id="227b3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="227b3-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="227b3-116">Header</span><span class="sxs-lookup"><span data-stu-id="227b3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="227b3-117"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="227b3-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="227b3-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="227b3-118">Library</span></span><br/> | <dl> <span data-ttu-id="227b3-119"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="227b3-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="227b3-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="227b3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="227b3-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="227b3-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
