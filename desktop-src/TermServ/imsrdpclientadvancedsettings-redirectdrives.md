---
title: Imsrdpclientadvancedsettings redirectdrives (Eigenschaft)
description: Gibt an, ob die Umleitung von Festplatten Laufwerken zulässig ist.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- Redirectdrives-Eigenschaft Remotedesktopdienste
- Redirectdrives-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, redirectdrives (Eigenschaft)
- Redirectdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, Eigenschaft redirectdrives
- Redirectdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, Eigenschaft redirectdrives
- Redirectdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, Eigenschaft redirectdrives
- Redirectdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, Eigenschaft redirectdrives
- Redirectdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, Eigenschaft redirectdrives
- Redirectdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, Eigenschaft redirectdrives
- Redirectdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, Eigenschaft redirectdrives
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743656"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a><span data-ttu-id="5f619-120">Imsrdpclientadvancedsettings:: redirectdrives (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5f619-120">IMsRdpClientAdvancedSettings::RedirectDrives property</span></span>

<span data-ttu-id="5f619-121">Gibt an, ob die Umleitung von Festplatten Laufwerken zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5f619-121">Specifies if redirection of disk drives is allowed.</span></span>

<span data-ttu-id="5f619-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5f619-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f619-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f619-123">Syntax</span></span>


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a><span data-ttu-id="5f619-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5f619-124">Property value</span></span>

<span data-ttu-id="5f619-125">Legen Sie diesen Parameter auf **Variant \_ true** fest, um eine Umleitung zuzulassen, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="5f619-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="5f619-126">**Variant \_ TRUE** fordert den Benutzer auf, die Umleitung zur Verbindungszeit zu bestätigen, aus Sicherheitsgründen.</span><span class="sxs-lookup"><span data-stu-id="5f619-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f619-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5f619-127">Error codes</span></span>

<span data-ttu-id="5f619-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5f619-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f619-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f619-129">Remarks</span></span>

<span data-ttu-id="5f619-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5f619-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f619-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f619-131">Requirements</span></span>



| <span data-ttu-id="5f619-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f619-132">Requirement</span></span> | <span data-ttu-id="5f619-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5f619-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f619-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f619-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5f619-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f619-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="5f619-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f619-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5f619-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f619-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="5f619-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5f619-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f619-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f619-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5f619-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5f619-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f619-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f619-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5f619-142">IID</span><span class="sxs-lookup"><span data-stu-id="5f619-142">IID</span></span><br/>                      | <span data-ttu-id="5f619-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="5f619-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f619-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f619-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f619-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5f619-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5f619-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5f619-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5f619-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5f619-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5f619-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5f619-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5f619-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5f619-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5f619-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5f619-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5f619-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5f619-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5f619-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="5f619-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





