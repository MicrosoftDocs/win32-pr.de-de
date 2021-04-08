---
title: Imsrdpclientadvancedsettings-hotkeyfullscreen-Eigenschaft
description: Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um den Hotkey-Ersatz für den Wechsel in den Vollbildmodus zu bestimmen.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
- Hotkeyfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, hotkeyfullscreen-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949503"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a><span data-ttu-id="d48e6-120">Imsrdpclientadvancedsettings:: hotkeyfullscreen-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d48e6-120">IMsRdpClientAdvancedSettings::HotKeyFullScreen property</span></span>

<span data-ttu-id="d48e6-121">Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um den Hotkey-Ersatz für den Wechsel in den Vollbildmodus zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d48e6-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for switching to full-screen mode.</span></span>

<span data-ttu-id="d48e6-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d48e6-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48e6-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d48e6-123">Syntax</span></span>


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="d48e6-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d48e6-124">Property value</span></span>

<span data-ttu-id="d48e6-125">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="d48e6-125">The new virtual-key code.</span></span> <span data-ttu-id="d48e6-126">**VK \_** Der Standardwert ist "Abbrechen".</span><span class="sxs-lookup"><span data-stu-id="d48e6-126">**VK\_CANCEL** is the default value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d48e6-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d48e6-127">Error codes</span></span>

<span data-ttu-id="d48e6-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d48e6-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d48e6-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d48e6-129">Remarks</span></span>

<span data-ttu-id="d48e6-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d48e6-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d48e6-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d48e6-131">Requirements</span></span>



| <span data-ttu-id="d48e6-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d48e6-132">Requirement</span></span> | <span data-ttu-id="d48e6-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d48e6-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d48e6-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d48e6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d48e6-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d48e6-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d48e6-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d48e6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d48e6-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d48e6-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d48e6-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d48e6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="d48e6-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48e6-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d48e6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d48e6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d48e6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d48e6-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d48e6-142">IID</span><span class="sxs-lookup"><span data-stu-id="d48e6-142">IID</span></span><br/>                      | <span data-ttu-id="d48e6-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="d48e6-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d48e6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d48e6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48e6-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d48e6-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d48e6-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d48e6-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d48e6-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d48e6-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d48e6-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d48e6-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d48e6-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d48e6-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d48e6-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d48e6-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d48e6-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d48e6-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d48e6-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="d48e6-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





