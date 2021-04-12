---
title: Imsrdpclientadvancedsettings shadobitmap (Eigenschaft)
description: Gibt an, ob Schatten Bitmaps verwendet werden sollen.
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- Shadowbitmap-Eigenschaft Remotedesktopdienste
- Shadowbitmap-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
- Shadowbitmap-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
- Shadowbitmap-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
- Shadowbitmap-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
- Shadowbitmap-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
- Shadowbitmap-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
- Shadowbitmap-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
- Shadowbitmap-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, shadowbitmap-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6c43862b498fe5828d2746666c5e414de4c71e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475231"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a><span data-ttu-id="b3951-120">Imsrdpclientadvancedsettings:: shadowbitmap-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b3951-120">IMsRdpClientAdvancedSettings::ShadowBitmap property</span></span>

<span data-ttu-id="b3951-121">\[Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b3951-121">\[This property is not supported.</span></span> <span data-ttu-id="b3951-122">Ab Windows Server 2008 und Windows 7 geben Aufrufe von **shadowbitmap** immer **\_ false** zurück.\]</span><span class="sxs-lookup"><span data-stu-id="b3951-122">Starting with Windows Server 2008 and Windows 7, calls to **ShadowBitmap** always return **S\_FALSE**.\]</span></span>

<span data-ttu-id="b3951-123">Gibt an, ob Schatten Bitmaps verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b3951-123">Specifies if shadow bitmaps should be used.</span></span>

<span data-ttu-id="b3951-124">Schatten Bitmaps sind immer im Vollbildmodus deaktiviert. Daher hat diese Eigenschaft im Vollbildmodus keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="b3951-124">Shadow bitmaps are always disabled in full-screen mode, therefore this property has no effect when in full-screen mode.</span></span>

<span data-ttu-id="b3951-125">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b3951-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3951-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3951-126">Syntax</span></span>


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="b3951-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b3951-127">Property value</span></span>

<span data-ttu-id="b3951-128">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b3951-128">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="b3951-129">Das Deaktivieren dieses Features verbessert in der Regel die Leistung, kann jedoch beim Zeichnen von Bildschirmen zu Artefakten führen.</span><span class="sxs-lookup"><span data-stu-id="b3951-129">Disabling this feature typically improves performance but can result in artifacts when painting screens.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3951-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3951-130">Remarks</span></span>

<span data-ttu-id="b3951-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b3951-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3951-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3951-132">Requirements</span></span>



| <span data-ttu-id="b3951-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3951-133">Requirement</span></span> | <span data-ttu-id="b3951-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b3951-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3951-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3951-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b3951-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3951-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="b3951-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3951-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b3951-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3951-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b3951-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b3951-139">End of client support</span></span><br/>    | <span data-ttu-id="b3951-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3951-140">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="b3951-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b3951-141">End of server support</span></span><br/>    | <span data-ttu-id="b3951-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3951-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b3951-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b3951-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3951-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3951-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b3951-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b3951-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3951-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3951-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b3951-147">IID</span><span class="sxs-lookup"><span data-stu-id="b3951-147">IID</span></span><br/>                      | <span data-ttu-id="b3951-148">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="b3951-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3951-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3951-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3951-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b3951-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b3951-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b3951-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b3951-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b3951-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b3951-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b3951-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b3951-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b3951-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b3951-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b3951-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b3951-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b3951-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b3951-157">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="b3951-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





