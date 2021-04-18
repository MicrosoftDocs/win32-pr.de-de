---
description: Gibt die Länge einer Quaternion zurück.
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: D3DXQuaternionLength-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f54136e7e34ba05442f98b25438dd03b7b5f211
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394213"
---
# <a name="d3dxquaternionlength-function"></a><span data-ttu-id="1723a-103">D3DXQuaternionLength-Funktion</span><span class="sxs-lookup"><span data-stu-id="1723a-103">D3DXQuaternionLength function</span></span>

<span data-ttu-id="1723a-104">Gibt die Länge einer Quaternion zurück.</span><span class="sxs-lookup"><span data-stu-id="1723a-104">Returns the length of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="1723a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1723a-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="1723a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1723a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1723a-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1723a-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1723a-108">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1723a-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1723a-109">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1723a-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1723a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1723a-110">Return value</span></span>

<span data-ttu-id="1723a-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1723a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1723a-112">Die Länge der Quaternion.</span><span class="sxs-lookup"><span data-stu-id="1723a-112">The quaternion's length.</span></span>

## <a name="remarks"></a><span data-ttu-id="1723a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1723a-113">Remarks</span></span>

<span data-ttu-id="1723a-114">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="1723a-114">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="1723a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1723a-115">Requirements</span></span>



| <span data-ttu-id="1723a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1723a-116">Requirement</span></span> | <span data-ttu-id="1723a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1723a-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1723a-118">Header</span><span class="sxs-lookup"><span data-stu-id="1723a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1723a-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1723a-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1723a-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1723a-120">Library</span></span><br/> | <dl> <span data-ttu-id="1723a-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1723a-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1723a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1723a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1723a-123">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1723a-123">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1723a-124">**D3DXQuaternionLengthSq**</span><span class="sxs-lookup"><span data-stu-id="1723a-124">**D3DXQuaternionLengthSq**</span></span>](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
