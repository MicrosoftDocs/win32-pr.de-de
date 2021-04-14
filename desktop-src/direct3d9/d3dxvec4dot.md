---
description: Bestimmt das Punktprodukt von zwei 4D-Vektoren.
ms.assetid: 565dede8-6cc8-4313-9480-2f252cac94f2
title: D3DXVec4Dot-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0ef075a768fe9b70a38a4bc3d88b094359bd546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394149"
---
# <a name="d3dxvec4dot-function"></a><span data-ttu-id="68ab6-103">D3DXVec4Dot-Funktion</span><span class="sxs-lookup"><span data-stu-id="68ab6-103">D3DXVec4Dot function</span></span>

<span data-ttu-id="68ab6-104">Bestimmt das Punktprodukt von zwei 4D-Vektoren.</span><span class="sxs-lookup"><span data-stu-id="68ab6-104">Determines the dot product of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ab6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ab6-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Dot(
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="68ab6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68ab6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68ab6-107">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68ab6-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68ab6-108">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="68ab6-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="68ab6-109">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="68ab6-109">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="68ab6-110">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68ab6-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68ab6-111">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="68ab6-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="68ab6-112">Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="68ab6-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68ab6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68ab6-113">Return value</span></span>

<span data-ttu-id="68ab6-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68ab6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68ab6-115">Das Skalarprodukt.</span><span class="sxs-lookup"><span data-stu-id="68ab6-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ab6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68ab6-116">Requirements</span></span>



| <span data-ttu-id="68ab6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68ab6-117">Requirement</span></span> | <span data-ttu-id="68ab6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="68ab6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68ab6-119">Header</span><span class="sxs-lookup"><span data-stu-id="68ab6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="68ab6-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68ab6-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="68ab6-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68ab6-121">Library</span></span><br/> | <dl> <span data-ttu-id="68ab6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68ab6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68ab6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68ab6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ab6-124">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="68ab6-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="68ab6-125">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="68ab6-125">**D3DXVec4Cross**</span></span>](d3dxvec4cross.md)
</dt> </dl>

 

 
