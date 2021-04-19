---
description: Bestimmt das Punktprodukt von zwei 3D-Vektoren.
ms.assetid: 61aa7751-cc06-4673-929b-d7c1e691e395
title: D3DXVec3Dot-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22d6930a44f129154482f9b1aab24337e8bcdc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366460"
---
# <a name="d3dxvec3dot-function"></a><span data-ttu-id="02f8d-103">D3DXVec3Dot-Funktion</span><span class="sxs-lookup"><span data-stu-id="02f8d-103">D3DXVec3Dot function</span></span>

<span data-ttu-id="02f8d-104">Bestimmt das Punktprodukt von zwei 3D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="02f8d-104">Determines the dot product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02f8d-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Dot(
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="02f8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02f8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f8d-107">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02f8d-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f8d-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="02f8d-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="02f8d-109">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="02f8d-109">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="02f8d-110">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02f8d-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f8d-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="02f8d-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="02f8d-112">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="02f8d-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02f8d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02f8d-113">Return value</span></span>

<span data-ttu-id="02f8d-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02f8d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02f8d-115">Das Punkt-Produkt.</span><span class="sxs-lookup"><span data-stu-id="02f8d-115">The dot-product.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f8d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02f8d-116">Requirements</span></span>



| <span data-ttu-id="02f8d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02f8d-117">Requirement</span></span> | <span data-ttu-id="02f8d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="02f8d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02f8d-119">Header</span><span class="sxs-lookup"><span data-stu-id="02f8d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="02f8d-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="02f8d-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="02f8d-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02f8d-121">Library</span></span><br/> | <dl> <span data-ttu-id="02f8d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02f8d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02f8d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02f8d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f8d-124">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="02f8d-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="02f8d-125">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="02f8d-125">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
</dt> </dl>

 

 
