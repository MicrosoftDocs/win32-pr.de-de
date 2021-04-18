---
title: Imstscadvancedsettings disablerdpdr (Eigenschaft)
description: Gibt an, ob die Umleitung von Drucker und Zwischenablage aktiviert ist.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- Disablerdpdr-Eigenschaft Remotedesktopdienste
- Disablerdpdr-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, disablerdpdr (Eigenschaft)
- Disablerdpdr-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, disablerdpdr-Eigenschaft
- Disablerdpdr-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, disablerdpdr (Eigenschaft)
- Disablerdpdr-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, disablerdpdr (Eigenschaft)
- Disablerdpdr-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, disablerdpdr (Eigenschaft)
- Disablerdpdr-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, disablerdpdr (Eigenschaft)
- Disablerdpdr-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, disablerdpdr (Eigenschaft)
- Disablerdpdr-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, disablerdpdr (Eigenschaft)
- Disablerdpdr-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, disablerdpdr (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338768"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a><span data-ttu-id="5b442-122">Imstscadvancedsettings::D der Eigenschaft "isablerdpdr"</span><span class="sxs-lookup"><span data-stu-id="5b442-122">IMsTscAdvancedSettings::DisableRdpdr property</span></span>

<span data-ttu-id="5b442-123">Gibt an, ob die Umleitung von Drucker und Zwischenablage aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5b442-123">Specifies whether printer and clipboard redirection is enabled.</span></span>

<span data-ttu-id="5b442-124">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5b442-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b442-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b442-125">Syntax</span></span>


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a><span data-ttu-id="5b442-126">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5b442-126">Property value</span></span>

<span data-ttu-id="5b442-127">Legen Sie diesen Parameter auf " **true** " fest, um die **Umleitung zu deaktivieren** .</span><span class="sxs-lookup"><span data-stu-id="5b442-127">Set this parameter to **TRUE** to disable redirection or **FALSE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5b442-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5b442-128">Error codes</span></span>

<span data-ttu-id="5b442-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5b442-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b442-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b442-130">Remarks</span></span>

<span data-ttu-id="5b442-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5b442-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b442-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b442-132">Requirements</span></span>



| <span data-ttu-id="5b442-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b442-133">Requirement</span></span> | <span data-ttu-id="5b442-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5b442-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b442-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b442-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5b442-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b442-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="5b442-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b442-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5b442-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b442-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5b442-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5b442-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b442-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b442-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="5b442-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b442-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b442-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b442-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="5b442-143">IID</span><span class="sxs-lookup"><span data-stu-id="5b442-143">IID</span></span><br/>                      | <span data-ttu-id="5b442-144">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="5b442-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b442-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b442-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b442-146">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="5b442-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5b442-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5b442-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5b442-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5b442-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="5b442-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5b442-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5b442-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5b442-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5b442-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5b442-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5b442-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5b442-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5b442-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5b442-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5b442-154">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="5b442-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





