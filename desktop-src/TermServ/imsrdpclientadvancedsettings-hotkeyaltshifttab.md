---
title: Imsrdpclientadvancedsettings-hotkeyaltshifittab (Eigenschaft)
description: Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Umschalt + Tab zu bestimmen.
ms.assetid: da52f2fb-15cc-4d55-b26e-cf5465290889
ms.tgt_platform: multiple
keywords:
- Hotkeyaltshif ttab-Eigenschaft Remotedesktopdienste
- Hotkeyaltshif ttab-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyaltshif ttab-Eigenschaft
- Hotkeyaltshibottab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, hotkeyaltshibottab-Eigenschaft
- Hotkeyaltshibottab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, hotkeyaltshibottab-Eigenschaft
- Hotkeyaltshibottab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, hotkeyaltshibottab-Eigenschaft
- Hotkeyaltshibottab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, hotkeyaltshibottab-Eigenschaft
- Hotkeyaltshibottab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyaltshibottab-Eigenschaft
- Hotkeyaltshibottab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyaltshibottab-Eigenschaft
- Hotkeyaltshibottab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyaltshibottab-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltShiftTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9819ddcba3f9cb10450525467eb8accce958c2f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341787"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltshifttab-property"></a><span data-ttu-id="c2b22-120">Imsrdpclientadvancedsettings:: hotkeyaltshif ttab-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2b22-120">IMsRdpClientAdvancedSettings::HotKeyAltShiftTab property</span></span>

<span data-ttu-id="c2b22-121">Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Umschalt + Tab zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c2b22-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SHIFT+TAB.</span></span>

<span data-ttu-id="c2b22-122">Diese Eigenschaft ist nur gültig, wenn die [**keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c2b22-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="c2b22-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c2b22-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b22-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2b22-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltShiftTab(
  [in]  LONG hotKeyAltShiftTab
);

HRESULT get_HotKeyAltShiftTab(
  [out] LONG *photKeyAltShiftTab
);
```



## <a name="property-value"></a><span data-ttu-id="c2b22-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2b22-125">Property value</span></span>

<span data-ttu-id="c2b22-126">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c2b22-126">The new virtual-key code.</span></span> <span data-ttu-id="c2b22-127">**VK \_ Der nächste** Schritt ist der Standardwert, wobei Alt + Bild-ab als resultierende Sequenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c2b22-127">**VK\_NEXT** is the default value, with ALT+PAGE DOWN as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2b22-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c2b22-128">Error codes</span></span>

<span data-ttu-id="c2b22-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c2b22-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2b22-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2b22-130">Remarks</span></span>

<span data-ttu-id="c2b22-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c2b22-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b22-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2b22-132">Requirements</span></span>



| <span data-ttu-id="c2b22-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2b22-133">Requirement</span></span> | <span data-ttu-id="c2b22-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c2b22-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b22-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2b22-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c2b22-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2b22-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c2b22-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2b22-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c2b22-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2b22-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c2b22-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c2b22-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2b22-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b22-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c2b22-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c2b22-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2b22-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b22-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c2b22-143">IID</span><span class="sxs-lookup"><span data-stu-id="c2b22-143">IID</span></span><br/>                      | <span data-ttu-id="c2b22-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="c2b22-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2b22-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2b22-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b22-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c2b22-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c2b22-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c2b22-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c2b22-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c2b22-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c2b22-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c2b22-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c2b22-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c2b22-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c2b22-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c2b22-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c2b22-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c2b22-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c2b22-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="c2b22-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





