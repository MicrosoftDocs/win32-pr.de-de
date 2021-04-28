---
description: 'ID3DXMATRIXStack::P ush-Methode (D3dx9math.h): Fügt dem Stapel eine Matrix hinzu.'
ms.assetid: 99bc636d-f1fd-4ace-a649-6a1a952927e0
title: ID3DXMATRIXStack::P ush-Methode (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Push
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aeaf40d3164d6bd9d892d30f352fd24467b24ddb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093503"
---
# <a name="id3dxmatrixstackpush-method-d3dx9mathh"></a><span data-ttu-id="8c1e9-103">ID3DXMATRIXStack::P ush-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8c1e9-103">ID3DXMATRIXStack::Push method (D3dx9math.h)</span></span>

<span data-ttu-id="8c1e9-104">Fügt dem Stapel eine Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c1e9-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c1e9-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="8c1e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c1e9-106">Parameters</span></span>

<span data-ttu-id="8c1e9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8c1e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c1e9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c1e9-108">Return value</span></span>

<span data-ttu-id="8c1e9-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c1e9-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c1e9-110">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c1e9-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8c1e9-111">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="8c1e9-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c1e9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c1e9-112">Remarks</span></span>

<span data-ttu-id="8c1e9-113">Diese Methode erhöht die Anzahl der Elemente im Stapel um 1, wodurch die aktuelle Matrix dupliziert wird.</span><span class="sxs-lookup"><span data-stu-id="8c1e9-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="8c1e9-114">Der Stapel wächst dynamisch, wenn weitere Elemente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8c1e9-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c1e9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c1e9-115">Requirements</span></span>



| <span data-ttu-id="8c1e9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c1e9-116">Requirement</span></span> | <span data-ttu-id="8c1e9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8c1e9-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1e9-118">Header</span><span class="sxs-lookup"><span data-stu-id="8c1e9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8c1e9-119"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8c1e9-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c1e9-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c1e9-120">Library</span></span><br/> | <dl> <span data-ttu-id="8c1e9-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c1e9-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c1e9-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8c1e9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c1e9-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="8c1e9-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8c1e9-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="8c1e9-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="8c1e9-125">**ID3DXMATRIXStack::P op**</span><span class="sxs-lookup"><span data-stu-id="8c1e9-125">**ID3DXMATRIXStack::Pop**</span></span>](id3dxmatrixstack--pop.md)
</dt> </dl>

 

 




