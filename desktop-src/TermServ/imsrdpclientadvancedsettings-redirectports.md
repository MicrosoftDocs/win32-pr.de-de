---
title: Imsrdpclientadvancedsettings redirectports (Eigenschaft)
description: Gibt an, ob die Umleitung lokaler Ports (z. b. com und LPT) zulässig ist.
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- Redirectports-Eigenschaft Remotedesktopdienste
- Redirectports-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, redirectports (Eigenschaft)
- Redirectports-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, redirectports (Eigenschaft)
- Redirectports-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, redirectports (Eigenschaft)
- Redirectports-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, redirectports (Eigenschaft)
- Redirectports-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, redirectports (Eigenschaft)
- Redirectports-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, redirectports (Eigenschaft)
- Redirectports-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, redirectports (Eigenschaft)
- Redirectports-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, redirectports (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 714b26081bb4caadface283553b1dd3ebd91192d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949433"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a><span data-ttu-id="f9262-120">Imsrdpclientadvancedsettings:: redirectports (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f9262-120">IMsRdpClientAdvancedSettings::RedirectPorts property</span></span>

<span data-ttu-id="f9262-121">Gibt an, ob die Umleitung lokaler Ports (z. b. com und LPT) zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f9262-121">Specifies if redirection of local ports (for example, COM and LPT) is allowed.</span></span>

<span data-ttu-id="f9262-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f9262-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9262-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9262-123">Syntax</span></span>


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a><span data-ttu-id="f9262-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f9262-124">Property value</span></span>

<span data-ttu-id="f9262-125">Legen Sie diesen Parameter auf **Variant \_ true** fest, um eine Umleitung zuzulassen, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="f9262-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="f9262-126">**Variant \_ TRUE** fordert den Benutzer auf, die Umleitung zur Verbindungszeit zu bestätigen, aus Sicherheitsgründen.</span><span class="sxs-lookup"><span data-stu-id="f9262-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9262-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f9262-127">Error codes</span></span>

<span data-ttu-id="f9262-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f9262-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9262-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9262-129">Remarks</span></span>

<span data-ttu-id="f9262-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f9262-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9262-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9262-131">Requirements</span></span>



| <span data-ttu-id="f9262-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9262-132">Requirement</span></span> | <span data-ttu-id="f9262-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f9262-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9262-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9262-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f9262-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9262-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f9262-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9262-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f9262-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9262-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f9262-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f9262-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9262-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9262-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f9262-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f9262-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9262-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9262-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f9262-142">IID</span><span class="sxs-lookup"><span data-stu-id="f9262-142">IID</span></span><br/>                      | <span data-ttu-id="f9262-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="f9262-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9262-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9262-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9262-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f9262-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f9262-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f9262-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f9262-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f9262-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f9262-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f9262-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f9262-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f9262-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f9262-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f9262-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f9262-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f9262-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f9262-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="f9262-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





