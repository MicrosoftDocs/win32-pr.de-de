---
title: Imsrdpclientadvancedsettings redirectprinter (Eigenschaft)
description: Gibt an, ob die Umleitung von Druckern zulässig ist.
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- Redirectprinters-Eigenschaft Remotedesktopdienste
- Redirectprinters-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, redirectprinter-Eigenschaft
- Redirectprinters-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, Eigenschaft redirectprinter
- Redirectprinters-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, Eigenschaft redirectprinter
- Redirectprinters-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, Eigenschaft redirectprinter
- Redirectprinters-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, Eigenschaft redirectprinter
- Redirectprinters-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, Eigenschaft redirectprinter
- Redirectprinters-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, Eigenschaft redirectprinter
- Redirectprinters-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, Eigenschaft redirectprinter
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fecc3b6f72b8706168c75d220d78fc49340752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740024"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a><span data-ttu-id="b7e53-120">Imsrdpclientadvancedsettings:: redirectprinters-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7e53-120">IMsRdpClientAdvancedSettings::RedirectPrinters property</span></span>

<span data-ttu-id="b7e53-121">Gibt an, ob die Umleitung von Druckern zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="b7e53-121">Specifies if redirection of printers is allowed.</span></span>

<span data-ttu-id="b7e53-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b7e53-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e53-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7e53-123">Syntax</span></span>


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a><span data-ttu-id="b7e53-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b7e53-124">Property value</span></span>

<span data-ttu-id="b7e53-125">Legen Sie diesen Parameter auf **Variant \_ true** fest, um eine Umleitung zuzulassen, andernfalls **\_ false** .</span><span class="sxs-lookup"><span data-stu-id="b7e53-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7e53-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b7e53-126">Error codes</span></span>

<span data-ttu-id="b7e53-127">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b7e53-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e53-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7e53-128">Remarks</span></span>

<span data-ttu-id="b7e53-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b7e53-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e53-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7e53-130">Requirements</span></span>



| <span data-ttu-id="b7e53-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7e53-131">Requirement</span></span> | <span data-ttu-id="b7e53-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b7e53-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e53-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7e53-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e53-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7e53-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="b7e53-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7e53-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e53-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7e53-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="b7e53-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b7e53-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7e53-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e53-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b7e53-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e53-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e53-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7e53-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b7e53-141">IID</span><span class="sxs-lookup"><span data-stu-id="b7e53-141">IID</span></span><br/>                      | <span data-ttu-id="b7e53-142">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="b7e53-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7e53-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7e53-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7e53-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b7e53-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b7e53-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b7e53-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b7e53-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b7e53-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b7e53-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b7e53-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b7e53-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b7e53-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b7e53-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b7e53-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b7e53-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b7e53-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b7e53-151">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="b7e53-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





