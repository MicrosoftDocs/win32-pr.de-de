---
title: Imstscadvancedsettings containerhandledfullscreen-Eigenschaft
description: Gibt an, ob der vom Container behandelte Vollbildmodus aktiviert ist.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
- Containerhandledfullscreen-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, containerhandledfullscreen-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392027"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a><span data-ttu-id="98e66-122">Imstscadvancedsettings:: containerhandledfullscreen-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="98e66-122">IMsTscAdvancedSettings::ContainerHandledFullScreen property</span></span>

<span data-ttu-id="98e66-123">Gibt an, ob der vom Container behandelte Vollbildmodus aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="98e66-123">Specifies whether the container-handled full-screen mode is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="98e66-124">Der Wert der **containerhandledfullscreen** -Eigenschaft hat keine Auswirkung, wenn das Remotedesktop ActiveX-Steuerelement für die Skripterstellung sicher ist, und gibt **\_ false** zurück, wenn versucht wird, den Wert zu ändern.</span><span class="sxs-lookup"><span data-stu-id="98e66-124">The value of the **ContainerHandledFullScreen** property has no effect when the Remote Desktop ActiveX control is safe for scripting, and returns **S\_FALSE** when an attempt is made to change the value.</span></span>

 

<span data-ttu-id="98e66-125">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="98e66-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e66-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="98e66-126">Syntax</span></span>


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="98e66-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="98e66-127">Property value</span></span>

<span data-ttu-id="98e66-128">Legen Sie diesen Parameter auf " **true** " fest, um den Modus oder einen anderen Wert zum Deaktivieren des Modus zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="98e66-128">Set this parameter to **TRUE** to enable the mode or another value to disable the mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="98e66-129">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="98e66-129">Error codes</span></span>

<span data-ttu-id="98e66-130">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="98e66-130">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="98e66-131">Gibt **\_ false** zurück, wenn dies nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="98e66-131">Returns **S\_FALSE** if not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e66-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98e66-132">Remarks</span></span>

<span data-ttu-id="98e66-133">Wenn dieser Modus aktiviert ist, verarbeitet der aktuelle Container den Wechsel in den und aus dem Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="98e66-133">When this mode is enabled, the current container processes the switch into and out of full-screen mode.</span></span> <span data-ttu-id="98e66-134">Diese Methode sollte nur verwendet werden, wenn der aktuelle Container eine umfassende Kontrolle über das Verhalten im Vollbildmodus benötigt.</span><span class="sxs-lookup"><span data-stu-id="98e66-134">This method should be used only if the current container needs extensive control over full-screen mode behavior.</span></span> <span data-ttu-id="98e66-135">Wenn diese Eigenschaft festgelegt ist, wird das Steuerelement nicht in der Antwort auf die Tastenkombination für den Vollbildmodus (Strg + Alt + untlos) angezeigt oder verlässt den Vollbildmodus. Stattdessen werden die Ereignisse [**imstscaxevents:: onrequestgofullscreen**](imstscaxevents-onrequestgofullscreen.md) und [**imstscaxevents:: onrequestleavefullscreen**](imstscaxevents-onrequestleavefullscreen.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="98e66-135">When this property is set, the control does not enter or leave full-screen mode in response to the full-screen mode shortcut key combination (CTRL+ALT+BREAK); instead, the [**IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) and [**IMsTscAxEvents::OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) events are called.</span></span> <span data-ttu-id="98e66-136">Weitere Informationen zu diesen Ereignissen finden Sie unter [**imstscaxevents**](imstscaxevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="98e66-136">See [**IMsTscAxEvents**](imstscaxevents-interface.md) for more information about these events.</span></span>

<span data-ttu-id="98e66-137">Die meisten Container Anwendungen müssen den im Container behandelten Vollbildmodus nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="98e66-137">Most container applications will not need to use container-handled full-screen mode.</span></span>

<span data-ttu-id="98e66-138">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="98e66-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98e66-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98e66-139">Requirements</span></span>



| <span data-ttu-id="98e66-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98e66-140">Requirement</span></span> | <span data-ttu-id="98e66-141">Wert</span><span class="sxs-lookup"><span data-stu-id="98e66-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e66-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98e66-142">Minimum supported client</span></span><br/> | <span data-ttu-id="98e66-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98e66-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="98e66-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98e66-144">Minimum supported server</span></span><br/> | <span data-ttu-id="98e66-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98e66-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="98e66-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="98e66-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="98e66-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e66-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="98e66-148">DLL</span><span class="sxs-lookup"><span data-stu-id="98e66-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98e66-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e66-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="98e66-150">IID</span><span class="sxs-lookup"><span data-stu-id="98e66-150">IID</span></span><br/>                      | <span data-ttu-id="98e66-151">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="98e66-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98e66-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98e66-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e66-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="98e66-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="98e66-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="98e66-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="98e66-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="98e66-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="98e66-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="98e66-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="98e66-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="98e66-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="98e66-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="98e66-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="98e66-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="98e66-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="98e66-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="98e66-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="98e66-161">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="98e66-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





