---
description: Gibt die Länge eines 4D-Vektors zurück.
ms.assetid: cb332160-3e3d-41b9-bfb0-e3b743d2eafd
title: D3DXVec4Length-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Length
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea16c6406c217f5e5d76af68a5da3a0c8bd17b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961774"
---
# <a name="d3dxvec4length-function"></a><span data-ttu-id="57275-103">D3DXVec4Length-Funktion</span><span class="sxs-lookup"><span data-stu-id="57275-103">D3DXVec4Length function</span></span>

<span data-ttu-id="57275-104">Gibt die Länge eines 4D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="57275-104">Returns the length of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="57275-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57275-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Length(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="57275-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57275-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57275-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57275-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57275-108">Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="57275-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="57275-109">Ein Zeiger auf die Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="57275-109">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57275-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57275-110">Return value</span></span>

<span data-ttu-id="57275-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57275-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57275-112">Die Länge des Vektors.</span><span class="sxs-lookup"><span data-stu-id="57275-112">The vector's length.</span></span>

## <a name="requirements"></a><span data-ttu-id="57275-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57275-113">Requirements</span></span>



| <span data-ttu-id="57275-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57275-114">Requirement</span></span> | <span data-ttu-id="57275-115">Wert</span><span class="sxs-lookup"><span data-stu-id="57275-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57275-116">Header</span><span class="sxs-lookup"><span data-stu-id="57275-116">Header</span></span><br/>  | <dl> <span data-ttu-id="57275-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="57275-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="57275-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="57275-118">Library</span></span><br/> | <dl> <span data-ttu-id="57275-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57275-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57275-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57275-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57275-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="57275-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="57275-122">**D3DXVec4LengthSq**</span><span class="sxs-lookup"><span data-stu-id="57275-122">**D3DXVec4LengthSq**</span></span>](d3dxvec4lengthsq.md)
</dt> </dl>

 

 
