---
description: Gibt die Länge eines 2D-Vektors zurück.
ms.assetid: 376fd2ca-c89d-41e7-a15c-a79d7281d010
title: D3DXVec2Length-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1753098d164cd67e79770a0ecfcf5db4d047c1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355002"
---
# <a name="d3dxvec2length-function"></a><span data-ttu-id="19ab4-103">D3DXVec2Length-Funktion</span><span class="sxs-lookup"><span data-stu-id="19ab4-103">D3DXVec2Length function</span></span>

<span data-ttu-id="19ab4-104">Gibt die Länge eines 2D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="19ab4-104">Returns the length of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ab4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ab4-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Length(
  _In_ const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="19ab4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ab4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ab4-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19ab4-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ab4-108">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="19ab4-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="19ab4-109">Ein Zeiger auf die Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="19ab4-109">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19ab4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19ab4-110">Return value</span></span>

<span data-ttu-id="19ab4-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19ab4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19ab4-112">Die Länge des Vektors.</span><span class="sxs-lookup"><span data-stu-id="19ab4-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ab4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19ab4-113">Requirements</span></span>



| <span data-ttu-id="19ab4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19ab4-114">Requirement</span></span> | <span data-ttu-id="19ab4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="19ab4-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19ab4-116">Header</span><span class="sxs-lookup"><span data-stu-id="19ab4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="19ab4-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ab4-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="19ab4-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19ab4-118">Library</span></span><br/> | <dl> <span data-ttu-id="19ab4-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19ab4-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19ab4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19ab4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ab4-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="19ab4-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="19ab4-122">**D3DXVec2LengthSq**</span><span class="sxs-lookup"><span data-stu-id="19ab4-122">**D3DXVec2LengthSq**</span></span>](d3dxvec2lengthsq.md)
</dt> </dl>

 

 
