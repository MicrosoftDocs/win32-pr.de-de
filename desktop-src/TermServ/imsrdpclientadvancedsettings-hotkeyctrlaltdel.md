---
title: Imsrdpclientadvancedsettings-hotkeyctrlaltdel-Eigenschaft
description: Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + ENTF, auch als "sichere Aufmerksamkeit" (Secure Attention Sequence, SAS) bezeichnet.
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
- Hotkeyctrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyctrlaltdel-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fa4c1f963841d0c1ea0375cdf11913b28d0286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391603"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a><span data-ttu-id="158dd-120">Imsrdpclientadvancedsettings:: hotkeyctrlaltdel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="158dd-120">IMsRdpClientAdvancedSettings::HotKeyCtrlAltDel property</span></span>

<span data-ttu-id="158dd-121">Gibt den Code des virtuellen Schlüssels an, der STRG + ALT hinzugefügt werden soll, um die Hotkey-Ersetzung für STRG + ALT + ENTF, auch als "sichere Aufmerksamkeit" (Secure Attention Sequence, SAS) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="158dd-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+DELETE, also called the secure attention sequence (SAS).</span></span>

> [!Note]  
> <span data-ttu-id="158dd-122">STRG + ALT + ENTF wird nie an den Remote Server umgeleitet, auch wenn die [keyboardhuokmode](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft aktiviert ist. STRG + ALT + ENTF ist die lokale SAS-Sequenz.</span><span class="sxs-lookup"><span data-stu-id="158dd-122">CTRL+ALT+DELETE is never redirected to the remote server, even when the [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) property is enabled; CTRL+ALT+DELETE is the local SAS sequence.</span></span>

 

<span data-ttu-id="158dd-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="158dd-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="158dd-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="158dd-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="158dd-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="158dd-125">Property value</span></span>

<span data-ttu-id="158dd-126">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="158dd-126">The new virtual-key code.</span></span> <span data-ttu-id="158dd-127">**VK \_ "End** " ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="158dd-127">**VK\_END** is the default.</span></span>

## <a name="error-codes"></a><span data-ttu-id="158dd-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="158dd-128">Error codes</span></span>

<span data-ttu-id="158dd-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="158dd-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="158dd-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="158dd-130">Remarks</span></span>

<span data-ttu-id="158dd-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="158dd-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="158dd-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="158dd-132">Requirements</span></span>



| <span data-ttu-id="158dd-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="158dd-133">Requirement</span></span> | <span data-ttu-id="158dd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="158dd-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="158dd-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="158dd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="158dd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="158dd-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="158dd-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="158dd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="158dd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="158dd-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="158dd-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="158dd-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="158dd-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="158dd-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="158dd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="158dd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="158dd-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="158dd-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="158dd-143">IID</span><span class="sxs-lookup"><span data-stu-id="158dd-143">IID</span></span><br/>                      | <span data-ttu-id="158dd-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="158dd-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="158dd-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="158dd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158dd-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="158dd-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="158dd-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="158dd-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="158dd-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="158dd-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="158dd-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="158dd-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="158dd-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="158dd-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="158dd-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="158dd-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="158dd-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="158dd-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="158dd-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="158dd-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





