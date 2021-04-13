---
title: Imsrdpclientadvancedsettings-bitmapcachesize (Eigenschaft)
description: Die Größe (in Kilobyte) der Bitmap-Cachedatei, die für 8-Bit-pro-Pixel-Bitmaps verwendet wird.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- Bitmapcachesize-Eigenschaft Remotedesktopdienste
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, bitmapcachesize-Eigenschaft
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, bitmapcachesize (Eigenschaft)
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, bitmapcachesize (Eigenschaft)
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, bitmapcachesize (Eigenschaft)
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, bitmapcachesize (Eigenschaft)
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, bitmapcachesize (Eigenschaft)
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, bitmapcachesize (Eigenschaft)
- Bitmapcachesize-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, bitmapcachesize (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391745"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a><span data-ttu-id="eafea-120">Imsrdpclientadvancedsettings:: bitmapcachesize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eafea-120">IMsRdpClientAdvancedSettings::BitmapCacheSize property</span></span>

<span data-ttu-id="eafea-121">Die Größe (in Kilobyte) der Bitmap-Cachedatei, die für 8-Bit-pro-Pixel-Bitmaps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eafea-121">The size, in kilobytes, of the bitmap cache file used for 8-bits-per-pixel bitmaps.</span></span>

<span data-ttu-id="eafea-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="eafea-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="eafea-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="eafea-123">Syntax</span></span>


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="eafea-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="eafea-124">Property value</span></span>

<span data-ttu-id="eafea-125">Die neue Cache Größe in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="eafea-125">The new cache size, in kilobytes.</span></span> <span data-ttu-id="eafea-126">Die gültigen numerischen Werte lauten zwischen 1 und 32.</span><span class="sxs-lookup"><span data-stu-id="eafea-126">The valid numeric values are 1 to 32 inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eafea-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="eafea-127">Error codes</span></span>

<span data-ttu-id="eafea-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="eafea-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="eafea-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eafea-129">Remarks</span></span>

<span data-ttu-id="eafea-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="eafea-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eafea-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eafea-131">Requirements</span></span>



| <span data-ttu-id="eafea-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eafea-132">Requirement</span></span> | <span data-ttu-id="eafea-133">Wert</span><span class="sxs-lookup"><span data-stu-id="eafea-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eafea-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eafea-134">Minimum supported client</span></span><br/> | <span data-ttu-id="eafea-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eafea-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="eafea-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eafea-136">Minimum supported server</span></span><br/> | <span data-ttu-id="eafea-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eafea-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="eafea-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eafea-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="eafea-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eafea-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eafea-140">DLL</span><span class="sxs-lookup"><span data-stu-id="eafea-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eafea-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eafea-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="eafea-142">IID</span><span class="sxs-lookup"><span data-stu-id="eafea-142">IID</span></span><br/>                      | <span data-ttu-id="eafea-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="eafea-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eafea-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eafea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eafea-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="eafea-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="eafea-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="eafea-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="eafea-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="eafea-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="eafea-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="eafea-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="eafea-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="eafea-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="eafea-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="eafea-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="eafea-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="eafea-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="eafea-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="eafea-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





