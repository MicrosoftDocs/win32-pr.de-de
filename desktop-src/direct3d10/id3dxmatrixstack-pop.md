---
description: Entfernt die aktuelle Matrix vom oberen Rand des Stapels.
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: ID3DXMATRIXStack::P op-Methode (d3dx10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a9a7b88cc749ef61c8b04395497fcc00ea9b36ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367402"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a><span data-ttu-id="018cf-103">ID3DXMATRIXStack::P op-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="018cf-103">ID3DXMATRIXStack::Pop method (D3DX10.h)</span></span>

<span data-ttu-id="018cf-104">Entfernt die aktuelle Matrix vom oberen Rand des Stapels.</span><span class="sxs-lookup"><span data-stu-id="018cf-104">Removes the current matrix from the top of the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="018cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="018cf-105">Syntax</span></span>


```C++
HRESULT Pop();
```



## <a name="parameters"></a><span data-ttu-id="018cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="018cf-106">Parameters</span></span>

<span data-ttu-id="018cf-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="018cf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="018cf-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="018cf-108">Return value</span></span>

<span data-ttu-id="018cf-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="018cf-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="018cf-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="018cf-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="018cf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="018cf-111">Remarks</span></span>

<span data-ttu-id="018cf-112">Beachten Sie, dass diese Methode die Anzahl der Elemente im Stapel um 1 verringert, wodurch die aktuelle Matrix aus dem Stapel Rand entfernt und eine Matrix an den Anfang des Stapels herauf gestuft wird.</span><span class="sxs-lookup"><span data-stu-id="018cf-112">Note that this method decrements the count of items on the stack by 1, effectively removing the current matrix from the top of the stack and promoting a matrix to the top of the stack.</span></span> <span data-ttu-id="018cf-113">Wenn die aktuelle Anzahl der Elemente auf dem Stapel 0 ist, wird diese Methode zurückgegeben, ohne eine Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="018cf-113">If the current count of items on the stack is 0, then this method returns without performing any action.</span></span> <span data-ttu-id="018cf-114">Wenn die aktuelle Anzahl der Elemente auf dem Stapel 1 ist, wird der Stapel von dieser Methode geleert.</span><span class="sxs-lookup"><span data-stu-id="018cf-114">If the current count of items on the stack is 1, then this method empties the stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="018cf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="018cf-115">Requirements</span></span>



| <span data-ttu-id="018cf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="018cf-116">Requirement</span></span> | <span data-ttu-id="018cf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="018cf-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="018cf-118">Header</span><span class="sxs-lookup"><span data-stu-id="018cf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="018cf-119"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="018cf-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="018cf-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="018cf-120">Library</span></span><br/> | <dl> <span data-ttu-id="018cf-121"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="018cf-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="018cf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="018cf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="018cf-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="018cf-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="018cf-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="018cf-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




