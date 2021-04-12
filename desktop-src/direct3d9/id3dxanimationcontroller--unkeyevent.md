---
description: Entfernt ein angegebenes Ereignis aus einem Animations Titel und verhindert die Ausführung des Ereignisses.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'ID3DXAnimationController:: unkeyevent-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355946"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a><span data-ttu-id="80391-103">ID3DXAnimationController:: unkeyevent-Methode</span><span class="sxs-lookup"><span data-stu-id="80391-103">ID3DXAnimationController::UnkeyEvent method</span></span>

<span data-ttu-id="80391-104">Entfernt ein angegebenes Ereignis aus einem Animations Titel und verhindert die Ausführung des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="80391-104">Removes a specified event from an animation track, preventing the execution of the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="80391-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80391-105">Syntax</span></span>


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="80391-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="80391-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80391-107">*hevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80391-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80391-108">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="80391-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="80391-109">Ereignis Handle für das Ereignis, das aus dem Animations Titel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="80391-109">Event handle to the event to be removed from the animation track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80391-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80391-110">Return value</span></span>

<span data-ttu-id="80391-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80391-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80391-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80391-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="80391-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="80391-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="80391-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80391-114">Requirements</span></span>



| <span data-ttu-id="80391-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80391-115">Requirement</span></span> | <span data-ttu-id="80391-116">Wert</span><span class="sxs-lookup"><span data-stu-id="80391-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80391-117">Header</span><span class="sxs-lookup"><span data-stu-id="80391-117">Header</span></span><br/>  | <dl> <span data-ttu-id="80391-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="80391-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="80391-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="80391-119">Library</span></span><br/> | <dl> <span data-ttu-id="80391-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80391-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80391-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80391-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80391-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="80391-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




