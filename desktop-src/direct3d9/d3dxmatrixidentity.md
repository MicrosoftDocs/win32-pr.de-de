---
description: Erstellt eine Identitätsmatrix.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: D3DXMatrixIdentity-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961550"
---
# <a name="d3dxmatrixidentity-function"></a><span data-ttu-id="eb63a-103">D3DXMatrixIdentity-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb63a-103">D3DXMatrixIdentity function</span></span>

<span data-ttu-id="eb63a-104">Erstellt eine Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="eb63a-104">Creates an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb63a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb63a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="eb63a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb63a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb63a-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eb63a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb63a-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb63a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eb63a-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="eb63a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb63a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb63a-110">Return value</span></span>

<span data-ttu-id="eb63a-111">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb63a-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="eb63a-112">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Identitätsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="eb63a-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the identity matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb63a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb63a-113">Remarks</span></span>

<span data-ttu-id="eb63a-114">Die Identitätsmatrix ist eine Matrix, in der alle Koeffizienten 0 (null) sind, mit Ausnahme der \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 Koeffizienten \] , die auf 1 festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="eb63a-114">The identity matrix is a matrix in which all coefficients are 0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.</span></span> <span data-ttu-id="eb63a-115">Die Identitätsmatrix ist ein besonderes, da Sie bei der Anwendung auf Vertices nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="eb63a-115">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="eb63a-116">Die Identitätsmatrix dient als Ausgangspunkt für Matrizen, die Scheitelpunkt Werte ändern, um Drehungen, Übersetzungen und andere Transformationen zu erstellen, die durch eine 4-X4-Matrix dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="eb63a-116">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4 x4 matrix.</span></span>

<span data-ttu-id="eb63a-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eb63a-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="eb63a-118">Auf diese Weise kann die **D3DXMatrixIdentity** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb63a-118">In this way, the **D3DXMatrixIdentity** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb63a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb63a-119">Requirements</span></span>



| <span data-ttu-id="eb63a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb63a-120">Requirement</span></span> | <span data-ttu-id="eb63a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="eb63a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb63a-122">Header</span><span class="sxs-lookup"><span data-stu-id="eb63a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eb63a-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb63a-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eb63a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb63a-124">Library</span></span><br/> | <dl> <span data-ttu-id="eb63a-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb63a-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb63a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb63a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb63a-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="eb63a-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eb63a-128">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="eb63a-128">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




