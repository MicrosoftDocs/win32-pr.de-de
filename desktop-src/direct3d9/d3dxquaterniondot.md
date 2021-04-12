---
description: Gibt das Punktprodukt von zwei Quaternionen zurück.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: D3DXQuaternionDot-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355517"
---
# <a name="d3dxquaterniondot-function"></a><span data-ttu-id="dddf2-103">D3DXQuaternionDot-Funktion</span><span class="sxs-lookup"><span data-stu-id="dddf2-103">D3DXQuaternionDot function</span></span>

<span data-ttu-id="dddf2-104">Gibt das Punktprodukt von zwei Quaternionen zurück.</span><span class="sxs-lookup"><span data-stu-id="dddf2-104">Returns the dot product of two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="dddf2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dddf2-105">Syntax</span></span>


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="dddf2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dddf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dddf2-107">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dddf2-107">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dddf2-108">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="dddf2-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dddf2-109">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dddf2-109">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dddf2-110">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dddf2-110">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dddf2-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="dddf2-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dddf2-112">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dddf2-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dddf2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dddf2-113">Return value</span></span>

<span data-ttu-id="dddf2-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dddf2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dddf2-115">Das Punktprodukt von zwei Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="dddf2-115">The dot product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="dddf2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dddf2-116">Remarks</span></span>

<span data-ttu-id="dddf2-117">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="dddf2-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="dddf2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dddf2-118">Requirements</span></span>



| <span data-ttu-id="dddf2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dddf2-119">Requirement</span></span> | <span data-ttu-id="dddf2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dddf2-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dddf2-121">Header</span><span class="sxs-lookup"><span data-stu-id="dddf2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dddf2-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dddf2-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dddf2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dddf2-123">Library</span></span><br/> | <dl> <span data-ttu-id="dddf2-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dddf2-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dddf2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dddf2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dddf2-126">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="dddf2-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
