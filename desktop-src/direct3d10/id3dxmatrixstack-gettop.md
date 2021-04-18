---
description: Ruft die aktuelle Matrix am Anfang des Stapels ab.
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'ID3DXMATRIXStack:: GetTop-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364400"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="2bc2b-103">ID3DXMATRIXStack:: GetTop-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="2bc2b-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="2bc2b-104">Ruft die aktuelle Matrix am Anfang des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc2b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bc2b-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="2bc2b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bc2b-106">Parameters</span></span>

<span data-ttu-id="2bc2b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bc2b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bc2b-108">Return value</span></span>

<span data-ttu-id="2bc2b-109">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2bc2b-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2bc2b-110">Diese Methode gibt einen Zeiger auf eine D3DXMATRIX-Struktur zurück, die die aktuelle Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc2b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bc2b-111">Remarks</span></span>

<span data-ttu-id="2bc2b-112">Der von dieser Methode zurückgegebene D3DXMATRIX-Zeiger ist nach nachfolgenden Stapel Vorgängen nicht garantiert gültig.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="2bc2b-113">Beachten Sie, dass diese Methode nicht die aktuelle Matrix von der obersten Position des Stapels entfernt. Stattdessen wird nur die aktuelle Matrix zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc2b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bc2b-114">Requirements</span></span>



| <span data-ttu-id="2bc2b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bc2b-115">Requirement</span></span> | <span data-ttu-id="2bc2b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2bc2b-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc2b-117">Header</span><span class="sxs-lookup"><span data-stu-id="2bc2b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2bc2b-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc2b-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bc2b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2bc2b-119">Library</span></span><br/> | <dl> <span data-ttu-id="2bc2b-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bc2b-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc2b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2bc2b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc2b-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2bc2b-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2bc2b-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2bc2b-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
