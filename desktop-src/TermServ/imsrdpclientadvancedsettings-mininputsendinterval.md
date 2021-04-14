---
title: Imsrdpclientadvancedsettings mininputsendinterval (Eigenschaft)
description: Gibt das minimale Intervall (in Millisekunden) zwischen dem Senden von Mausereignissen an.
ms.assetid: d186c05f-0b45-47bd-8a8e-e1f9baf2bd75
ms.tgt_platform: multiple
keywords:
- mininputsendinterval-Eigenschaft Remotedesktopdienste
- mininputsendinterval-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
- mininputsendinterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
- mininputsendinterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
- mininputsendinterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
- mininputsendinterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
- mininputsendinterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
- mininputsendinterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
- mininputsendinterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, mininputsendinterval-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.minInputSendInterval
- IMsRdpClientAdvancedSettings.get_minInputSendInterval
- IMsRdpClientAdvancedSettings.put_minInputSendInterval
- IMsRdpClientAdvancedSettings2.minInputSendInterval
- IMsRdpClientAdvancedSettings2.get_minInputSendInterval
- IMsRdpClientAdvancedSettings2.put_minInputSendInterval
- IMsRdpClientAdvancedSettings3.minInputSendInterval
- IMsRdpClientAdvancedSettings3.get_minInputSendInterval
- IMsRdpClientAdvancedSettings3.put_minInputSendInterval
- IMsRdpClientAdvancedSettings4.minInputSendInterval
- IMsRdpClientAdvancedSettings4.get_minInputSendInterval
- IMsRdpClientAdvancedSettings4.put_minInputSendInterval
- IMsRdpClientAdvancedSettings5.minInputSendInterval
- IMsRdpClientAdvancedSettings5.get_minInputSendInterval
- IMsRdpClientAdvancedSettings5.put_minInputSendInterval
- IMsRdpClientAdvancedSettings6.minInputSendInterval
- IMsRdpClientAdvancedSettings6.get_minInputSendInterval
- IMsRdpClientAdvancedSettings6.put_minInputSendInterval
- IMsRdpClientAdvancedSettings7.minInputSendInterval
- IMsRdpClientAdvancedSettings7.get_minInputSendInterval
- IMsRdpClientAdvancedSettings7.put_minInputSendInterval
- IMsRdpClientAdvancedSettings8.minInputSendInterval
- IMsRdpClientAdvancedSettings8.get_minInputSendInterval
- IMsRdpClientAdvancedSettings8.put_minInputSendInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56070e2ba395c4b89dc9caa9e6e5181bb03d81ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391736"
---
# <a name="imsrdpclientadvancedsettingsmininputsendinterval-property"></a><span data-ttu-id="fb675-120">Imsrdpclientadvancedsettings:: mininputsendinterval-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fb675-120">IMsRdpClientAdvancedSettings::minInputSendInterval property</span></span>

<span data-ttu-id="fb675-121">Gibt das minimale Intervall (in Millisekunden) zwischen dem Senden von Mausereignissen an.</span><span class="sxs-lookup"><span data-stu-id="fb675-121">Specifies the minimum interval, in milliseconds, between the sending of mouse events.</span></span>

<span data-ttu-id="fb675-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="fb675-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb675-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb675-123">Syntax</span></span>


```C++
HRESULT put_minInputSendInterval(
  [in]  LONG minInputSendInterval
);

HRESULT get_minInputSendInterval(
  [out] LONG *pminInputSendInterval
);
```



## <a name="property-value"></a><span data-ttu-id="fb675-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fb675-124">Property value</span></span>

<span data-ttu-id="fb675-125">Das neue Intervall in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="fb675-125">The new interval, in milliseconds.</span></span> <span data-ttu-id="fb675-126">Der Standardwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="fb675-126">The default value is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb675-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fb675-127">Error codes</span></span>

<span data-ttu-id="fb675-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fb675-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb675-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb675-129">Remarks</span></span>

<span data-ttu-id="fb675-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fb675-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb675-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb675-131">Requirements</span></span>



| <span data-ttu-id="fb675-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb675-132">Requirement</span></span> | <span data-ttu-id="fb675-133">Wert</span><span class="sxs-lookup"><span data-stu-id="fb675-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb675-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb675-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fb675-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb675-135">Windows 7</span></span><br/>                                                                            |
| <span data-ttu-id="fb675-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb675-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fb675-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb675-137">Windows Server 2008 R2</span></span><br/>                                                               |
| <span data-ttu-id="fb675-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fb675-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb675-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb675-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fb675-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fb675-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb675-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb675-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fb675-142">IID</span><span class="sxs-lookup"><span data-stu-id="fb675-142">IID</span></span><br/>                      | <span data-ttu-id="fb675-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="fb675-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb675-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb675-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb675-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fb675-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fb675-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fb675-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fb675-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fb675-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fb675-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fb675-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fb675-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fb675-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fb675-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fb675-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fb675-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fb675-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fb675-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="fb675-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





