---
description: 'ID3DXMATRIXStack::GetTop-Methode (D3dx9math.h): Ruft die aktuelle Matrix oben im Stapel ab.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: ID3DXMATRIXStack::GetTop-Methode (D3dx9math.h)
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
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093578"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a><span data-ttu-id="c3e96-103">ID3DXMATRIXStack::GetTop-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c3e96-103">ID3DXMATRIXStack::GetTop method (D3dx9math.h)</span></span>

<span data-ttu-id="c3e96-104">Ruft die aktuelle Matrix am oberen Rand des Stapels ab.</span><span class="sxs-lookup"><span data-stu-id="c3e96-104">Retrieves the current matrix at the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e96-105">Syntax</span></span>


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a><span data-ttu-id="c3e96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3e96-106">Parameters</span></span>

<span data-ttu-id="c3e96-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c3e96-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3e96-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3e96-108">Return value</span></span>

<span data-ttu-id="c3e96-109">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3e96-109">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c3e96-110">Diese Methode gibt einen Zeiger auf eine [**D3DXMATRIX-Struktur**](d3dxmatrix.md) zurück, die die aktuelle Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3e96-110">This method returns a pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure representing the current matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3e96-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3e96-111">Remarks</span></span>

<span data-ttu-id="c3e96-112">Der von dieser Methode [**zurückgegebene D3DXMATRIX-Zeiger**](d3dxmatrix.md) ist nach nachfolgenden Stapelvorgängen nicht garantiert gültig.</span><span class="sxs-lookup"><span data-stu-id="c3e96-112">The [**D3DXMATRIX**](d3dxmatrix.md) pointer returned by this method is not guaranteed to be valid after subsequent stack operations.</span></span>

<span data-ttu-id="c3e96-113">Beachten Sie, dass diese Methode die aktuelle Matrix nicht vom Anfang des Stapels entfernt. stattdessen wird nur die aktuelle Matrix zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c3e96-113">Note that this method does not remove the current matrix from the top of the stack; rather, it just returns the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3e96-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3e96-114">Requirements</span></span>



| <span data-ttu-id="c3e96-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3e96-115">Requirement</span></span> | <span data-ttu-id="c3e96-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c3e96-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e96-117">Header</span><span class="sxs-lookup"><span data-stu-id="c3e96-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3e96-118"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c3e96-118"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c3e96-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3e96-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3e96-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3e96-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3e96-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c3e96-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e96-122">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="c3e96-122">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c3e96-123">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="c3e96-123">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> <dt>

[<span data-ttu-id="c3e96-124">**ID3DXMATRIXStack::P ush**</span><span class="sxs-lookup"><span data-stu-id="c3e96-124">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




