---
description: Bestimmt, ob eine Matrix eine Identitätsmatrix ist.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: D3DXMatrixIsIdentity-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355436"
---
# <a name="d3dxmatrixisidentity-function"></a><span data-ttu-id="4d78a-103">D3DXMatrixIsIdentity-Funktion</span><span class="sxs-lookup"><span data-stu-id="4d78a-103">D3DXMatrixIsIdentity function</span></span>

<span data-ttu-id="4d78a-104">Bestimmt, ob eine Matrix eine Identitätsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="4d78a-104">Determines if a matrix is an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d78a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d78a-105">Syntax</span></span>


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4d78a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d78a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d78a-107">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d78a-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d78a-108">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d78a-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4d78a-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die auf die Identität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="4d78a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d78a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d78a-110">Return value</span></span>

<span data-ttu-id="4d78a-111">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d78a-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d78a-112">Wenn die Matrix eine Identitätsmatrix ist, gibt diese Funktion " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="4d78a-112">If the matrix is an identity matrix, this function returns **TRUE**.</span></span> <span data-ttu-id="4d78a-113">Andernfalls gibt diese Funktion **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="4d78a-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d78a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d78a-114">Requirements</span></span>



| <span data-ttu-id="4d78a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d78a-115">Requirement</span></span> | <span data-ttu-id="4d78a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4d78a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d78a-117">Header</span><span class="sxs-lookup"><span data-stu-id="4d78a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4d78a-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d78a-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4d78a-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d78a-119">Library</span></span><br/> | <dl> <span data-ttu-id="4d78a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d78a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d78a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d78a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d78a-122">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4d78a-122">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4d78a-123">**D3DXMatrixIdentity**</span><span class="sxs-lookup"><span data-stu-id="4d78a-123">**D3DXMatrixIdentity**</span></span>](d3dxmatrixidentity.md)
</dt> </dl>

 

 
