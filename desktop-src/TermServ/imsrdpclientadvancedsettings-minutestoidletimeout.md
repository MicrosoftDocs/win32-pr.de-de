---
title: Imsrdpclientadvancedsettings minutestoidletimeout-Eigenschaft
description: Gibt die maximale Zeitspanne in Minuten an, die der Client ohne Benutzereingabe verbunden bleiben soll. Wenn die angegebene Zeit verstrichen ist, ruft das Steuerelement die Methode "imstscaxevents onidletimeoutnotification" auf.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, minutestoidletimeout-Eigenschaft
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, minutestoidletimeout-Eigenschaft
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, minutestoidletimeout-Eigenschaft
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, minutestoidletimeout-Eigenschaft
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, minutestoidletimeout-Eigenschaft
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, minutestoidletimeout-Eigenschaft
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, minutestoidletimeout-Eigenschaft
- Minutestoidletimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, minutestoidletimeout-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342196"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a><span data-ttu-id="5fbb8-121">Imsrdpclientadvancedsettings:: minutestoidletimeout-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5fbb8-121">IMsRdpClientAdvancedSettings::MinutesToIdleTimeout property</span></span>

<span data-ttu-id="5fbb8-122">Gibt die maximale Zeitspanne in Minuten an, die der Client ohne Benutzereingabe verbunden bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-122">Specifies the maximum length of time, in minutes, that the client should remain connected without user input.</span></span> <span data-ttu-id="5fbb8-123">Wenn die angegebene Zeit verstrichen ist, ruft das Steuerelement die [**imstscaxevents:: onidletimeoutnotification**](imstscaxevents-onidletimeoutnotification.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-123">If the specified time elapses, the control calls the [**IMsTscAxEvents::OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) method.</span></span>

<span data-ttu-id="5fbb8-124">Sie können diese Eigenschaft in einer Situation verwenden, in der Sie eine Sitzung im Leerlauf trennen müssen. beispielsweise in einer Kiosk Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-124">You can use this property in a situation where you need to disconnect an idle session; for example, in a kiosk environment.</span></span>

<span data-ttu-id="5fbb8-125">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fbb8-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fbb8-126">Syntax</span></span>


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="5fbb8-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5fbb8-127">Property value</span></span>

<span data-ttu-id="5fbb8-128">Die neue Zeit in Minuten.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-128">The new time, in minutes.</span></span> <span data-ttu-id="5fbb8-129">Der Standardwert ist 0 (null), wodurch die Funktion deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-129">The default value is zero, which disables the feature.</span></span> <span data-ttu-id="5fbb8-130">Der Höchstwert ist 240, der vier Stunden darstellt.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-130">The maximum value is 240, which represents 4 hours.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5fbb8-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5fbb8-131">Error codes</span></span>

<span data-ttu-id="5fbb8-132">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-132">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fbb8-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fbb8-133">Remarks</span></span>

<span data-ttu-id="5fbb8-134">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5fbb8-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbb8-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fbb8-135">Requirements</span></span>



| <span data-ttu-id="5fbb8-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fbb8-136">Requirement</span></span> | <span data-ttu-id="5fbb8-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5fbb8-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fbb8-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fbb8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5fbb8-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fbb8-139">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="5fbb8-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fbb8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5fbb8-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fbb8-141">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="5fbb8-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5fbb8-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="5fbb8-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fbb8-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5fbb8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5fbb8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fbb8-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fbb8-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5fbb8-146">IID</span><span class="sxs-lookup"><span data-stu-id="5fbb8-146">IID</span></span><br/>                      | <span data-ttu-id="5fbb8-147">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="5fbb8-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fbb8-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fbb8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbb8-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5fbb8-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5fbb8-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5fbb8-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5fbb8-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5fbb8-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5fbb8-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5fbb8-156">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="5fbb8-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





