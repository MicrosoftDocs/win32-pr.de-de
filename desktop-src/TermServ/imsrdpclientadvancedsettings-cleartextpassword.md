---
title: Imsrdpclientadvancedsettings cleartextpassword (Eigenschaft)
description: Gibt das Kennwort für die Verbindung an. Weitere Informationen finden Sie unter der imstscnonscriptable-Schnittstelle.
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- Cleartextpassword-Eigenschaft Remotedesktopdienste
- Cleartextpassword-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476461"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a><span data-ttu-id="fa5e7-121">Imsrdpclientadvancedsettings:: cleartextpassword (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fa5e7-121">IMsRdpClientAdvancedSettings::ClearTextPassword property</span></span>

<span data-ttu-id="fa5e7-122">Gibt das Kennwort für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="fa5e7-122">Specifies the password with which to connect.</span></span> <span data-ttu-id="fa5e7-123">Weitere Informationen finden Sie unter der [**imstscnonscriptable**](imstscnonscriptable-interface.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fa5e7-123">For more information, see the [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) interface.</span></span>

> [!Caution]  
> <span data-ttu-id="fa5e7-124">Obwohl der Skript fähige-Zugriff auf nur-Text-Kenn Wörter über diese Eigenschaft verfügbar ist, liegt es immer noch in der Verantwortung des Entwicklers, bei der Übergabe von Kenn Wörtern in Ihren Anwendungen alle Vorsicht walten zu lassen und die Sicherheit aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="fa5e7-124">Even though scriptable access to plaintext passwords is available through this property, it is still the responsibility of the developer to exercise every caution and maintain security when passing passwords in their applications.</span></span>

 

<span data-ttu-id="fa5e7-125">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="fa5e7-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5e7-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa5e7-126">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a><span data-ttu-id="fa5e7-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fa5e7-127">Property value</span></span>

<span data-ttu-id="fa5e7-128">Das neue Kennwort.</span><span class="sxs-lookup"><span data-stu-id="fa5e7-128">The new password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa5e7-129">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="fa5e7-129">Error codes</span></span>

<span data-ttu-id="fa5e7-130">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fa5e7-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa5e7-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa5e7-131">Remarks</span></span>

<span data-ttu-id="fa5e7-132">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fa5e7-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5e7-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa5e7-133">Requirements</span></span>



| <span data-ttu-id="fa5e7-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa5e7-134">Requirement</span></span> | <span data-ttu-id="fa5e7-135">Wert</span><span class="sxs-lookup"><span data-stu-id="fa5e7-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5e7-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa5e7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fa5e7-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa5e7-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fa5e7-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa5e7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fa5e7-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa5e7-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fa5e7-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fa5e7-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa5e7-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa5e7-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fa5e7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fa5e7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa5e7-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa5e7-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fa5e7-144">IID</span><span class="sxs-lookup"><span data-stu-id="fa5e7-144">IID</span></span><br/>                      | <span data-ttu-id="fa5e7-145">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="fa5e7-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa5e7-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa5e7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5e7-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fa5e7-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fa5e7-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fa5e7-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fa5e7-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fa5e7-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fa5e7-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fa5e7-154">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="fa5e7-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





