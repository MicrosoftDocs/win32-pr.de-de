---
description: Ruft die aktuelle Matrix am Anfang des Stapels ab.
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack:: GetTop-Methode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361187"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="d078b-103">ID3DXMATRIXStack:: GetTop-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d078b-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="d078b-104">Ruft die aktuelle Matrix am Anfang des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="d078b-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d078b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d078b-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="d078b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d078b-106">Parameters</span></span>

<span data-ttu-id="d078b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d078b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d078b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d078b-108">Return value</span></span>

<span data-ttu-id="d078b-109">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d078b-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d078b-110">Diese Methode gibt einen Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur zurück, die die aktuelle Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="d078b-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d078b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d078b-111">Remarks</span></span>

<span data-ttu-id="d078b-112">Der von dieser Methode zurückgegebene [**D3DXMATRIX**](d3dxmatrix.md) -Zeiger ist nach nachfolgenden Stapel Vorgängen nicht garantiert gültig.</span><span class="sxs-lookup"><span data-stu-id="d078b-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="d078b-113">Beachten Sie, dass diese Methode nicht die aktuelle Matrix von der obersten Position des Stapels entfernt. Stattdessen wird nur die aktuelle Matrix zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d078b-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d078b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d078b-114">Requirements</span></span>



| <span data-ttu-id="d078b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d078b-115">Requirement</span></span> | <span data-ttu-id="d078b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d078b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d078b-117">Header</span><span class="sxs-lookup"><span data-stu-id="d078b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d078b-118"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d078b-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d078b-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d078b-119">Library</span></span><br/> | <dl> <span data-ttu-id="d078b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d078b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d078b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d078b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d078b-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="d078b-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d078b-123">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="d078b-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="d078b-124">**ID3DXMATRIXStack::P USH**</span><span class="sxs-lookup"><span data-stu-id="d078b-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




