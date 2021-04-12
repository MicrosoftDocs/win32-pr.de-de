---
title: Imstscaxevents onremotedesktopsizechange-Methode
description: Wird aufgerufen, um anzugeben, dass sich die Größe des Client Steuer Elements auf dem Remote Desktop als Reaktion auf einen Client Steuerungs Vorgang geändert hat.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Onremotedesktopsizechange-Methode Remotedesktopdienste
- Onremotedesktopsizechange-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onremotedesktopsizechange-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518053"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a><span data-ttu-id="a2f8a-106">Imstscaxevents:: onremotedesktopsizechange-Methode</span><span class="sxs-lookup"><span data-stu-id="a2f8a-106">IMsTscAxEvents::OnRemoteDesktopSizeChange method</span></span>

<span data-ttu-id="a2f8a-107">Wird aufgerufen, um anzugeben, dass sich die Größe des Client Steuer Elements auf dem Remote Desktop als Reaktion auf einen Client Steuerungs Vorgang geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a2f8a-107">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f8a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2f8a-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="a2f8a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2f8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2f8a-110">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2f8a-110">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2f8a-111">Breite der Größe des Remote Desktops in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a2f8a-111">Width, in pixels, of the resized remote desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a2f8a-112">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2f8a-112">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2f8a-113">Höhe der Größe des Remote Desktops in Pixel.</span><span class="sxs-lookup"><span data-stu-id="a2f8a-113">Height, in pixels, of the resized remote desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2f8a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2f8a-114">Return value</span></span>

<span data-ttu-id="a2f8a-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a2f8a-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2f8a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2f8a-116">Remarks</span></span>

<span data-ttu-id="a2f8a-117">Dieses Ereignis ermöglicht dem Container festzustellen, ob seine Größe als Reaktion auf einen Client Steuerungs Vorgang geändert werden muss. Dies kann zu einer größeren sichtbaren Desktop Größe führen.</span><span class="sxs-lookup"><span data-stu-id="a2f8a-117">This event allows the container to determine if it must resize itself in response to a client control operation, which could result in a larger viewable desktop size.</span></span> <span data-ttu-id="a2f8a-118">Beachten Sie, dass das Steuerelement Scrollleisten automatisch für die neue Sitzungs Größe anpasst.</span><span class="sxs-lookup"><span data-stu-id="a2f8a-118">Note that the control will automatically adjust scroll bars for the new session size.</span></span>

<span data-ttu-id="a2f8a-119">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a2f8a-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f8a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2f8a-120">Requirements</span></span>



| <span data-ttu-id="a2f8a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2f8a-121">Requirement</span></span> | <span data-ttu-id="a2f8a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a2f8a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f8a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2f8a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2f8a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2f8a-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a2f8a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2f8a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2f8a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2f8a-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a2f8a-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a2f8a-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2f8a-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2f8a-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a2f8a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a2f8a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2f8a-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2f8a-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a2f8a-131">IID</span><span class="sxs-lookup"><span data-stu-id="a2f8a-131">IID</span></span><br/>                      | <span data-ttu-id="a2f8a-132">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="a2f8a-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a2f8a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2f8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f8a-134">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="a2f8a-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





