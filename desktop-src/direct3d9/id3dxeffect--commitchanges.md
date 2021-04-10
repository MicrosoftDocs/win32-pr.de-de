---
description: Weitergeben von Zustandsänderungen, die innerhalb eines aktiven Durchlaufs an das Gerät erfolgen, vor dem Rendering.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'ID3DXEffect:: CommitChanges-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219545"
---
# <a name="id3dxeffectcommitchanges-method"></a><span data-ttu-id="03d82-103">ID3DXEffect:: CommitChanges-Methode</span><span class="sxs-lookup"><span data-stu-id="03d82-103">ID3DXEffect::CommitChanges method</span></span>

<span data-ttu-id="03d82-104">Weitergeben von Zustandsänderungen, die innerhalb eines aktiven Durchlaufs an das Gerät erfolgen, vor dem Rendering.</span><span class="sxs-lookup"><span data-stu-id="03d82-104">Propagate state changes that occur inside of an active pass to the device before rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d82-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03d82-105">Syntax</span></span>


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a><span data-ttu-id="03d82-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03d82-106">Parameters</span></span>

<span data-ttu-id="03d82-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="03d82-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03d82-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03d82-108">Return value</span></span>

<span data-ttu-id="03d82-109">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03d82-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03d82-110">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="03d82-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="03d82-111">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="03d82-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="03d82-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03d82-112">Remarks</span></span>

<span data-ttu-id="03d82-113">Wenn die Anwendung einen Effekt Zustand mithilfe einer der [**ID3DXEffect:: SETX**](id3dxeffect.md) -Methoden innerhalb eines [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) -Vergleichs Paars ändert, muss die Anwendung **ID3DXEffect:: CommitChanges** aufrufen, bevor ein drawxprimitiver-Befehl vor dem Rendering Zustandsänderungen an das Gerät weitergibt.</span><span class="sxs-lookup"><span data-stu-id="03d82-113">If the application changes any effect state using any of the [**ID3DXEffect::Setx**](id3dxeffect.md) methods inside of an [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call **ID3DXEffect::CommitChanges** before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span> <span data-ttu-id="03d82-114">Wenn keine Zustandsänderungen innerhalb eines **ID3DXEffect:: beginpass** -und **ID3DXEffect:: endpass** -übereinstimmenden Paars auftreten, ist es nicht erforderlich, **ID3DXEffect:: CommitChanges** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="03d82-114">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

<span data-ttu-id="03d82-115">Dies unterscheidet sich geringfügig von freigegebenen Parametern in einem geklonten Effekt.</span><span class="sxs-lookup"><span data-stu-id="03d82-115">This is slightly different for any shared parameters in a cloned effect.</span></span> <span data-ttu-id="03d82-116">Wenn eine Technik für einen geklonten Effekt aktiv ist (d. h., wenn [**ID3DXEffect:: begin**](id3dxeffect--begin.md) aufgerufen wurde, aber [**ID3DXEffect:: End**](id3dxeffect--end.md) nicht aufgerufen wurde), aktualisiert **ID3DXEffect:: CommitChanges** Parameter, die nicht wie erwartet freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="03d82-116">When a technique is active on a cloned effect (that is, when [**ID3DXEffect::Begin**](id3dxeffect--begin.md) has been called but and [**ID3DXEffect::End**](id3dxeffect--end.md) has not been called), **ID3DXEffect::CommitChanges** updates parameters that are not shared as expected.</span></span> <span data-ttu-id="03d82-117">Um einen freigegebenen Parameter (nur für einen geklonten Effekt mit aktiver Technik) zu aktualisieren, rufen Sie **ID3DXEffect:: End** auf, um die Technik zu deaktivieren, und **ID3DXEffect:: begin** , um die Technik vor dem Aufrufen von **ID3DXEffect:: CommitChanges** erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="03d82-117">To update a shared parameter (only for a cloned effect whose technique is active), call **ID3DXEffect::End** to deactivate the technique and **ID3DXEffect::Begin** to reactivate the technique before calling **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d82-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03d82-118">Requirements</span></span>



| <span data-ttu-id="03d82-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03d82-119">Requirement</span></span> | <span data-ttu-id="03d82-120">Wert</span><span class="sxs-lookup"><span data-stu-id="03d82-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d82-121">Header</span><span class="sxs-lookup"><span data-stu-id="03d82-121">Header</span></span><br/>  | <dl> <span data-ttu-id="03d82-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d82-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="03d82-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03d82-123">Library</span></span><br/> | <dl> <span data-ttu-id="03d82-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03d82-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="03d82-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03d82-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d82-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="03d82-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




