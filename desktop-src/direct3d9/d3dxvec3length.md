---
description: Gibt die Länge eines 3D-Vektors zurück.
ms.assetid: 78da506c-3169-48e9-934c-cc09271a10d4
title: D3DXVec3Length-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 653e53fb22961c858c7649f95e4453fec08087fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370420"
---
# <a name="d3dxvec3length-function"></a><span data-ttu-id="53ace-103">D3DXVec3Length-Funktion</span><span class="sxs-lookup"><span data-stu-id="53ace-103">D3DXVec3Length function</span></span>

<span data-ttu-id="53ace-104">Gibt die Länge eines 3D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="53ace-104">Returns the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ace-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53ace-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Length(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="53ace-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53ace-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53ace-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53ace-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53ace-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="53ace-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="53ace-109">Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="53ace-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53ace-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53ace-110">Return value</span></span>

<span data-ttu-id="53ace-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53ace-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53ace-112">Die Länge des Vektors.</span><span class="sxs-lookup"><span data-stu-id="53ace-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="53ace-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53ace-113">Requirements</span></span>



| <span data-ttu-id="53ace-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53ace-114">Requirement</span></span> | <span data-ttu-id="53ace-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53ace-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53ace-116">Header</span><span class="sxs-lookup"><span data-stu-id="53ace-116">Header</span></span><br/>  | <dl> <span data-ttu-id="53ace-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="53ace-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="53ace-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53ace-118">Library</span></span><br/> | <dl> <span data-ttu-id="53ace-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53ace-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53ace-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53ace-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ace-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="53ace-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="53ace-122">**D3DXVec3LengthSq**</span><span class="sxs-lookup"><span data-stu-id="53ace-122">**D3DXVec3LengthSq**</span></span>](d3dxvec3lengthsq.md)
</dt> </dl>

 

 
