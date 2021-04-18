---
title: Imstscax startconnected (Eigenschaft)
description: Gibt an, ob das-Steuerelement die Server Verbindung des Remotedesktop-Sitzungshost (RD-Sitzungshost) unmittelbar nach dem Start herstellen soll.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Startconnected-Eigenschaften Remotedesktopdienste
- Startconnected-Eigenschaften Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, startconnected-Eigenschaft
- Startconnected-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, startconnected-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340977"
---
# <a name="imstscaxstartconnected-property"></a><span data-ttu-id="ccf56-124">Imstscax:: startconnected (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ccf56-124">IMsTscAx::StartConnected property</span></span>

<span data-ttu-id="ccf56-125">Gibt an, ob das-Steuerelement die Server Verbindung des Remotedesktop-Sitzungshost (RD-Sitzungshost) unmittelbar nach dem Start herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="ccf56-125">Indicates whether the control will establish the Remote Desktop Session Host (RD Session Host) server connection immediately upon startup.</span></span>

<span data-ttu-id="ccf56-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ccf56-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccf56-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccf56-127">Syntax</span></span>


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a><span data-ttu-id="ccf56-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ccf56-128">Property value</span></span>

<span data-ttu-id="ccf56-129">Legen Sie diesen Parameter auf **true** fest, wenn das Steuerelement beim Start sofort eine Verbindung herstellen soll, und andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ccf56-129">Set this parameter to **TRUE** if the control should connect immediately on startup, or **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccf56-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ccf56-130">Error codes</span></span>

<span data-ttu-id="ccf56-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ccf56-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccf56-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccf56-132">Remarks</span></span>

<span data-ttu-id="ccf56-133">Diese Eigenschaft ist besonders nützlich, wenn die Steuerelement Eigenschaften in der Parameterliste eines <OBJECT> Tags anstelle von Skript aufrufen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ccf56-133">This property is most useful when the control properties are set in the parameter list of an <OBJECT> tag, rather than through script calls.</span></span>

<span data-ttu-id="ccf56-134">Diese Eigenschaft kann nur verwendet werden, wenn der Servername auch mit der Server-Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ccf56-134">This property can be used only if the server name is also specified using the server property.</span></span> <span data-ttu-id="ccf56-135">Dieser Parameter muss festgelegt werden, bevor das-Steuerelement beispielsweise gestartet wird, indem es in der Parameterliste eines Tags eingeschlossen wird, <OBJECT> Wenn das Steuerelement auf einer Webseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccf56-135">This parameter has to be set before the control starts up for example, by including it in the parameter list of an <OBJECT> tag when using the control from a webpage.</span></span>

<span data-ttu-id="ccf56-136">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ccf56-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf56-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccf56-137">Requirements</span></span>



| <span data-ttu-id="ccf56-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccf56-138">Requirement</span></span> | <span data-ttu-id="ccf56-139">Wert</span><span class="sxs-lookup"><span data-stu-id="ccf56-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf56-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccf56-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf56-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccf56-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ccf56-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccf56-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf56-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccf56-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ccf56-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ccf56-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccf56-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf56-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ccf56-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ccf56-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccf56-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccf56-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ccf56-148">IID</span><span class="sxs-lookup"><span data-stu-id="ccf56-148">IID</span></span><br/>                      | <span data-ttu-id="ccf56-149">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="ccf56-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ccf56-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccf56-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf56-151">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="ccf56-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ccf56-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ccf56-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ccf56-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ccf56-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ccf56-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ccf56-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ccf56-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ccf56-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ccf56-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ccf56-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ccf56-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ccf56-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ccf56-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ccf56-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ccf56-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ccf56-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ccf56-160">Einbetten des Remotedesktop ActiveX-Steuer Elements in eine Webseite</span><span class="sxs-lookup"><span data-stu-id="ccf56-160">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[<span data-ttu-id="ccf56-161">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="ccf56-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





