---
description: 'ID3DXMATRIXStack::P ush-Methode (D3DX10.h): Fügt dem Stapel eine Matrix hinzu.'
ms.assetid: 8660047f-64bc-4b34-8270-3087412db942
title: ID3DXMATRIXStack::P ush-Methode (D3DX10.h)
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
ms.openlocfilehash: 9c248fdaed8235c383388a52172021921e2c78d8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107917"
---
# <a name="id3dxmatrixstackpush-method-d3dx10h"></a><span data-ttu-id="53e02-103">ID3DXMATRIXStack::P ush-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="53e02-103">ID3DXMATRIXStack::Push method (D3DX10.h)</span></span>

<span data-ttu-id="53e02-104">Fügt dem Stapel eine Matrix hinzu.</span><span class="sxs-lookup"><span data-stu-id="53e02-104">Adds a matrix to the stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53e02-105">Syntax</span></span>


```C++
HRESULT Push();
```



## <a name="parameters"></a><span data-ttu-id="53e02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53e02-106">Parameters</span></span>

<span data-ttu-id="53e02-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="53e02-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53e02-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53e02-108">Return value</span></span>

<span data-ttu-id="53e02-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53e02-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53e02-110">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53e02-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="53e02-111">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="53e02-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e02-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53e02-112">Remarks</span></span>

<span data-ttu-id="53e02-113">Diese Methode erhöht die Anzahl der Elemente im Stapel um 1 und dupliziert die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="53e02-113">This method increments the count of items on the stack by 1, duplicating the current matrix.</span></span> <span data-ttu-id="53e02-114">Der Stapel wächst dynamisch, wenn weitere Elemente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="53e02-114">The stack will grow dynamically as more items are added.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e02-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53e02-115">Requirements</span></span>



| <span data-ttu-id="53e02-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53e02-116">Requirement</span></span> | <span data-ttu-id="53e02-117">Wert</span><span class="sxs-lookup"><span data-stu-id="53e02-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53e02-118">Header</span><span class="sxs-lookup"><span data-stu-id="53e02-118">Header</span></span><br/>  | <dl> <span data-ttu-id="53e02-119"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="53e02-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="53e02-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53e02-120">Library</span></span><br/> | <dl> <span data-ttu-id="53e02-121"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="53e02-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e02-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53e02-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e02-123">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="53e02-123">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="53e02-124">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="53e02-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




