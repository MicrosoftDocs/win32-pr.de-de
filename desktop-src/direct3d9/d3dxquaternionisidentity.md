---
description: Bestimmt, ob eine Quaternion eine Identitäts-Quaternion ist.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: D3DXQuaternionIsIdentity-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363171"
---
# <a name="d3dxquaternionisidentity-function"></a><span data-ttu-id="9e0ae-103">D3DXQuaternionIsIdentity-Funktion</span><span class="sxs-lookup"><span data-stu-id="9e0ae-103">D3DXQuaternionIsIdentity function</span></span>

<span data-ttu-id="9e0ae-104">Bestimmt, ob eine Quaternion eine Identitäts-Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="9e0ae-104">Determines if a quaternion is an identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e0ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e0ae-105">Syntax</span></span>


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="9e0ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e0ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e0ae-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e0ae-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e0ae-108">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e0ae-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9e0ae-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die auf die Identität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="9e0ae-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e0ae-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e0ae-110">Return value</span></span>

<span data-ttu-id="9e0ae-111">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e0ae-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e0ae-112">Wenn die Quaternion eine Identitäts-Quaternion ist, gibt diese Funktion " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="9e0ae-112">If the quaternion is an identity quaternion, this function returns **TRUE**.</span></span> <span data-ttu-id="9e0ae-113">Andernfalls gibt diese Funktion **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="9e0ae-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e0ae-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e0ae-114">Remarks</span></span>

<span data-ttu-id="9e0ae-115">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e0ae-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0ae-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e0ae-116">Requirements</span></span>



| <span data-ttu-id="9e0ae-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e0ae-117">Requirement</span></span> | <span data-ttu-id="9e0ae-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9e0ae-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0ae-119">Header</span><span class="sxs-lookup"><span data-stu-id="9e0ae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9e0ae-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e0ae-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9e0ae-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e0ae-121">Library</span></span><br/> | <dl> <span data-ttu-id="9e0ae-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e0ae-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e0ae-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e0ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0ae-124">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9e0ae-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9e0ae-125">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="9e0ae-125">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
</dt> </dl>

 

 
