---
title: Imstscadvancedsettings allowbackgroundinput (Eigenschaft)
description: Gibt an, ob der Hintergrund Eingabemodus aktiviert ist.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- allowbackgroundinput-Eigenschaft Remotedesktopdienste
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, allowbackgroundinput-Eigenschaft
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, allowbackgroundinput-Eigenschaft
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, allowbackgroundinput (Eigenschaft)
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, allowbackgroundinput (Eigenschaft)
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, allowbackgroundinput (Eigenschaft)
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, allowbackgroundinput (Eigenschaft)
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, allowbackgroundinput (Eigenschaft)
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, allowbackgroundinput (Eigenschaft)
- allowbackgroundinput-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, allowbackgroundinput (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392206"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a><span data-ttu-id="7ac0f-122">Imstscadvancedsettings:: allowbackgroundinput-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7ac0f-122">IMsTscAdvancedSettings::allowBackgroundInput property</span></span>

<span data-ttu-id="7ac0f-123">Gibt an, ob der Hintergrund Eingabemodus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7ac0f-123">Specifies whether background input mode is enabled.</span></span> <span data-ttu-id="7ac0f-124">Wenn Hintergrund Eingaben aktiviert sind, kann der Client Eingaben akzeptieren, wenn der Client keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="7ac0f-124">When background input is enabled the client can accept input when the client does not have focus.</span></span>

<span data-ttu-id="7ac0f-125">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7ac0f-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac0f-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ac0f-126">Syntax</span></span>


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a><span data-ttu-id="7ac0f-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7ac0f-127">Property value</span></span>

<span data-ttu-id="7ac0f-128">Legen Sie diesen Parameter auf 0 fest, um den Hintergrund Eingabemodus zu deaktivieren, oder einen Wert ungleich NULL, um den Hintergrund Eingabemodus zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="7ac0f-128">Set this parameter to 0 to disable background input mode or a nonzero value to enable background input mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7ac0f-129">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7ac0f-129">Error codes</span></span>

<span data-ttu-id="7ac0f-130">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7ac0f-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac0f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ac0f-131">Remarks</span></span>

<span data-ttu-id="7ac0f-132">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7ac0f-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac0f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ac0f-133">Requirements</span></span>



| <span data-ttu-id="7ac0f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ac0f-134">Requirement</span></span> | <span data-ttu-id="7ac0f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="7ac0f-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac0f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ac0f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7ac0f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ac0f-137">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="7ac0f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ac0f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7ac0f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ac0f-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7ac0f-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7ac0f-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="7ac0f-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ac0f-141"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7ac0f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7ac0f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ac0f-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ac0f-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7ac0f-144">IID</span><span class="sxs-lookup"><span data-stu-id="7ac0f-144">IID</span></span><br/>                      | <span data-ttu-id="7ac0f-145">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="7ac0f-145">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ac0f-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ac0f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac0f-147">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-147">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-149">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7ac0f-155">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="7ac0f-155">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





