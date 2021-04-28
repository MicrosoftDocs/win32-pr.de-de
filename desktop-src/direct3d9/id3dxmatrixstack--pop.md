---
description: 'ID3DXMATRIXStack::P op-Methode (D3dx9math.h): Entfernt die aktuelle Matrix vom anfang des Stapels.'
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: ID3DXMATRIXStack::P op-Methode (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8d9185d10b9ef98a1fc3499f49c2ccc9c17a366
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093502"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="ea10b-103">ID3DXMATRIXStack::P op-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="ea10b-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="ea10b-104">Entfernt die aktuelle Matrix vom anfang des Stapels.</span><span class="sxs-lookup"><span data-stu-id="ea10b-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea10b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea10b-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="ea10b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea10b-106">Parameters</span></span>

<span data-ttu-id="ea10b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ea10b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea10b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea10b-108">Return value</span></span>

<span data-ttu-id="ea10b-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea10b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea10b-110">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea10b-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea10b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea10b-111">Remarks</span></span>

<span data-ttu-id="ea10b-112">Beachten Sie, dass diese Methode die Anzahl der Elemente im Stapel um 1 dekrementiert, indem die aktuelle Matrix effektiv von der obersten Seite des Stapels entfernt und eine Matrix an den Anfang des Stapels hoch gerechnet wird.</span><span class="sxs-lookup"><span data-stu-id="ea10b-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="ea10b-113">Wenn die aktuelle Anzahl von Elementen im Stapel 0 beträgt, gibt diese Methode zurück, ohne eine Aktion ausführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ea10b-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="ea10b-114">Wenn die aktuelle Anzahl von Elementen im Stapel 1 beträgt, leert diese Methode den Stapel.</span><span class="sxs-lookup"><span data-stu-id="ea10b-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea10b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea10b-115">Requirements</span></span>



| <span data-ttu-id="ea10b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea10b-116">Requirement</span></span> | <span data-ttu-id="ea10b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ea10b-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea10b-118">Header</span><span class="sxs-lookup"><span data-stu-id="ea10b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ea10b-119"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea10b-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ea10b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ea10b-120">Library</span></span><br/> | <dl> <span data-ttu-id="ea10b-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea10b-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea10b-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ea10b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea10b-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ea10b-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ea10b-124">**ID3DXMATRIXStack::GetTop**</span><span class="sxs-lookup"><span data-stu-id="ea10b-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="ea10b-125">**ID3DXMATRIXStack::P ush**</span><span class="sxs-lookup"><span data-stu-id="ea10b-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




