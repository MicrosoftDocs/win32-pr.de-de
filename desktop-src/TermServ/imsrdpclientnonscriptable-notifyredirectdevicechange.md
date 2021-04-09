---
title: Imsrdpclientnonscriptable notifyredirectdevicechange-Methode
description: Benachrichtigt das Geräte Umleitungs Modul des Remotedesktop ActiveX-Steuer Elements, dass eine Geräte Änderung auf dem System aufgetreten ist. Diese Methode übergibt WM \_ devicechange-Benachrichtigungen an das-Steuerelement.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Notifyredirectdevicechange-Methode Remotedesktopdienste
- Notifyredirectdevicechange-Methode Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
- Notifyredirectdevicechange-Methode Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste, notifyredirectdevicechange-Methode
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957131"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a><span data-ttu-id="b9108-115">Imsrdpclientnonscriptable:: notifyredirectdevicechange-Methode</span><span class="sxs-lookup"><span data-stu-id="b9108-115">IMsRdpClientNonScriptable::NotifyRedirectDeviceChange method</span></span>

<span data-ttu-id="b9108-116">Benachrichtigt das Geräte Umleitungs Modul des Remotedesktop ActiveX-Steuer Elements, dass eine Geräte Änderung auf dem System aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b9108-116">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="b9108-117">Diese Methode übergibt [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) -Benachrichtigungen an das-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="b9108-117">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9108-118">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9108-118">Syntax</span></span>


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="b9108-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9108-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9108-120">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9108-120">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9108-121">Gibt das Geräte Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="b9108-121">Specifies the device event.</span></span> <span data-ttu-id="b9108-122">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="b9108-122">This parameter can be one of the following values.</span></span>

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span data-ttu-id="b9108-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ configchangeabgeb Rochen**</span><span class="sxs-lookup"><span data-stu-id="b9108-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT\_CONFIGCHANGECANCELED**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-124">Eine Anforderung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b9108-124">A request to change the current configuration (dock or undock) has been canceled.</span></span>

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span data-ttu-id="b9108-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT- \_ ConfigChanged**</span><span class="sxs-lookup"><span data-stu-id="b9108-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT\_CONFIGCHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-126">Die aktuelle Konfiguration wurde aufgrund eines Andocken oder Abdocken geändert.</span><span class="sxs-lookup"><span data-stu-id="b9108-126">The current configuration has changed due to a dock or undock.</span></span>

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span data-ttu-id="b9108-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CustomEvent**</span><span class="sxs-lookup"><span data-stu-id="b9108-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT\_CUSTOMEVENT**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-128">Ein benutzerdefiniertes Ereignis ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b9108-128">A custom event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span data-ttu-id="b9108-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ devicearrival**</span><span class="sxs-lookup"><span data-stu-id="b9108-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT\_DEVICEARRIVAL**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-130">Ein Gerät wurde eingefügt und ist jetzt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9108-130">A device has been inserted and is now available.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span data-ttu-id="b9108-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DeviceQueryRemove**</span><span class="sxs-lookup"><span data-stu-id="b9108-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT\_DEVICEQUERYREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-132">Die Berechtigung zum Entfernen eines Geräts wird angefordert.</span><span class="sxs-lookup"><span data-stu-id="b9108-132">Permission is requested to remove a device.</span></span> <span data-ttu-id="b9108-133">Jede Anwendung kann diese Anforderung verweigern und das Entfernen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="b9108-133">Any application can deny this request and cancel the removal.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span data-ttu-id="b9108-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ devicequeryremovefailed**</span><span class="sxs-lookup"><span data-stu-id="b9108-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT\_DEVICEQUERYREMOVEFAILED**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-135">Eine Anforderung zum Entfernen eines Geräts wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b9108-135">A request to remove a device has been canceled.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span data-ttu-id="b9108-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ deviceremovecomplete**</span><span class="sxs-lookup"><span data-stu-id="b9108-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT\_DEVICEREMOVECOMPLETE**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-137">Ein Gerät wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="b9108-137">A device has been removed.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span data-ttu-id="b9108-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ deviceremovepending**</span><span class="sxs-lookup"><span data-stu-id="b9108-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT\_DEVICEREMOVEPENDING**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-139">Ein Gerät wird gerade entfernt.</span><span class="sxs-lookup"><span data-stu-id="b9108-139">A device is about to be removed.</span></span> <span data-ttu-id="b9108-140">Das Entfernen kann nicht verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="b9108-140">The removal cannot be denied.</span></span>

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span data-ttu-id="b9108-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT-Geräte- \_ /richtlinientypespecific**</span><span class="sxs-lookup"><span data-stu-id="b9108-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT\_DEVICETYPESPECIFIC**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-142">Ein Geräte spezifisches Ereignis ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b9108-142">A device-specific event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span data-ttu-id="b9108-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT- \_ Devnodes \_ geändert**</span><span class="sxs-lookup"><span data-stu-id="b9108-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT\_DEVNODES\_CHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-144">Ein Gerät wurde dem System hinzugefügt oder daraus entfernt.</span><span class="sxs-lookup"><span data-stu-id="b9108-144">A device has been added to or removed from the system.</span></span>

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span data-ttu-id="b9108-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ querychangeconfig**</span><span class="sxs-lookup"><span data-stu-id="b9108-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT\_QUERYCHANGECONFIG**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-146">Die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wird angefordert.</span><span class="sxs-lookup"><span data-stu-id="b9108-146">Permission is requested to change the current configuration (dock or undock).</span></span>

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span data-ttu-id="b9108-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ UserDefined**</span><span class="sxs-lookup"><span data-stu-id="b9108-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT\_USERDEFINED**</span></span>


</dt> <dd>

<span data-ttu-id="b9108-148">Die Bedeutung dieser Meldung ist Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="b9108-148">The meaning of this message is user-defined.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b9108-149">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9108-149">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9108-150">Zeiger auf eine-Struktur, die ereignisspezifische Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="b9108-150">Pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="b9108-151">Das Format hängt vom Wert des *wParam* -Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="b9108-151">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="b9108-152">Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="b9108-152">For more information, refer to the documentation for each event.</span></span> <span data-ttu-id="b9108-153">Weitere Informationen finden Sie unter [Geräte Ereignis Typen](/windows/desktop/DevIO/device-event-types).</span><span class="sxs-lookup"><span data-stu-id="b9108-153">For more information, see [Device Event Types](/windows/desktop/DevIO/device-event-types).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9108-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9108-154">Return value</span></span>

<span data-ttu-id="b9108-155">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b9108-155">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9108-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9108-156">Remarks</span></span>

<span data-ttu-id="b9108-157">Eine Containeranwendung, die das dynamische Hinzufügen oder Entfernen von Geräten zulässt, sollte die [**WM \_ devicechange**](/windows/desktop/DevIO/wm-devicechange) -Nachricht im Fenster der obersten Ebene verarbeiten und die Nachricht mithilfe der **notifyredirectdevicechange** -Methode an das Steuerelement weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="b9108-157">A container application that allows dynamic addition or removal of devices should process the [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) message in its top level window and forward the message to the control using the **NotifyRedirectDeviceChange** method.</span></span> <span data-ttu-id="b9108-158">Ein Beispiel für eine dynamische Geräte Änderung ist, wenn ein umgeleitetes Laufwerk hinzugefügt oder entfernt wird, während das System ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9108-158">An example of a dynamic device change is when a redirected disk drive is added or removed while the system is running.</span></span>

<span data-ttu-id="b9108-159">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b9108-159">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9108-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9108-160">Requirements</span></span>



| <span data-ttu-id="b9108-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9108-161">Requirement</span></span> | <span data-ttu-id="b9108-162">Wert</span><span class="sxs-lookup"><span data-stu-id="b9108-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9108-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9108-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b9108-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9108-164">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="b9108-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9108-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b9108-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9108-166">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="b9108-167">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b9108-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9108-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9108-168"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="b9108-169">DLL</span><span class="sxs-lookup"><span data-stu-id="b9108-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9108-170"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9108-170"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="b9108-171">IID</span><span class="sxs-lookup"><span data-stu-id="b9108-171">IID</span></span><br/>                      | <span data-ttu-id="b9108-172">IID \_ imsrdpclientnonscriptable ist als 2f079c4c-87b2-4afd-97ab-20cdb43038ae definiert.</span><span class="sxs-lookup"><span data-stu-id="b9108-172">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9108-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9108-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9108-174">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="b9108-174">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="b9108-175">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="b9108-175">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="b9108-176">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="b9108-176">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="b9108-177">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="b9108-177">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="b9108-178">**Imsrdpclientnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="b9108-178">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

