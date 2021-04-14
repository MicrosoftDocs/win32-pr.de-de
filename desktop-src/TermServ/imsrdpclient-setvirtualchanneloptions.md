---
title: Imsrdpclient setvirtualchanneloptions-Methode
description: Legt die Optionen des virtuellen Kanals für das Remotedesktop ActiveX-Steuerelement fest.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Setvirtualchanneloptions-Methode Remotedesktopdienste
- Setvirtualchanneloptions-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
- Setvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, setvirtualchanneloptions-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391684"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a><span data-ttu-id="6f6b1-124">Imsrdpclient:: setvirtualchanneloptions-Methode</span><span class="sxs-lookup"><span data-stu-id="6f6b1-124">IMsRdpClient::SetVirtualChannelOptions method</span></span>

<span data-ttu-id="6f6b1-125">Legt die Optionen des virtuellen Kanals für das Remotedesktop ActiveX-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-125">Sets the virtual channel options for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="6f6b1-126">Rufen Sie diese Methode nach dem Aufrufen der [**createvirtualchannels**](imstscax-createvirtualchannels.md) -Methode auf, aber vor dem Herstellen einer Verbindung mit der [**Connect**](imstscax-connect.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-126">Call this method after calling the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method, but before establishing a connection with the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="6f6b1-127">Mit dieser Methode werden zusätzliche Optionen für virtuelle Kanäle festgelegt, die mit " **kreatevirtualchannels**" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-127">This method sets additional options on virtual channels that have been created with **CreateVirtualChannels**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6b1-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f6b1-128">Syntax</span></span>


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="6f6b1-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f6b1-129">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f6b1-130">*Channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f6b1-130">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f6b1-131">Der Name des virtuellen Kanals, der im Aufrufen der Methode " [**kreatevirtualchannels**](imstscax-createvirtualchannels.md) " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-131">The name of the virtual channel that was specified in the call to the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="6f6b1-132">*chanoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f6b1-132">*chanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f6b1-133">Die Optionen, die für den durch den *channame* -Parameter angegebenen virtuellen Kanal festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-133">The options to set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="6f6b1-134">Eine Beschreibung möglicher Optionen finden Sie unter [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="6f6b1-134">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span> <span data-ttu-id="6f6b1-135">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="6f6b1-135">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f6b1-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f6b1-136">Return value</span></span>

<span data-ttu-id="6f6b1-137">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-137">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6b1-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f6b1-138">Remarks</span></span>

<span data-ttu-id="6f6b1-139">Ein Beispiel für die Verwendung dieser Methode wäre, den Kanal als persistente Remote Steuerung zu deklarieren, indem Sie die **Kanal \_ Option \_ \_ \_ persistentes** Flag für die Remote Steuerung festlegen.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-139">An example of using this method would be to declare the channel as remote control persistent by setting the **CHANNEL\_OPTION\_REMOTE\_CONTROL\_PERSISTENT** flag.</span></span> <span data-ttu-id="6f6b1-140">Dies bedeutet, dass der Kanal nicht geschlossen wird, wenn eine Remote Steuerung eine Verbindung mit der Sitzung herstellt, die mit dem Client verbunden ist, oder die Verbindung trennt.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-140">This means that the channel would not be closed when a remote control connects to or disconnects from the session connected to the client.</span></span> <span data-ttu-id="6f6b1-141">Weitere Informationen finden Sie unter [permanente virtuelle Kanäle für die Remote Steuerung](remote-control-persistent-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="6f6b1-141">For more information, see [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).</span></span>

<span data-ttu-id="6f6b1-142">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6f6b1-142">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f6b1-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f6b1-143">Requirements</span></span>



| <span data-ttu-id="6f6b1-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f6b1-144">Requirement</span></span> | <span data-ttu-id="6f6b1-145">Wert</span><span class="sxs-lookup"><span data-stu-id="6f6b1-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f6b1-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f6b1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6f6b1-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f6b1-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6f6b1-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f6b1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6f6b1-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f6b1-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6f6b1-150">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6f6b1-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f6b1-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f6b1-151"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f6b1-152">DLL</span><span class="sxs-lookup"><span data-stu-id="6f6b1-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f6b1-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f6b1-153"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f6b1-154">IID</span><span class="sxs-lookup"><span data-stu-id="6f6b1-154">IID</span></span><br/>                      | <span data-ttu-id="6f6b1-155">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="6f6b1-155">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6f6b1-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f6b1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f6b1-157">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-157">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-158">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-158">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-159">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-159">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-160">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-160">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-161">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-161">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-162">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-162">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-163">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-163">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-164">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-164">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-165">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-165">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-166">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-166">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-167">**Channel \_ DEF**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-167">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="6f6b1-168">**"Kreatevirtualchannels"**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-168">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="6f6b1-169">**Getvirtualchanneloptions**</span><span class="sxs-lookup"><span data-stu-id="6f6b1-169">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





