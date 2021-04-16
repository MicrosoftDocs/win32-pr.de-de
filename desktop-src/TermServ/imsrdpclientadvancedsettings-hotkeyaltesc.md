---
title: Imsrdpclientadvancedsettings-hotkeyaltesc-Eigenschaft
description: Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Esc zu bestimmen.
ms.assetid: 17cae4ca-8e97-4713-bb4e-ac9a9876c16c
ms.tgt_platform: multiple
keywords:
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyaltesc-Eigenschaft
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, hotkeyaltesc-Eigenschaft
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, hotkeyaltesc-Eigenschaft
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, hotkeyaltesc-Eigenschaft
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, hotkeyaltesc-Eigenschaft
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, hotkeyaltesc-Eigenschaft
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, hotkeyaltesc-Eigenschaft
- Hotkeyaltesc-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, hotkeyaltesc-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltEsc
- IMsRdpClientAdvancedSettings.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyAltEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b661a91a0204177525063629825c478b40b4c29e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479299"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltesc-property"></a><span data-ttu-id="5b665-120">Imsrdpclientadvancedsettings:: hotkeyaltesc-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5b665-120">IMsRdpClientAdvancedSettings::HotKeyAltEsc property</span></span>

<span data-ttu-id="5b665-121">Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Esc zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5b665-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+ESC.</span></span>

<span data-ttu-id="5b665-122">Diese Eigenschaft ist nur gültig, wenn die [**keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5b665-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="5b665-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5b665-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b665-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b665-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltEsc(
  [in]  LONG hotKeyAltEsc
);

HRESULT get_HotKeyAltEsc(
  [out] LONG *photKeyAltEsc
);
```



## <a name="property-value"></a><span data-ttu-id="5b665-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5b665-125">Property value</span></span>

<span data-ttu-id="5b665-126">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="5b665-126">The new virtual-key code.</span></span> <span data-ttu-id="5b665-127">**VK \_ INSERT** ist der Standardwert, wobei alt + INSERT als resultierende Sequenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5b665-127">**VK\_INSERT** is the default value, with ALT+INSERT as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5b665-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5b665-128">Error codes</span></span>

<span data-ttu-id="5b665-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5b665-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b665-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b665-130">Remarks</span></span>

<span data-ttu-id="5b665-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5b665-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b665-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b665-132">Requirements</span></span>



| <span data-ttu-id="5b665-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b665-133">Requirement</span></span> | <span data-ttu-id="5b665-134">Wert</span><span class="sxs-lookup"><span data-stu-id="5b665-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b665-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b665-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5b665-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b665-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="5b665-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b665-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5b665-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b665-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="5b665-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5b665-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b665-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b665-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5b665-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b665-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b665-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b665-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5b665-143">IID</span><span class="sxs-lookup"><span data-stu-id="5b665-143">IID</span></span><br/>                      | <span data-ttu-id="5b665-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="5b665-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b665-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b665-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b665-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5b665-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5b665-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5b665-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5b665-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5b665-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5b665-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5b665-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5b665-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5b665-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5b665-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5b665-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5b665-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5b665-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5b665-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="5b665-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





