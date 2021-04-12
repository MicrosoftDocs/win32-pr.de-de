---
description: Gibt die Determinante einer Matrix zurück.
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: D3DXMatrixDeterminant-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 53d90d70e75ba4bb92dbed3abe7ee06eae1ae6e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354207"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="c51cb-103">D3DXMatrixDeterminant-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c51cb-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="c51cb-104">Gibt die Determinante einer Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="c51cb-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c51cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c51cb-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c51cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c51cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c51cb-107">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c51cb-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c51cb-108">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c51cb-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c51cb-109">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c51cb-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c51cb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c51cb-110">Return value</span></span>

<span data-ttu-id="c51cb-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c51cb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c51cb-112">Gibt den Determinanten der Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="c51cb-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c51cb-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c51cb-113">Requirements</span></span>



| <span data-ttu-id="c51cb-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c51cb-114">Requirement</span></span> | <span data-ttu-id="c51cb-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c51cb-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c51cb-116">Header</span><span class="sxs-lookup"><span data-stu-id="c51cb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c51cb-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c51cb-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c51cb-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c51cb-118">Library</span></span><br/> | <dl> <span data-ttu-id="c51cb-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c51cb-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c51cb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c51cb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51cb-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c51cb-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
