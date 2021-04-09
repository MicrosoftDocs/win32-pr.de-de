---
title: Imsrdpclient RequestClose-Methode
description: Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuer Elements an.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- RequestClose-Methode Remotedesktopdienste
- RequestClose-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, RequestClose-Methode
- RequestClose-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, RequestClose-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740576"
---
# <a name="imsrdpclientrequestclose-method"></a><span data-ttu-id="a1a7b-124">Imsrdpclient:: RequestClose-Methode</span><span class="sxs-lookup"><span data-stu-id="a1a7b-124">IMsRdpClient::RequestClose method</span></span>

<span data-ttu-id="a1a7b-125">Fordert ein ordnungsgemäßes Herunterfahren des Remotedesktop ActiveX-Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-125">Requests a graceful shutdown of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="a1a7b-126">Ein ordnungsgemäßes Herunterfahren kann das Beenden der Remotedesktopdienste Sitzung des Benutzers einschließen, aber der Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server wird nicht heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-126">A graceful shutdown can include ending the user's Remote Desktop Services session but it does not shut down the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a7b-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1a7b-127">Syntax</span></span>


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a1a7b-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1a7b-128">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a7b-129">*pclosestatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1a7b-129">*pCloseStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a7b-130">Der Wert aus der [**controlclosestatus**](controlclosestatus.md) -Enumeration, der angibt, ob die Anwendung das Steuerelement sofort schließen kann.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-130">Value from the [**ControlCloseStatus**](controlclosestatus.md) enumeration that indicates whether the application can close the control immediately.</span></span> <span data-ttu-id="a1a7b-131">Im folgenden finden Sie eine Liste möglicher Werte.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-131">Following is a list of possible values.</span></span>

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span data-ttu-id="a1a7b-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlclosecanfortsetzung** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="a1a7b-132"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="a1a7b-133">Die Containeranwendung kann fortfahren, um das Steuerelement sofort zu schließen.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-133">The container application can proceed to close the control immediately.</span></span> <span data-ttu-id="a1a7b-134">Dieser Wert kann auch darauf hindeuten, dass die Verbindung bereits beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-134">This value can also indicate that the connection has already terminated.</span></span>

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span data-ttu-id="a1a7b-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlclosewaitforevents** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="a1a7b-135"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="a1a7b-136">Die Containeranwendung sollte das Steuerelement nicht sofort schließen. die Anwendung sollte warten, bis eines der im folgenden Abschnitt "Hinweise" beschriebenen Ereignisse vor dem Schließen auftritt.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-136">The container application should not close the control immediately; the application should wait for one of the events described in the following Remarks section to occur before closing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a7b-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1a7b-137">Return value</span></span>

<span data-ttu-id="a1a7b-138">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a7b-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1a7b-139">Remarks</span></span>

<span data-ttu-id="a1a7b-140">Wenn der Parameter " *pclosestatus* " gleich " **controlclosewaitforevents**" ist, muss die Anwendung warten, bis eines der folgenden Ereignisse eintritt, bevor die Anwendung das Steuerelement schließt:</span><span class="sxs-lookup"><span data-stu-id="a1a7b-140">If the *pCloseStatus* parameter is equal to **controlCloseWaitForEvents**, the application should wait for one of the following events to occur before the application closes the control:</span></span>

-   <span data-ttu-id="a1a7b-141">[**Imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="a1a7b-141">[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md).</span></span> <span data-ttu-id="a1a7b-142">Wenn der Benutzer nicht bei der Remotedesktopdienste Sitzung angemeldet ist, kann die Anwendung die [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) -Funktion aufzurufen, um alle Fenster zu zerstören und dann das Steuerelement zu schließen.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-142">If the user is not logged on to the Remote Desktop Services session, the application can call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy all windows and then close the control.</span></span>
-   <span data-ttu-id="a1a7b-143">[**Imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="a1a7b-143">[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span> <span data-ttu-id="a1a7b-144">Wenn der Benutzer bei der Remotedesktopdienste Sitzung angemeldet ist, löst das Steuerelement ein **onconfirmclose** -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-144">If the user is logged on to the Remote Desktop Services session, the control fires an **OnConfirmClose** event.</span></span> <span data-ttu-id="a1a7b-145">Dieses Ereignis ermöglicht der Anwendung, den Benutzer zur Eingabe aufzufordern, ob die Verbindung geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-145">This event allows the application to prompt the user about whether to close the connection.</span></span> <span data-ttu-id="a1a7b-146">Wenn der Benutzer die Eingabeaufforderung auf Ja antwortet, kann die Containeranwendung [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) zum zerstören aller Fenster und zum Schließen des Steuer Elements auffordern.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-146">If the user replies yes to the prompt, the container application can call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to destroy all windows, and close the control.</span></span>

<span data-ttu-id="a1a7b-147">**RequestClose** ermöglicht einer Containeranwendung, den Benutzer aufzufordern, ob eine Verbindung geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-147">**RequestClose** allows a container application to prompt the user about whether to close a connection.</span></span> <span data-ttu-id="a1a7b-148">Weitere Informationen finden Sie unter [**imstscaxevents:: onconfirmclose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="a1a7b-148">For more information, see [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

<span data-ttu-id="a1a7b-149">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a1a7b-149">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a7b-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1a7b-150">Requirements</span></span>



| <span data-ttu-id="a1a7b-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1a7b-151">Requirement</span></span> | <span data-ttu-id="a1a7b-152">Wert</span><span class="sxs-lookup"><span data-stu-id="a1a7b-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a7b-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1a7b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a7b-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1a7b-154">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a1a7b-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1a7b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a7b-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1a7b-156">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a1a7b-157">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a1a7b-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1a7b-158"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1a7b-158"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1a7b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a1a7b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1a7b-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1a7b-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a1a7b-161">IID</span><span class="sxs-lookup"><span data-stu-id="a1a7b-161">IID</span></span><br/>                      | <span data-ttu-id="a1a7b-162">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="a1a7b-162">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a1a7b-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1a7b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a7b-164">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-164">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-165">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-165">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-166">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-166">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-167">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-167">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-168">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-168">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-169">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-169">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-170">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-170">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-171">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-171">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-172">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-172">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-173">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-173">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-174">**Imstscaxevents:: onconfirmclose**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-174">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="a1a7b-175">**Imstscaxevents:: ongetrennte**</span><span class="sxs-lookup"><span data-stu-id="a1a7b-175">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

