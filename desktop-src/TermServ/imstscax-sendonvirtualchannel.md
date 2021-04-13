---
title: Imstscax sendonvirtualchannel-Methode
description: Sendet Daten an den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) über einen virtuellen Kanal, der zuvor mithilfe der Methode "| atevirtualchannels" erstellt wurde.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Sendonvirtualchannel-Methode Remotedesktopdienste
- Sendonvirtualchannel-Methode Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
- Sendonvirtualchannel-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, sendonvirtualchannel-Methode
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475612"
---
# <a name="imstscaxsendonvirtualchannel-method"></a><span data-ttu-id="b857f-124">Imstscax:: sendonvirtualchannel-Methode</span><span class="sxs-lookup"><span data-stu-id="b857f-124">IMsTscAx::SendOnVirtualChannel method</span></span>

<span data-ttu-id="b857f-125">Sendet Daten an den Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) über einen virtuellen Kanal, der zuvor mithilfe der Methode "| [**atevirtualchannels**](imstscax-createvirtualchannels.md) " erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b857f-125">Sends data to the Remote Desktop Session Host (RD Session Host) server over a virtual channel that was created previously by using the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b857f-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="b857f-126">Syntax</span></span>


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a><span data-ttu-id="b857f-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="b857f-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b857f-128">*Channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b857f-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b857f-129">Der Name des virtuellen Kanals, der im Aufrufen von " [**anatevirtualchannels**](imstscax-createvirtualchannels.md)" angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b857f-129">The virtual channel name that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="b857f-130">*Chandata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b857f-130">*ChanData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b857f-131">Die Daten, die über den virtuellen Kanal in **BSTR** -Form gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b857f-131">The data to send over the virtual channel, in **BSTR** form.</span></span> <span data-ttu-id="b857f-132">Es gibt keine Einschränkung, dass diese Daten Zeichen folgen mit null-terminierten Zeichen folgen müssen.</span><span class="sxs-lookup"><span data-stu-id="b857f-132">There is no restriction that this data must be null-terminated strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b857f-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b857f-133">Return value</span></span>

<span data-ttu-id="b857f-134">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b857f-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b857f-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b857f-135">Remarks</span></span>

<span data-ttu-id="b857f-136">Informationen zu Benennungs Einschränkungen für virtuelle Kanäle finden Sie unter [Virtual Channel Client-Registrierung](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="b857f-136">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="b857f-137">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b857f-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b857f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b857f-138">Requirements</span></span>



| <span data-ttu-id="b857f-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b857f-139">Requirement</span></span> | <span data-ttu-id="b857f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="b857f-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b857f-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b857f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b857f-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b857f-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b857f-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b857f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b857f-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b857f-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b857f-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b857f-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="b857f-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b857f-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b857f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b857f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b857f-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b857f-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b857f-149">IID</span><span class="sxs-lookup"><span data-stu-id="b857f-149">IID</span></span><br/>                      | <span data-ttu-id="b857f-150">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="b857f-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b857f-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b857f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b857f-152">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="b857f-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="b857f-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="b857f-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="b857f-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="b857f-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="b857f-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="b857f-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="b857f-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b857f-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b857f-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b857f-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b857f-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b857f-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b857f-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b857f-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b857f-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b857f-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b857f-161">**"Kreatevirtualchannels"**</span><span class="sxs-lookup"><span data-stu-id="b857f-161">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="b857f-162">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="b857f-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





