---
description: Ruft eine Beschreibung eines angegebenen Animations Ereignisses ab.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'ID3DXAnimationController:: GetEventDesc-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357278"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a><span data-ttu-id="72261-103">ID3DXAnimationController:: GetEventDesc-Methode</span><span class="sxs-lookup"><span data-stu-id="72261-103">ID3DXAnimationController::GetEventDesc method</span></span>

<span data-ttu-id="72261-104">Ruft eine Beschreibung eines angegebenen Animations Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="72261-104">Gets a description of a specified animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="72261-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72261-105">Syntax</span></span>


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="72261-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="72261-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72261-107">*hevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72261-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72261-108">Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="72261-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="72261-109">Ereignis Handle für ein Animations Ereignis, das beschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="72261-109">Event handle to an animation event to describe.</span></span>

</dd> <dt>

<span data-ttu-id="72261-110">*PDE SC* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72261-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72261-111">Typ: **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="72261-111">Type: **[**LPD3DXEVENT\_DESC**](d3dxevent-desc.md)**</span></span>

<span data-ttu-id="72261-112">Zeiger auf eine [**D3DXEVENT- \_ decoderstruktur**](d3dxevent-desc.md) , die eine Beschreibung des Animations Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="72261-112">Pointer to a [**D3DXEVENT\_DESC**](d3dxevent-desc.md) structure that contains a description of the animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72261-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72261-113">Return value</span></span>

<span data-ttu-id="72261-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="72261-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="72261-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="72261-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="72261-116">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="72261-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="72261-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72261-117">Requirements</span></span>



| <span data-ttu-id="72261-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72261-118">Requirement</span></span> | <span data-ttu-id="72261-119">Wert</span><span class="sxs-lookup"><span data-stu-id="72261-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72261-120">Header</span><span class="sxs-lookup"><span data-stu-id="72261-120">Header</span></span><br/>  | <dl> <span data-ttu-id="72261-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="72261-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="72261-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="72261-122">Library</span></span><br/> | <dl> <span data-ttu-id="72261-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72261-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72261-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72261-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72261-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="72261-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




