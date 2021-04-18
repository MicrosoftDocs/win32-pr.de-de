---
title: Imsrdpclientadvancedsettings-smartsizing-Eigenschaft
description: Gibt an, ob die Anzeige für den Client Bereich des Steuer Elements skaliert werden soll. Beachten Sie, dass Bild Lauf leisten nicht angezeigt werden, wenn die smartsizing-Eigenschaft aktiviert ist.
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- Smartsizing-Eigenschaft Remotedesktopdienste
- Smartsizing-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, smartsizing-Eigenschaft
- Smartsizing-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, smartsizing (Eigenschaft)
- Smartsizing-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, smartsizing (Eigenschaft)
- Smartsizing-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, smartsizing (Eigenschaft)
- Smartsizing-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, smartsizing (Eigenschaft)
- Smartsizing-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, smartsizing (Eigenschaft)
- Smartsizing-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, smartsizing (Eigenschaft)
- Smartsizing-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, smartsizing (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec2a825725e01d876b9e8658f215de6595f32f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391528"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a><span data-ttu-id="ff540-121">Imsrdpclientadvancedsettings:: smartsizing (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ff540-121">IMsRdpClientAdvancedSettings::SmartSizing property</span></span>

<span data-ttu-id="ff540-122">Gibt an, ob die Anzeige für den Client Bereich des Steuer Elements skaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff540-122">Specifies if the display should be scaled to fit the client area of the control.</span></span> <span data-ttu-id="ff540-123">Beachten Sie, dass Bild Lauf leisten nicht angezeigt werden, wenn die **smartsizing** -Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ff540-123">Note that scroll bars do not appear when the **SmartSizing** property is enabled.</span></span>

<span data-ttu-id="ff540-124">Im Gegensatz zu den meisten anderen Eigenschaften kann diese Eigenschaft festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ff540-124">Unlike most other properties, this property can be set when the control is connected.</span></span>

<span data-ttu-id="ff540-125">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ff540-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff540-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff540-126">Syntax</span></span>


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a><span data-ttu-id="ff540-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ff540-127">Property value</span></span>

<span data-ttu-id="ff540-128">Legen Sie diesen Parameter auf **Variant \_ false** fest, um das Feature zu deaktivieren, oder **Variant \_ true** , um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ff540-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ff540-129">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ff540-129">Error codes</span></span>

<span data-ttu-id="ff540-130">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ff540-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff540-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff540-131">Remarks</span></span>

<span data-ttu-id="ff540-132">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ff540-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff540-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff540-133">Requirements</span></span>



| <span data-ttu-id="ff540-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff540-134">Requirement</span></span> | <span data-ttu-id="ff540-135">Wert</span><span class="sxs-lookup"><span data-stu-id="ff540-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff540-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff540-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ff540-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff540-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ff540-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff540-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ff540-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff540-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ff540-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ff540-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff540-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff540-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ff540-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ff540-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff540-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff540-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ff540-144">IID</span><span class="sxs-lookup"><span data-stu-id="ff540-144">IID</span></span><br/>                      | <span data-ttu-id="ff540-145">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="ff540-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff540-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff540-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff540-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ff540-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ff540-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ff540-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ff540-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ff540-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ff540-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ff540-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ff540-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ff540-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ff540-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ff540-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ff540-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ff540-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ff540-154">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="ff540-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





