---
title: Imsrdpclientadvancedsettings-Eigenschaft grabfocusonconnect
description: Gibt an, ob das Client Steuerelement während der Verbindungs Herstellung den Fokus haben soll.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, Eigenschaft ' grabfocusonconnect '
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, grabfocusonconnect (Eigenschaft)
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, grabfocusonconnect (Eigenschaft)
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, grabfocusonconnect (Eigenschaft)
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, grabfocusonconnect (Eigenschaft)
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, grabfocusonconnect (Eigenschaft)
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, grabfocusonconnect (Eigenschaft)
- Grabfocusonconnect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, grabfocusonconnect (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339590"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a><span data-ttu-id="00544-120">Imsrdpclientadvancedsettings:: grabfocusonconnect-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="00544-120">IMsRdpClientAdvancedSettings::GrabFocusOnConnect property</span></span>

<span data-ttu-id="00544-121">Gibt an, ob das Client Steuerelement während der Verbindungs Herstellung den Fokus haben soll.</span><span class="sxs-lookup"><span data-stu-id="00544-121">Specifies if the client control should have the focus while connecting.</span></span> <span data-ttu-id="00544-122">Das-Steuerelement versucht nicht, den Fokus von einem Fenster zu erhalten, das in einem anderen Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00544-122">The control will not attempt to grab focus from a window running in a different process.</span></span>

<span data-ttu-id="00544-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="00544-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="00544-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="00544-124">Syntax</span></span>


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a><span data-ttu-id="00544-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="00544-125">Property value</span></span>

<span data-ttu-id="00544-126">Legen Sie diesen Parameter auf **Variant \_ false** fest, um das Feature zu deaktivieren, oder **Variant \_ true** , um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="00544-126">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="00544-127">Das Festlegen dieser Eigenschaft auf **Variant \_ false** verhindert, dass das Steuerelement beim Herstellen der Verbindung den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="00544-127">Setting this property to **VARIANT\_FALSE** prevents the control from grabbing focus when connecting.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00544-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="00544-128">Error codes</span></span>

<span data-ttu-id="00544-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="00544-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="00544-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00544-130">Remarks</span></span>

<span data-ttu-id="00544-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="00544-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00544-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00544-132">Requirements</span></span>



| <span data-ttu-id="00544-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00544-133">Requirement</span></span> | <span data-ttu-id="00544-134">Wert</span><span class="sxs-lookup"><span data-stu-id="00544-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00544-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00544-135">Minimum supported client</span></span><br/> | <span data-ttu-id="00544-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00544-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="00544-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00544-137">Minimum supported server</span></span><br/> | <span data-ttu-id="00544-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00544-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="00544-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="00544-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="00544-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00544-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="00544-141">DLL</span><span class="sxs-lookup"><span data-stu-id="00544-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00544-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00544-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="00544-143">IID</span><span class="sxs-lookup"><span data-stu-id="00544-143">IID</span></span><br/>                      | <span data-ttu-id="00544-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="00544-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="00544-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00544-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00544-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="00544-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="00544-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="00544-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="00544-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="00544-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="00544-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="00544-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="00544-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="00544-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="00544-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="00544-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="00544-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="00544-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="00544-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="00544-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





