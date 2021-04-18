---
description: Gibt das Quadrat der Länge einer Quaternion zurück.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: D3DXQuaternionLengthSq-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0771d571b15ef690b115f12e5fa1d8ff6fea4dad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354400"
---
# <a name="d3dxquaternionlengthsq-function"></a><span data-ttu-id="5241c-103">D3DXQuaternionLengthSq-Funktion</span><span class="sxs-lookup"><span data-stu-id="5241c-103">D3DXQuaternionLengthSq function</span></span>

<span data-ttu-id="5241c-104">Gibt das Quadrat der Länge einer Quaternion zurück.</span><span class="sxs-lookup"><span data-stu-id="5241c-104">Returns the square of the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="5241c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5241c-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="5241c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5241c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5241c-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5241c-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5241c-108">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="5241c-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="5241c-109">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5241c-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5241c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5241c-110">Return value</span></span>

<span data-ttu-id="5241c-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5241c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5241c-112">Die Quadrat Länge der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="5241c-112">The quaternion's squared length.</span></span>

## <a name="remarks"></a><span data-ttu-id="5241c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5241c-113">Remarks</span></span>

<span data-ttu-id="5241c-114">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="5241c-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="5241c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5241c-115">Requirements</span></span>



| <span data-ttu-id="5241c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5241c-116">Requirement</span></span> | <span data-ttu-id="5241c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5241c-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5241c-118">Header</span><span class="sxs-lookup"><span data-stu-id="5241c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5241c-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5241c-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5241c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5241c-120">Library</span></span><br/> | <dl> <span data-ttu-id="5241c-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5241c-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5241c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5241c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5241c-123">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5241c-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5241c-124">**D3DXQuaternionLength**</span><span class="sxs-lookup"><span data-stu-id="5241c-124">**D3DXQuaternionLength**</span></span>](d3dxquaternionlength.md)
</dt> </dl>

 

 
