---
description: Beenden eines aktiven Pass.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect:: endpass-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355007"
---
# <a name="id3dxeffectendpass-method"></a><span data-ttu-id="4e548-103">ID3DXEffect:: endpass-Methode</span><span class="sxs-lookup"><span data-stu-id="4e548-103">ID3DXEffect::EndPass method</span></span>

<span data-ttu-id="4e548-104">Beenden eines aktiven Pass.</span><span class="sxs-lookup"><span data-stu-id="4e548-104">End an active pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e548-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e548-105">Syntax</span></span>


```C++
HRESULT EndPass();
```



## <a name="parameters"></a><span data-ttu-id="4e548-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e548-106">Parameters</span></span>

<span data-ttu-id="4e548-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4e548-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e548-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e548-108">Return value</span></span>

<span data-ttu-id="4e548-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e548-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e548-110">Diese Methode gibt immer den Wert S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4e548-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e548-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e548-111">Remarks</span></span>

<span data-ttu-id="4e548-112">Eine Anwendung signalisiert das Ende des Renderings eines aktiven Pass durch Aufrufen von **ID3DXEffect:: endpass**.</span><span class="sxs-lookup"><span data-stu-id="4e548-112">An application signals the end of rendering an active pass by calling **ID3DXEffect::EndPass**.</span></span> <span data-ttu-id="4e548-113">Jede **ID3DXEffect:: endpass** -Aktivität muss Teil eines übereinstimmenden Paars von [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) -und **ID3DXEffect:: endpass** -aufrufen sein.</span><span class="sxs-lookup"><span data-stu-id="4e548-113">Each **ID3DXEffect::EndPass** must be part of a matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls.</span></span>

<span data-ttu-id="4e548-114">Jedes übereinstimmende Paar aus [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) -und **ID3DXEffect:: endpass** -aufrufen muss sich innerhalb eines übereinstimmenden Paares von [**ID3DXEffect:: begin**](id3dxeffect--begin.md) -und [**ID3DXEffect:: End**](id3dxeffect--end.md) -aufrufen befinden.</span><span class="sxs-lookup"><span data-stu-id="4e548-114">Each matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls must be located within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="4e548-115">Wenn die Anwendung in einem [](id3dxeffect.md) [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: endpass** -übereinstimmenden paar den Effekt Zustand ändert, muss Sie [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aufrufen, bevor ein drawxprimitiver-Aufrufvorgang Zustandsänderungen vor dem Rendering an das Gerät weitergibt.</span><span class="sxs-lookup"><span data-stu-id="4e548-115">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/**ID3DXEffect::EndPass** matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e548-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e548-116">Requirements</span></span>



| <span data-ttu-id="4e548-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e548-117">Requirement</span></span> | <span data-ttu-id="4e548-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4e548-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e548-119">Header</span><span class="sxs-lookup"><span data-stu-id="4e548-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4e548-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e548-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4e548-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e548-121">Library</span></span><br/> | <dl> <span data-ttu-id="4e548-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e548-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4e548-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e548-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e548-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="4e548-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




