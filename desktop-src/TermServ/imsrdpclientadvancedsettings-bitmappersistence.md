---
title: Imsrdpclientadvancedsettings-bitmappersistenz (Eigenschaft)
description: Gibt an, ob das persistente Bitmap-Caching verwendet werden soll. Persistentes zwischenspeichern kann die Leistung verbessern, erfordert jedoch zusätzlichen Speicherplatz.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- Bitmappersistenz-Eigenschaft Remotedesktopdienste
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, bitmappersistenz-Eigenschaft
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, bitmappersistenz (Eigenschaft)
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, bitmappersistenz (Eigenschaft)
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, bitmappersistenz (Eigenschaft)
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, bitmappersistenz (Eigenschaft)
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, bitmappersistenz (Eigenschaft)
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, bitmappersistenz (Eigenschaft)
- Bitmappersistenz-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, bitmappersistenz (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391744"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a><span data-ttu-id="4772f-121">Imsrdpclientadvancedsettings:: bitmappersistenz (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4772f-121">IMsRdpClientAdvancedSettings::BitmapPersistence property</span></span>

<span data-ttu-id="4772f-122">Gibt an, ob das persistente Bitmap-Caching verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4772f-122">Specifies if persistent bitmap caching should be used.</span></span> <span data-ttu-id="4772f-123">Persistentes zwischenspeichern kann die Leistung verbessern, erfordert jedoch zusätzlichen Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="4772f-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="4772f-124">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4772f-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4772f-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="4772f-125">Syntax</span></span>


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="4772f-126">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4772f-126">Property value</span></span>

<span data-ttu-id="4772f-127">Legen Sie diesen Parameter auf 0 fest, um das Zwischenspeichern zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="4772f-127">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

> [!Note]  
> <span data-ttu-id="4772f-128">Der Rechtschreibfehler im Namen des-Parameters ist in der veröffentlichten Version des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="4772f-128">The spelling error in the name of the parameter is in the released version of the control.</span></span>

 

## <a name="error-codes"></a><span data-ttu-id="4772f-129">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4772f-129">Error codes</span></span>

<span data-ttu-id="4772f-130">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4772f-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4772f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4772f-131">Remarks</span></span>

<span data-ttu-id="4772f-132">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4772f-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4772f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4772f-133">Requirements</span></span>



| <span data-ttu-id="4772f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4772f-134">Requirement</span></span> | <span data-ttu-id="4772f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4772f-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4772f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4772f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4772f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4772f-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4772f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4772f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4772f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4772f-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4772f-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4772f-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4772f-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4772f-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4772f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4772f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4772f-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4772f-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4772f-144">IID</span><span class="sxs-lookup"><span data-stu-id="4772f-144">IID</span></span><br/>                      | <span data-ttu-id="4772f-145">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="4772f-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4772f-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4772f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4772f-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4772f-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4772f-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4772f-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4772f-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4772f-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4772f-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4772f-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4772f-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4772f-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4772f-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4772f-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4772f-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4772f-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4772f-154">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="4772f-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





