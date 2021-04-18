---
title: IMsRdpClientAdvancedSettings2 enableautoreconnetct (Eigenschaft)
description: Gibt an, ob das Client Steuerelement das automatische erneute Herstellen einer Verbindung mit einer Sitzung im Falle einer Netzwerk Trennung aktivieren soll.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, enableautoreconnetct (Eigenschaft)
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, enableautoreconnetct (Eigenschaft)
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, enableautoreconnetct (Eigenschaft)
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, enableautoreconnetct (Eigenschaft)
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, enableautoreconnetct (Eigenschaft)
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, enableautoreconnetct (Eigenschaft)
- Enableautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, enableautoreconnetct (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344073"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a><span data-ttu-id="a71f2-118">IMsRdpClientAdvancedSettings2:: enableautoreconnetct-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a71f2-118">IMsRdpClientAdvancedSettings2::EnableAutoReconnect property</span></span>

<span data-ttu-id="a71f2-119">Gibt an, ob das Client Steuerelement das automatische erneute Herstellen einer Verbindung mit einer Sitzung im Falle einer Netzwerk Trennung aktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="a71f2-119">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span>

<span data-ttu-id="a71f2-120">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a71f2-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a71f2-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="a71f2-121">Syntax</span></span>


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="a71f2-122">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a71f2-122">Property value</span></span>

<span data-ttu-id="a71f2-123">Legen Sie auf **Variant \_ true** fest, um die automatische erneute Verbindung zu aktivieren, und auf **Variant \_ false** , um Sie zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a71f2-123">Set to **VARIANT\_TRUE** to enable automatic reconnection, and to **VARIANT\_FALSE** to disable it.</span></span> <span data-ttu-id="a71f2-124">Der Standardwert ist **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="a71f2-124">The default is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a71f2-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a71f2-125">Error codes</span></span>

<span data-ttu-id="a71f2-126">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a71f2-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a71f2-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a71f2-127">Remarks</span></span>

<span data-ttu-id="a71f2-128">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a71f2-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="a71f2-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a71f2-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a71f2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a71f2-130">Requirements</span></span>



| <span data-ttu-id="a71f2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a71f2-131">Requirement</span></span> | <span data-ttu-id="a71f2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a71f2-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a71f2-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a71f2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a71f2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a71f2-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a71f2-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a71f2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a71f2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a71f2-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a71f2-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a71f2-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a71f2-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a71f2-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a71f2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a71f2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a71f2-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a71f2-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a71f2-141">IID</span><span class="sxs-lookup"><span data-stu-id="a71f2-141">IID</span></span><br/>                      | <span data-ttu-id="a71f2-142">IID \_ IMsRdpClientAdvancedSettings2 ist als 9ac42117-2b76-4320-aa44-0e616ab8437b definiert.</span><span class="sxs-lookup"><span data-stu-id="a71f2-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a71f2-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a71f2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a71f2-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a71f2-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a71f2-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a71f2-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a71f2-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a71f2-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a71f2-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a71f2-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a71f2-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a71f2-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a71f2-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a71f2-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a71f2-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a71f2-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





