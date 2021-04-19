---
title: Imsrdpclientadvancedsettings BitmapVirtualCache16BppSize (Eigenschaft)
description: Gibt die Größe der persistenten Bitmap-Cachedatei in Megabyte an, die für die 15-und 16-Bit-pro-Pixel-High-Color-Einstellungen verwendet werden soll.
ms.assetid: f2558c88-d60f-4be3-9941-8e0e18bbb778
ms.tgt_platform: multiple
keywords:
- BitmapVirtualCache16BppSize-Eigenschaft Remotedesktopdienste
- BitmapVirtualCache16BppSize-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
- BitmapVirtualCache16BppSize-Eigenschaften Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, BitmapVirtualCache16BppSize-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache16BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fd0a11a1cf3b313c1f6f2c12d1a73b61c6f45a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338709"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache16bppsize-property"></a><span data-ttu-id="03e5f-120">Imsrdpclientadvancedsettings:: BitmapVirtualCache16BppSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="03e5f-120">IMsRdpClientAdvancedSettings::BitmapVirtualCache16BppSize property</span></span>

<span data-ttu-id="03e5f-121">Gibt die Größe der persistenten Bitmap-Cachedatei in Megabyte an, die für die 15-und 16-Bit-pro-Pixel-High-Color-Einstellungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="03e5f-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for the 15 and 16 bits-per-pixel high-color settings.</span></span>

<span data-ttu-id="03e5f-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="03e5f-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e5f-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="03e5f-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache16BppSize(
  [in]  LONG bitmapVirtualCache16BppSize
);

HRESULT get_BitmapVirtualCache16BppSize(
  [out] LONG *pbitmapVirtualCache16BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="03e5f-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="03e5f-124">Property value</span></span>

<span data-ttu-id="03e5f-125">Die neue Cache Größe.</span><span class="sxs-lookup"><span data-stu-id="03e5f-125">The new cache size.</span></span> <span data-ttu-id="03e5f-126">Gültige Werte sind 1 bis 32 einschließlich, der Standardwert ist 20.</span><span class="sxs-lookup"><span data-stu-id="03e5f-126">The valid values are 1 to 32 inclusive, and the default value is 20.</span></span> <span data-ttu-id="03e5f-127">Beachten Sie, dass die maximale Größe für alle virtuellen Cache Dateien 128 MB beträgt.</span><span class="sxs-lookup"><span data-stu-id="03e5f-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="03e5f-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="03e5f-128">Error codes</span></span>

<span data-ttu-id="03e5f-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="03e5f-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="03e5f-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03e5f-130">Remarks</span></span>

<span data-ttu-id="03e5f-131">Zu den zugehörigen Eigenschaften gehören die **bitmapvirtualcachesize** -Eigenschaft und die **BitmapVirtualCache24BppSize** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="03e5f-131">Related properties include the **BitmapVirtualCacheSize** and **BitmapVirtualCache24BppSize** properties.</span></span>

<span data-ttu-id="03e5f-132">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="03e5f-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03e5f-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03e5f-133">Requirements</span></span>



| <span data-ttu-id="03e5f-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03e5f-134">Requirement</span></span> | <span data-ttu-id="03e5f-135">Wert</span><span class="sxs-lookup"><span data-stu-id="03e5f-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e5f-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03e5f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="03e5f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03e5f-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="03e5f-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03e5f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="03e5f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03e5f-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="03e5f-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="03e5f-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="03e5f-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03e5f-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="03e5f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="03e5f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03e5f-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03e5f-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="03e5f-144">IID</span><span class="sxs-lookup"><span data-stu-id="03e5f-144">IID</span></span><br/>                      | <span data-ttu-id="03e5f-145">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="03e5f-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03e5f-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03e5f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03e5f-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="03e5f-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="03e5f-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="03e5f-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="03e5f-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="03e5f-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="03e5f-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="03e5f-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="03e5f-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="03e5f-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="03e5f-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="03e5f-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="03e5f-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="03e5f-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="03e5f-154">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="03e5f-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





