---
title: Imsrdpclientadvancedsettings singleconnectiontimeout (Eigenschaft)
description: Gibt die maximale Zeitspanne in Sekunden an, die das Client Steuerelement auf eine Verbindung mit einer IP-Adresse wartet.
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, singleconnectiontimeout-Eigenschaft
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, singleconnectiontimeout (Eigenschaft)
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, singleconnectiontimeout (Eigenschaft)
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, singleconnectiontimeout (Eigenschaft)
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, singleconnectiontimeout (Eigenschaft)
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, singleconnectiontimeout (Eigenschaft)
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, singleconnectiontimeout (Eigenschaft)
- singleconnectiontimeout-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, singleconnectiontimeout (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391529"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a><span data-ttu-id="69aaa-120">Imsrdpclientadvancedsettings:: singleconnectiontimeout (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="69aaa-120">IMsRdpClientAdvancedSettings::singleConnectionTimeout property</span></span>

<span data-ttu-id="69aaa-121">Gibt die maximale Zeitspanne in Sekunden an, die das Client Steuerelement auf eine Verbindung mit einer IP-Adresse wartet.</span><span class="sxs-lookup"><span data-stu-id="69aaa-121">Specifies the maximum length of time, in seconds, that the client control waits for a connection to an IP address.</span></span>

<span data-ttu-id="69aaa-122">Während der Verbindung kann das Steuerelement versuchen, eine Verbindung mit mehreren IP-Adressen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="69aaa-122">During connection, the control may attempt to connect to multiple IP addresses.</span></span>

<span data-ttu-id="69aaa-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="69aaa-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="69aaa-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="69aaa-124">Syntax</span></span>


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="69aaa-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="69aaa-125">Property value</span></span>

<span data-ttu-id="69aaa-126">Die neue Zeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="69aaa-126">The new time, in seconds.</span></span> <span data-ttu-id="69aaa-127">Der Höchstwert ist 600.</span><span class="sxs-lookup"><span data-stu-id="69aaa-127">The maximum value is 600.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69aaa-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="69aaa-128">Error codes</span></span>

<span data-ttu-id="69aaa-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="69aaa-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="69aaa-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69aaa-130">Remarks</span></span>

<span data-ttu-id="69aaa-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="69aaa-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69aaa-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69aaa-132">Requirements</span></span>



| <span data-ttu-id="69aaa-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69aaa-133">Requirement</span></span> | <span data-ttu-id="69aaa-134">Wert</span><span class="sxs-lookup"><span data-stu-id="69aaa-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69aaa-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69aaa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="69aaa-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69aaa-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="69aaa-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69aaa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="69aaa-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69aaa-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="69aaa-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="69aaa-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="69aaa-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69aaa-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="69aaa-141">DLL</span><span class="sxs-lookup"><span data-stu-id="69aaa-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69aaa-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69aaa-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="69aaa-143">IID</span><span class="sxs-lookup"><span data-stu-id="69aaa-143">IID</span></span><br/>                      | <span data-ttu-id="69aaa-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="69aaa-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69aaa-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69aaa-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69aaa-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="69aaa-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="69aaa-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="69aaa-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="69aaa-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="69aaa-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="69aaa-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="69aaa-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="69aaa-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="69aaa-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="69aaa-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="69aaa-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="69aaa-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="69aaa-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="69aaa-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="69aaa-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="69aaa-154">**overallconnectiontimeout**</span><span class="sxs-lookup"><span data-stu-id="69aaa-154">**overallConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





