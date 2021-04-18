---
title: Imsrdpclientadvancedsettings redirectmartcards (Eigenschaft)
description: Gibt an, ob die Umleitung von Smartcards zulässig ist.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- Redirectmartcards-Eigenschaft Remotedesktopdienste
- Redirectmartcards-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, redirectmartcards-Eigenschaft
- Redirectmartcards-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, redirectmartcards (Eigenschaft)
- Redirectmartcards-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, redirectmartcards (Eigenschaft)
- Redirectmartcards-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, redirectmartcards (Eigenschaft)
- Redirectmartcards-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, redirectmartcards (Eigenschaft)
- Redirectmartcards-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, redirectmartcards (Eigenschaft)
- Redirectmartcards-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, redirectmartcards (Eigenschaft)
- Redirectmartcards-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, redirectmartcards (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba58a492ede5371c0f43d996f46ed7a898df7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338115"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a><span data-ttu-id="dc95c-120">Imsrdpclientadvancedsettings:: redirectmartcards (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dc95c-120">IMsRdpClientAdvancedSettings::RedirectSmartCards property</span></span>

<span data-ttu-id="dc95c-121">Gibt an, ob die Umleitung von Smartcards zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="dc95c-121">Specifies if redirection of smart cards is allowed.</span></span>

<span data-ttu-id="dc95c-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="dc95c-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc95c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc95c-123">Syntax</span></span>


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a><span data-ttu-id="dc95c-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dc95c-124">Property value</span></span>

<span data-ttu-id="dc95c-125">Legen Sie diesen Parameter auf **Variant \_ true** fest, um eine Umleitung zuzulassen, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="dc95c-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="dc95c-126">**Variant \_ TRUE** fordert den Benutzer auf, die Umleitung zur Verbindungszeit zu bestätigen, aus Sicherheitsgründen.</span><span class="sxs-lookup"><span data-stu-id="dc95c-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dc95c-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="dc95c-127">Error codes</span></span>

<span data-ttu-id="dc95c-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="dc95c-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc95c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc95c-129">Remarks</span></span>

<span data-ttu-id="dc95c-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="dc95c-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc95c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc95c-131">Requirements</span></span>



| <span data-ttu-id="dc95c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc95c-132">Requirement</span></span> | <span data-ttu-id="dc95c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="dc95c-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc95c-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc95c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dc95c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc95c-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="dc95c-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc95c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dc95c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc95c-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="dc95c-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="dc95c-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc95c-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc95c-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="dc95c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="dc95c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc95c-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc95c-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="dc95c-142">IID</span><span class="sxs-lookup"><span data-stu-id="dc95c-142">IID</span></span><br/>                      | <span data-ttu-id="dc95c-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="dc95c-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc95c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc95c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc95c-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="dc95c-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="dc95c-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="dc95c-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="dc95c-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="dc95c-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="dc95c-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="dc95c-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="dc95c-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="dc95c-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="dc95c-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="dc95c-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="dc95c-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="dc95c-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="dc95c-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="dc95c-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





