---
title: Imstscadvancedsettings-bitmapperistenz (Eigenschaft)
description: Gibt an, ob bitmapcaching aktiviert ist.
ms.assetid: 8cabeae8-26bc-4d33-82cc-47bb201d79b6
ms.tgt_platform: multiple
keywords:
- Bitmapperistenz-Eigenschaft Remotedesktopdienste
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, bitmapperistenz-Eigenschaft
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, bitmapperistenz-Eigenschaft
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, bitmapperistenz (Eigenschaft)
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, bitmapperistenz (Eigenschaft)
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, bitmapperistenz (Eigenschaft)
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, bitmapperistenz (Eigenschaft)
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, bitmapperistenz (Eigenschaft)
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, bitmapperistenz (Eigenschaft)
- Bitmapperistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, bitmapperistenz (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.BitmapPeristence
- IMsTscAdvancedSettings.get_BitmapPeristence
- IMsTscAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings.BitmapPeristence
- IMsRdpClientAdvancedSettings.get_BitmapPeristence
- IMsRdpClientAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings2.BitmapPeristence
- IMsRdpClientAdvancedSettings2.get_BitmapPeristence
- IMsRdpClientAdvancedSettings2.put_BitmapPeristence
- IMsRdpClientAdvancedSettings3.BitmapPeristence
- IMsRdpClientAdvancedSettings3.get_BitmapPeristence
- IMsRdpClientAdvancedSettings3.put_BitmapPeristence
- IMsRdpClientAdvancedSettings4.BitmapPeristence
- IMsRdpClientAdvancedSettings4.get_BitmapPeristence
- IMsRdpClientAdvancedSettings4.put_BitmapPeristence
- IMsRdpClientAdvancedSettings5.BitmapPeristence
- IMsRdpClientAdvancedSettings5.get_BitmapPeristence
- IMsRdpClientAdvancedSettings5.put_BitmapPeristence
- IMsRdpClientAdvancedSettings6.BitmapPeristence
- IMsRdpClientAdvancedSettings6.get_BitmapPeristence
- IMsRdpClientAdvancedSettings6.put_BitmapPeristence
- IMsRdpClientAdvancedSettings7.BitmapPeristence
- IMsRdpClientAdvancedSettings7.get_BitmapPeristence
- IMsRdpClientAdvancedSettings7.put_BitmapPeristence
- IMsRdpClientAdvancedSettings8.BitmapPeristence
- IMsRdpClientAdvancedSettings8.get_BitmapPeristence
- IMsRdpClientAdvancedSettings8.put_BitmapPeristence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a543d24b200d8fa484939d5ffeabfeeac0b5f73f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479032"
---
# <a name="imstscadvancedsettingsbitmapperistence-property"></a><span data-ttu-id="2c035-122">Imstscadvancedsettings:: bitmapperistenz-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2c035-122">IMsTscAdvancedSettings::BitmapPeristence property</span></span>

<span data-ttu-id="2c035-123">Gibt an, ob bitmapcaching aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2c035-123">Specifies whether bitmap caching is enabled.</span></span> <span data-ttu-id="2c035-124">Persistentes zwischenspeichern kann die Leistung verbessern, erfordert jedoch zusätzlichen Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="2c035-124">Persistent caching can improve performance but requires additional disk space.</span></span>

> [!Note]  
> <span data-ttu-id="2c035-125">Der Rechtschreibfehler im Namen der Eigenschaft und dessen Parameter ist in der veröffentlichten Version des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="2c035-125">The spelling error in the name of the property and its parameter is in the released version of the control.</span></span>

 

<span data-ttu-id="2c035-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2c035-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c035-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c035-127">Syntax</span></span>


```C++
HRESULT put_BitmapPeristence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPeristence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="2c035-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2c035-128">Property value</span></span>

<span data-ttu-id="2c035-129">Legen Sie diesen Parameter auf 0 fest, um das Zwischenspeichern zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="2c035-129">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c035-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2c035-130">Error codes</span></span>

<span data-ttu-id="2c035-131">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2c035-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c035-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c035-132">Remarks</span></span>

<span data-ttu-id="2c035-133">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2c035-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c035-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c035-134">Requirements</span></span>



| <span data-ttu-id="2c035-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c035-135">Requirement</span></span> | <span data-ttu-id="2c035-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2c035-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c035-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c035-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2c035-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c035-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="2c035-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c035-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2c035-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c035-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2c035-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2c035-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c035-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c035-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="2c035-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2c035-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c035-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c035-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="2c035-145">IID</span><span class="sxs-lookup"><span data-stu-id="2c035-145">IID</span></span><br/>                      | <span data-ttu-id="2c035-146">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="2c035-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c035-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c035-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c035-148">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="2c035-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2c035-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2c035-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2c035-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2c035-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="2c035-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2c035-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2c035-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2c035-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2c035-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2c035-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2c035-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2c035-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2c035-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2c035-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2c035-156">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="2c035-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





