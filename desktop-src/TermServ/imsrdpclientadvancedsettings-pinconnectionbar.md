---
title: Imsrdpclientadvancedsettings pinconnectionbar (Eigenschaft)
description: Gibt den Status der UI-Verbindungs Leiste an.
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- Pinconnectionbar-Eigenschaft Remotedesktopdienste
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, pinconnectionbar-Eigenschaft
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, pinconnectionbar (Eigenschaft)
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, pinconnectionbar (Eigenschaft)
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, pinconnectionbar (Eigenschaft)
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, pinconnectionbar (Eigenschaft)
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, pinconnectionbar (Eigenschaft)
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, pinconnectionbar (Eigenschaft)
- Pinconnectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, pinconnectionbar (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858664"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a><span data-ttu-id="14596-120">Imsrdpclientadvancedsettings::P inconnectionbar-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14596-120">IMsRdpClientAdvancedSettings::PinConnectionBar property</span></span>

<span data-ttu-id="14596-121">Gibt den Status der UI-Verbindungs Leiste an.</span><span class="sxs-lookup"><span data-stu-id="14596-121">Specifies the state of the UI connection bar.</span></span>

<span data-ttu-id="14596-122">Diese Eigenschaft gibt **E \_ notimpl** zurück, wenn der Container die [**iobjectafety:: setinterfacesafetyoptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="14596-122">This property returns **E\_NOTIMPL** if the container calls the [**IObjectSafety::SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) method.</span></span>

<span data-ttu-id="14596-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="14596-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="14596-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="14596-124">Syntax</span></span>


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="14596-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="14596-125">Property value</span></span>

<span data-ttu-id="14596-126">Wenn diese Eigenschaft auf **Variant \_ true** festgelegt wird, wird der Status auf "gesenkt" festgelegt, d. h. für den Benutzer unsichtbar und nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="14596-126">Setting this property to **VARIANT\_TRUE** sets the state to "lowered", that is, invisible to the user and unavailable for input.</span></span> <span data-ttu-id="14596-127">**Variant \_ FALSE** legt den Zustand auf "ausgelöst" fest und ist für Benutzereingaben verfügbar.</span><span class="sxs-lookup"><span data-stu-id="14596-127">**VARIANT\_FALSE** sets the state to "raised" and available for user input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14596-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="14596-128">Error codes</span></span>

<span data-ttu-id="14596-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="14596-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="14596-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14596-130">Remarks</span></span>

<span data-ttu-id="14596-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="14596-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14596-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14596-132">Requirements</span></span>



| <span data-ttu-id="14596-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14596-133">Requirement</span></span> | <span data-ttu-id="14596-134">Wert</span><span class="sxs-lookup"><span data-stu-id="14596-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14596-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14596-135">Minimum supported client</span></span><br/> | <span data-ttu-id="14596-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14596-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="14596-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14596-137">Minimum supported server</span></span><br/> | <span data-ttu-id="14596-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14596-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="14596-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="14596-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="14596-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14596-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="14596-141">DLL</span><span class="sxs-lookup"><span data-stu-id="14596-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14596-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14596-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="14596-143">IID</span><span class="sxs-lookup"><span data-stu-id="14596-143">IID</span></span><br/>                      | <span data-ttu-id="14596-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="14596-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14596-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14596-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14596-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="14596-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="14596-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="14596-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="14596-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="14596-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="14596-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="14596-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="14596-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="14596-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="14596-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="14596-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="14596-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="14596-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="14596-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="14596-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

