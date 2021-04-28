---
description: 'ID3DXMATRIXStack::GetTop-Methode (D3DX10.h): Ruft die aktuelle Matrix oben im Stapel ab.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: ID3DXMATRIXStack::GetTop-Methode (D3DX10.h)
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
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108038"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a><span data-ttu-id="d9aa5-103">ID3DXMATRIXStack::GetTop-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="d9aa5-103">ID3DXMATRIXStack::GetTop method (D3DX10.h)</span></span>

<span data-ttu-id="d9aa5-104">Ruft die aktuelle Matrix oben im Stapel ab.</span><span class="sxs-lookup"><span data-stu-id="d9aa5-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9aa5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9aa5-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="d9aa5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9aa5-106">Parameters</span></span>

<span data-ttu-id="d9aa5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d9aa5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9aa5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9aa5-108">Return value</span></span>

<span data-ttu-id="d9aa5-109">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d9aa5-109">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d9aa5-110">Diese Methode gibt einen Zeiger auf eine D3DXMATRIX-Struktur zurück, die die aktuelle Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9aa5-110">This method returns a pointer to a D3DXMATRIX structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9aa5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9aa5-111">Remarks</span></span>

<span data-ttu-id="d9aa5-112">Der von dieser Methode zurückgegebene D3DXMATRIX-Zeiger ist nach nachfolgenden Stapelvorgängen nicht garantiert gültig.</span><span class="sxs-lookup"><span data-stu-id="d9aa5-112">The D3DXMATRIX pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="d9aa5-113">Beachten Sie, dass diese Methode die aktuelle Matrix nicht vom anfang des Stapels entfernt. stattdessen wird nur die aktuelle Matrix zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d9aa5-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9aa5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9aa5-114">Requirements</span></span>



| <span data-ttu-id="d9aa5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9aa5-115">Requirement</span></span> | <span data-ttu-id="d9aa5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d9aa5-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9aa5-117">Header</span><span class="sxs-lookup"><span data-stu-id="d9aa5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d9aa5-118"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="d9aa5-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9aa5-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9aa5-119">Library</span></span><br/> | <dl> <span data-ttu-id="d9aa5-120"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9aa5-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9aa5-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9aa5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9aa5-122">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="d9aa5-122">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d9aa5-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d9aa5-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
