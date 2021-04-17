---
title: Imsrdpclientadvancedsettings-hotkeyalttab (Eigenschaft)
description: Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Tab zu bestimmen.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Hotkeyalttab-Eigenschaft Remotedesktopdienste
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyalttab-Eigenschaft
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, hotkeyalttab-Eigenschaft
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, hotkeyalttab-Eigenschaft
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, hotkeyalttab-Eigenschaft
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, hotkeyalttab-Eigenschaft
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyalttab-Eigenschaft
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyalttab-Eigenschaft
- Hotkeyalttab-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyalttab-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391739"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a><span data-ttu-id="88cb8-120">Imsrdpclientadvancedsettings:: hotkeyalttab-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="88cb8-120">IMsRdpClientAdvancedSettings::HotKeyAltTab property</span></span>

<span data-ttu-id="88cb8-121">Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Tab zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="88cb8-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+TAB.</span></span>

<span data-ttu-id="88cb8-122">Diese Eigenschaft ist nur gültig, wenn die [**keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="88cb8-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="88cb8-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="88cb8-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="88cb8-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="88cb8-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a><span data-ttu-id="88cb8-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="88cb8-125">Property value</span></span>

<span data-ttu-id="88cb8-126">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="88cb8-126">The new virtual-key code.</span></span> <span data-ttu-id="88cb8-127">**VK \_ "Prior** " ist der Standardwert, wobei Alt + Bild-auf als resultierende Sequenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="88cb8-127">**VK\_PRIOR** is the default value, with ALT+PAGE UP as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88cb8-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="88cb8-128">Error codes</span></span>

<span data-ttu-id="88cb8-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="88cb8-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="88cb8-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88cb8-130">Remarks</span></span>

<span data-ttu-id="88cb8-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="88cb8-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88cb8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88cb8-132">Requirements</span></span>



| <span data-ttu-id="88cb8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88cb8-133">Requirement</span></span> | <span data-ttu-id="88cb8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="88cb8-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88cb8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88cb8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="88cb8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88cb8-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="88cb8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88cb8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="88cb8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88cb8-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="88cb8-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="88cb8-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="88cb8-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88cb8-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="88cb8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="88cb8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88cb8-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88cb8-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="88cb8-143">IID</span><span class="sxs-lookup"><span data-stu-id="88cb8-143">IID</span></span><br/>                      | <span data-ttu-id="88cb8-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="88cb8-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88cb8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88cb8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cb8-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="88cb8-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="88cb8-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="88cb8-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="88cb8-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="88cb8-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="88cb8-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="88cb8-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="88cb8-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="88cb8-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="88cb8-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="88cb8-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="88cb8-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="88cb8-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="88cb8-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="88cb8-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





