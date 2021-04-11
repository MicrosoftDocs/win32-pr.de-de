---
description: Entfernt die aktuelle Matrix vom oberen Rand des Stapels.
ms.assetid: 4c542012-058a-4818-8ec4-27e7d3357ca3
title: ID3DXMATRIXStack::P op-Methode (D3dx9math. h)
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
ms.openlocfilehash: 229892ab9b6a1ec75396b24cd9313e27667d0acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050840"
---
# <a name="id3dxmatrixstackpop-method-d3dx9mathh"></a><span data-ttu-id="aa377-103">ID3DXMATRIXStack::P op-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="aa377-103">ID3DXMATRIXStack::Pop method (D3dx9math.h)</span></span>

<span data-ttu-id="aa377-104">Entfernt die aktuelle Matrix vom oberen Rand des Stapels.</span><span class="sxs-lookup"><span data-stu-id="aa377-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa377-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa377-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="aa377-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa377-106">Parameters</span></span>

<span data-ttu-id="aa377-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="aa377-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa377-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa377-108">Return value</span></span>

<span data-ttu-id="aa377-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aa377-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aa377-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aa377-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa377-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa377-111">Remarks</span></span>

<span data-ttu-id="aa377-112">Beachten Sie, dass diese Methode die Anzahl der Elemente im Stapel um 1 verringert, wodurch die aktuelle Matrix aus dem Stapel Rand entfernt und eine Matrix an den Anfang des Stapels herauf gestuft wird.</span><span class="sxs-lookup"><span data-stu-id="aa377-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="aa377-113">Wenn die aktuelle Anzahl der Elemente auf dem Stapel 0 ist, wird diese Methode zurückgegeben, ohne eine Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="aa377-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="aa377-114">Wenn die aktuelle Anzahl der Elemente auf dem Stapel 1 ist, wird der Stapel von dieser Methode geleert.</span><span class="sxs-lookup"><span data-stu-id="aa377-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa377-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa377-115">Requirements</span></span>



| <span data-ttu-id="aa377-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa377-116">Requirement</span></span> | <span data-ttu-id="aa377-117">Wert</span><span class="sxs-lookup"><span data-stu-id="aa377-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa377-118">Header</span><span class="sxs-lookup"><span data-stu-id="aa377-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aa377-119"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa377-119"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="aa377-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa377-120">Library</span></span><br/> | <dl> <span data-ttu-id="aa377-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa377-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aa377-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa377-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa377-123">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="aa377-123">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="aa377-124">**ID3DXMATRIXStack:: GetTop**</span><span class="sxs-lookup"><span data-stu-id="aa377-124">**ID3DXMATRIXStack::GetTop**</span></span>](id3dxmatrixstack--gettop.md)
</dt> <dt>

[<span data-ttu-id="aa377-125">**ID3DXMATRIXStack::P USH**</span><span class="sxs-lookup"><span data-stu-id="aa377-125">**ID3DXMATRIXStack::Push**</span></span>](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




