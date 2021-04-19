---
description: Fügt dem Stapel eine Matrix hinzu.
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: ID3DXMATRIXStack::P USH-Methode (d3dx10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 694bb8b02f340be14f38b7d2a44ec2038d175098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367497"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="1cab5-103">ID3DXMATRIXStack::P USH-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="1cab5-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="1cab5-104">Fügt dem Stapel eine Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="1cab5-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cab5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cab5-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="1cab5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cab5-106">Parameters</span></span>

<span data-ttu-id="1cab5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1cab5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cab5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cab5-108">Return value</span></span>

<span data-ttu-id="1cab5-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1cab5-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1cab5-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1cab5-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1cab5-111">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="1cab5-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cab5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cab5-112">Remarks</span></span>

<span data-ttu-id="1cab5-113">Mit dieser Methode wird die Anzahl der Elemente im Stapel um 1 erhöht, und die aktuelle Matrix wird duplizieren.</span><span class="sxs-lookup"><span data-stu-id="1cab5-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="1cab5-114">Der Stapel vergrößert sich dynamisch, wenn weitere Elemente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1cab5-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cab5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cab5-115">Requirements</span></span>



| <span data-ttu-id="1cab5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cab5-116">Requirement</span></span> | <span data-ttu-id="1cab5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1cab5-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cab5-118">Header</span><span class="sxs-lookup"><span data-stu-id="1cab5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1cab5-119"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cab5-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cab5-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1cab5-120">Library</span></span><br/> | <dl> <span data-ttu-id="1cab5-121"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cab5-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cab5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cab5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cab5-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="1cab5-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="1cab5-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1cab5-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




