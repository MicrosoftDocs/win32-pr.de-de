---
description: Bestimmt das Punktprodukt zweier 2D-Vektoren.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: D3DXVec2Dot-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 79b65127c415695b3df9f927b6edff8fcdd5c58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353710"
---
# <a name="d3dxvec2dot-function"></a><span data-ttu-id="3d983-103">D3DXVec2Dot-Funktion</span><span class="sxs-lookup"><span data-stu-id="3d983-103">D3DXVec2Dot function</span></span>

<span data-ttu-id="3d983-104">Bestimmt das Punktprodukt zweier 2D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="3d983-104">Determines the dot product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d983-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d983-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="3d983-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d983-107">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d983-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d983-108">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d983-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3d983-109">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d983-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d983-110">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d983-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d983-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d983-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3d983-112">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d983-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d983-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d983-113">Return value</span></span>

<span data-ttu-id="3d983-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d983-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d983-115">Das Skalarprodukt.</span><span class="sxs-lookup"><span data-stu-id="3d983-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d983-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d983-116">Requirements</span></span>



| <span data-ttu-id="3d983-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d983-117">Requirement</span></span> | <span data-ttu-id="3d983-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3d983-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d983-119">Header</span><span class="sxs-lookup"><span data-stu-id="3d983-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3d983-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d983-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3d983-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d983-121">Library</span></span><br/> | <dl> <span data-ttu-id="3d983-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d983-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d983-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d983-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d983-124">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3d983-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3d983-125">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="3d983-125">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
</dt> </dl>

 

 
