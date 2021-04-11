---
title: Imsrdpclientadvancedsettings-hotkeyaltspace-Eigenschaft
description: Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Leertaste zu bestimmen.
ms.assetid: 943935e9-a6f1-496e-895c-e993755e25cc
ms.tgt_platform: multiple
keywords:
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
- Hotkeyaltspace-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, hotkeyaltspace-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltSpace
- IMsRdpClientAdvancedSettings.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.put_HotKeyAltSpace
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b257bd04171f8bff22bbe91ee7310fafe89c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949799"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltspace-property"></a><span data-ttu-id="804b0-120">Imsrdpclientadvancedsettings:: hotkeyaltspace-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="804b0-120">IMsRdpClientAdvancedSettings::HotKeyAltSpace property</span></span>

<span data-ttu-id="804b0-121">Gibt den Code des virtuellen Schlüssels an, der alt addiert werden soll, um die Hotkey-Ersetzung für Alt + Leertaste zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="804b0-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SPACE.</span></span>

<span data-ttu-id="804b0-122">Diese Eigenschaft ist nur gültig, wenn die [**keyboardhuokmode**](imsrdpclientsecuredsettings-keyboardhookmode.md) -Eigenschaft nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="804b0-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="804b0-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="804b0-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="804b0-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="804b0-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltSpace(
  [in]  LONG hotKeyAltSpace
);

HRESULT get_HotKeyAltSpace(
  [out] LONG *photKeyAltSpace
);
```



## <a name="property-value"></a><span data-ttu-id="804b0-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="804b0-125">Property value</span></span>

<span data-ttu-id="804b0-126">Der neue Code des virtuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="804b0-126">The new virtual-key code.</span></span> <span data-ttu-id="804b0-127">**VK \_ DELETE** ist die Standardeinstellung, wobei ALT + DELETE als resultierende Sequenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="804b0-127">**VK\_DELETE** is the default, with ALT+DELETE as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="804b0-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="804b0-128">Error codes</span></span>

<span data-ttu-id="804b0-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="804b0-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="804b0-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="804b0-130">Remarks</span></span>

<span data-ttu-id="804b0-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="804b0-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="804b0-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="804b0-132">Requirements</span></span>



| <span data-ttu-id="804b0-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="804b0-133">Requirement</span></span> | <span data-ttu-id="804b0-134">Wert</span><span class="sxs-lookup"><span data-stu-id="804b0-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="804b0-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="804b0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="804b0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="804b0-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="804b0-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="804b0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="804b0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="804b0-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="804b0-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="804b0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="804b0-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="804b0-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="804b0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="804b0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="804b0-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="804b0-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="804b0-143">IID</span><span class="sxs-lookup"><span data-stu-id="804b0-143">IID</span></span><br/>                      | <span data-ttu-id="804b0-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="804b0-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="804b0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="804b0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804b0-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="804b0-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="804b0-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="804b0-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="804b0-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="804b0-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="804b0-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="804b0-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="804b0-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="804b0-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="804b0-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="804b0-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="804b0-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="804b0-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="804b0-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="804b0-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





