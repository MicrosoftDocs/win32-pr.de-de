---
title: Imsrdpclientadvancedsettings displayconnectionbar (Eigenschaft)
description: Gibt an, ob die Verbindungs Leiste verwendet werden soll. Der Standardwert ist Variant \_ true, wodurch die-Eigenschaft aktiviert wird.
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- Display connectionbar-Eigenschaft Remotedesktopdienste
- Displayconnectionbar-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, displayconnectionbar-Eigenschaft
- Display connectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, displayconnectionbar-Eigenschaft
- Display connectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, displayconnectionbar-Eigenschaft
- Display connectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, displayconnectionbar-Eigenschaft
- Display connectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, displayconnectionbar-Eigenschaft
- Display connectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, displayconnectionbar-Eigenschaft
- Display connectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, displayconnectionbar-Eigenschaft
- Display connectionbar-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, displayconnectionbar-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339551"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a><span data-ttu-id="d7dd7-121">Imsrdpclientadvancedsettings::D isplayconnectionbar-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d7dd7-121">IMsRdpClientAdvancedSettings::DisplayConnectionBar property</span></span>

<span data-ttu-id="d7dd7-122">Gibt an, ob die Verbindungs Leiste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-122">Specifies whether to use the connection bar.</span></span> <span data-ttu-id="d7dd7-123">Der Standardwert ist **Variant \_ true**, wodurch die-Eigenschaft aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-123">The default value is **VARIANT\_TRUE**, which enables the property.</span></span> <span data-ttu-id="d7dd7-124">Wenn diese Eigenschaft in einer sicheren Skript Umgebung auf **Variant \_ false** festgelegt wird, wird **E \_ Fail** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-124">Setting this property to **VARIANT\_FALSE** in a safe scripting environment returns **E\_FAIL**.</span></span>

<span data-ttu-id="d7dd7-125">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7dd7-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7dd7-126">Syntax</span></span>


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="d7dd7-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d7dd7-127">Property value</span></span>

<span data-ttu-id="d7dd7-128">Legen Sie diesen Parameter auf **Variant \_ false** fest, um das Feature zu deaktivieren, oder **Variant \_ true** , um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="d7dd7-129">Der Standardwert ist **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-129">The default value is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7dd7-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d7dd7-130">Error codes</span></span>

<span data-ttu-id="d7dd7-131">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7dd7-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7dd7-132">Remarks</span></span>

<span data-ttu-id="d7dd7-133">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d7dd7-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7dd7-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7dd7-134">Requirements</span></span>



| <span data-ttu-id="d7dd7-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7dd7-135">Requirement</span></span> | <span data-ttu-id="d7dd7-136">Wert</span><span class="sxs-lookup"><span data-stu-id="d7dd7-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7dd7-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d7dd7-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7dd7-138">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d7dd7-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7dd7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d7dd7-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7dd7-140">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d7dd7-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d7dd7-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7dd7-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd7-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d7dd7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d7dd7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7dd7-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd7-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d7dd7-145">IID</span><span class="sxs-lookup"><span data-stu-id="d7dd7-145">IID</span></span><br/>                      | <span data-ttu-id="d7dd7-146">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="d7dd7-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7dd7-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7dd7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7dd7-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d7dd7-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d7dd7-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d7dd7-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d7dd7-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d7dd7-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d7dd7-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d7dd7-155">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="d7dd7-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





