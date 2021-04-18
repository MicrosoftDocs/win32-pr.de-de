---
title: Imsrdpclientadvancedsettings overallconnectiontimeout (Eigenschaft)
description: Gibt die Gesamt Zeitdauer in Sekunden an, die das Client Steuerelement auf den Abschluss einer Verbindung wartet.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
- overallconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, overallconnectiontimeout (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340320"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a><span data-ttu-id="c2b88-120">Imsrdpclientadvancedsettings:: overallconnectiontimeout-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2b88-120">IMsRdpClientAdvancedSettings::overallConnectionTimeout property</span></span>

<span data-ttu-id="c2b88-121">Gibt die Gesamt Zeitdauer in Sekunden an, die das Client Steuerelement auf den Abschluss einer Verbindung wartet.</span><span class="sxs-lookup"><span data-stu-id="c2b88-121">Specifies the total length of time, in seconds, that the client control waits for a connection to complete.</span></span>

<span data-ttu-id="c2b88-122">Wenn die angegebene Zeitspanne abläuft, bevor die Verbindung abgeschlossen ist, trennt das Steuerelement die Verbindung und ruft die [**imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="c2b88-122">If the specified time elapses before connection completes, the control disconnects and calls the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) method.</span></span>

<span data-ttu-id="c2b88-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c2b88-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b88-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2b88-124">Syntax</span></span>


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="c2b88-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2b88-125">Property value</span></span>

<span data-ttu-id="c2b88-126">Die neue Zeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c2b88-126">The new time, in seconds.</span></span> <span data-ttu-id="c2b88-127">Der Höchstwert ist 600, der 10 Minuten darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2b88-127">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2b88-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c2b88-128">Error codes</span></span>

<span data-ttu-id="c2b88-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c2b88-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2b88-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2b88-130">Remarks</span></span>

<span data-ttu-id="c2b88-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c2b88-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b88-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2b88-132">Requirements</span></span>



| <span data-ttu-id="c2b88-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2b88-133">Requirement</span></span> | <span data-ttu-id="c2b88-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c2b88-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b88-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2b88-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b88-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2b88-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c2b88-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2b88-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b88-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2b88-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c2b88-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c2b88-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2b88-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b88-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c2b88-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c2b88-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2b88-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b88-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c2b88-143">IID</span><span class="sxs-lookup"><span data-stu-id="c2b88-143">IID</span></span><br/>                      | <span data-ttu-id="c2b88-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="c2b88-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2b88-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2b88-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b88-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c2b88-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c2b88-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c2b88-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c2b88-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c2b88-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c2b88-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c2b88-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c2b88-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c2b88-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c2b88-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c2b88-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c2b88-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c2b88-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c2b88-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="c2b88-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c2b88-154">**singleconnectiontimeout**</span><span class="sxs-lookup"><span data-stu-id="c2b88-154">**singleConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





