---
title: Imsrdpclientadvancedsettings-hotkeyctrlesc (Eigenschaft)
description: Gibt den Code des virtuellen Schlüssels an, der alt hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ESC zu bestimmen.
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyctrlesc-Eigenschaft
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
- Hotkeyctrlesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyctrlesc (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339965"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a><span data-ttu-id="19b33-120">Imsrdpclientadvancedsettings:: hotkeyctrlesc (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="19b33-120">IMsRdpClientAdvancedSettings::HotKeyCtrlEsc property</span></span>

<span data-ttu-id="19b33-121">Gibt den Code des virtuellen Schlüssels an, der alt hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ESC zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="19b33-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for CTRL+ESC.</span></span>

<span data-ttu-id="19b33-122">Diese Eigenschaft ist nur gültig, wenn die [**keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="19b33-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="19b33-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="19b33-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b33-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="19b33-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a><span data-ttu-id="19b33-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="19b33-125">Property value</span></span>

<span data-ttu-id="19b33-126">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="19b33-126">The new virtual-key code.</span></span> <span data-ttu-id="19b33-127">**VK \_ Home** ist der Standardwert, wobei Alt + Home als resultierende Sequenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="19b33-127">**VK\_HOME** is the default value, with ALT+HOME as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="19b33-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="19b33-128">Error codes</span></span>

<span data-ttu-id="19b33-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="19b33-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="19b33-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19b33-130">Remarks</span></span>

<span data-ttu-id="19b33-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="19b33-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19b33-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19b33-132">Requirements</span></span>



| <span data-ttu-id="19b33-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19b33-133">Requirement</span></span> | <span data-ttu-id="19b33-134">Wert</span><span class="sxs-lookup"><span data-stu-id="19b33-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b33-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19b33-135">Minimum supported client</span></span><br/> | <span data-ttu-id="19b33-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19b33-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="19b33-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19b33-137">Minimum supported server</span></span><br/> | <span data-ttu-id="19b33-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19b33-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="19b33-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="19b33-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="19b33-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b33-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="19b33-141">DLL</span><span class="sxs-lookup"><span data-stu-id="19b33-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b33-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b33-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="19b33-143">IID</span><span class="sxs-lookup"><span data-stu-id="19b33-143">IID</span></span><br/>                      | <span data-ttu-id="19b33-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="19b33-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19b33-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19b33-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b33-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="19b33-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="19b33-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="19b33-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="19b33-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="19b33-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="19b33-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="19b33-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="19b33-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="19b33-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="19b33-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="19b33-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="19b33-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="19b33-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="19b33-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="19b33-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





