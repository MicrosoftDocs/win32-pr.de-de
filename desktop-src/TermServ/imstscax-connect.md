---
title: Imstscax Connect-Methode
description: Initiiert eine Verbindung mithilfe der derzeit für das Steuerelement festgelegten Eigenschaften.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Connect-Methode Remotedesktopdienste
- Connect-Methode Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Connect-Methode
- Connect-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Connect-Methode
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949623"
---
# <a name="imstscaxconnect-method"></a><span data-ttu-id="825a6-124">Imstscax:: Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="825a6-124">IMsTscAx::Connect method</span></span>

<span data-ttu-id="825a6-125">Initiiert eine Verbindung mithilfe der derzeit für das Steuerelement festgelegten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="825a6-125">Initiates a connection using the properties currently set on the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="825a6-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="825a6-126">Syntax</span></span>


```C++
HRESULT Connect();
```



## <a name="parameters"></a><span data-ttu-id="825a6-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="825a6-127">Parameters</span></span>

<span data-ttu-id="825a6-128">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="825a6-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="825a6-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="825a6-129">Return value</span></span>

<span data-ttu-id="825a6-130">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="825a6-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="825a6-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="825a6-131">Remarks</span></span>

<span data-ttu-id="825a6-132">Die einzige erforderliche Eigenschaft ist der Servername.</span><span class="sxs-lookup"><span data-stu-id="825a6-132">The only required property is the server name.</span></span> <span data-ttu-id="825a6-133">Weitere Informationen finden Sie in der [**Server**](imstscax-server.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="825a6-133">Refer to the [**Server**](imstscax-server.md) property.</span></span>

<span data-ttu-id="825a6-134">Das-Steuerelement stellt eine asynchrone Verbindung her, sodass eine Rückgabe von einem Connect-Befehl nur anzeigt, dass die Verbindung erfolgreich initiiert wurde, und nicht, dass Sie abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="825a6-134">The control connects asynchronously, so a return from a Connect call indicates only that the connection has been initiated successfully, not that it has been completed.</span></span> <span data-ttu-id="825a6-135">Sie sollten auf Ereignisse auf der [**imstscaxevents**](imstscaxevents-interface.md) -Schnittstelle reagieren, um zu bestimmen, wann das Steuerelement erfolgreich eine Verbindung hergestellt hat (oder ob es getrennt wurde).</span><span class="sxs-lookup"><span data-stu-id="825a6-135">You should respond to events on the [**IMsTscAxEvents**](imstscaxevents-interface.md) interface to determine when the control has successfully connected (or has been disconnected.)</span></span>

<span data-ttu-id="825a6-136">Diese Methode gibt " **E \_ Fail** " zurück, wenn Sie aufgerufen wird, während das Steuerelement bereits verbunden ist oder sich im Verbindungs Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="825a6-136">This method returns **E\_FAIL** if it is called while the control is already connected or in the connecting state.</span></span>

<span data-ttu-id="825a6-137">Nachdem **Connect** aufgerufen wurde, können die meisten Steuerelement Eigenschaften erst dann festgelegt werden, wenn das Steuerelement in den getrennten Zustand zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="825a6-137">After **Connect** has been called, most of the control properties can no longer be set until the control returns to the disconnected state.</span></span>

<span data-ttu-id="825a6-138">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="825a6-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="825a6-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="825a6-139">Requirements</span></span>



| <span data-ttu-id="825a6-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="825a6-140">Requirement</span></span> | <span data-ttu-id="825a6-141">Wert</span><span class="sxs-lookup"><span data-stu-id="825a6-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="825a6-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="825a6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="825a6-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="825a6-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="825a6-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="825a6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="825a6-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="825a6-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="825a6-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="825a6-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="825a6-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="825a6-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="825a6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="825a6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="825a6-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="825a6-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="825a6-150">IID</span><span class="sxs-lookup"><span data-stu-id="825a6-150">IID</span></span><br/>                      | <span data-ttu-id="825a6-151">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="825a6-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="825a6-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="825a6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825a6-153">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="825a6-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="825a6-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="825a6-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="825a6-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="825a6-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="825a6-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="825a6-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="825a6-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="825a6-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="825a6-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="825a6-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="825a6-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="825a6-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="825a6-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="825a6-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="825a6-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="825a6-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="825a6-162">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="825a6-162">**Disconnect**</span></span>](imstscax-disconnect.md)
</dt> <dt>

[<span data-ttu-id="825a6-163">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="825a6-163">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





