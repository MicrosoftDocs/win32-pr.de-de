---
title: Imsrdpclient getvirtualchanneloptions-Methode
description: Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Getvirtualchanneloptions-Methode Remotedesktopdienste
- Getvirtualchanneloptions-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
- Getvirtualchanneloptions-Methode Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, getvirtualchanneloptions-Methode
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346758"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a><span data-ttu-id="004cc-124">Imsrdpclient:: getvirtualchanneloptions-Methode</span><span class="sxs-lookup"><span data-stu-id="004cc-124">IMsRdpClient::GetVirtualChannelOptions method</span></span>

<span data-ttu-id="004cc-125">Ruft die Optionen ab, die für einen virtuellen Kanal festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="004cc-125">Retrieves the options set for a virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="004cc-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="004cc-126">Syntax</span></span>


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="004cc-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="004cc-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="004cc-128">*Channame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="004cc-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="004cc-129">Der Name eines virtuellen Kanals, der im Aufrufen der Methode " [**kreatevirtualchannels**](imstscax-createvirtualchannels.md) " angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="004cc-129">The name of a virtual channel that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="004cc-130">*pchanoptions* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="004cc-130">*pChanOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="004cc-131">Die Optionen, die für den durch den *channame* -Parameter angegebenen virtuellen Kanal festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="004cc-131">The options set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="004cc-132">Eine Beschreibung möglicher Optionen finden Sie unter [**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="004cc-132">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="004cc-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="004cc-133">Return value</span></span>

<span data-ttu-id="004cc-134">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="004cc-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="004cc-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="004cc-135">Remarks</span></span>

<span data-ttu-id="004cc-136">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="004cc-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="004cc-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="004cc-137">Requirements</span></span>



| <span data-ttu-id="004cc-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="004cc-138">Requirement</span></span> | <span data-ttu-id="004cc-139">Wert</span><span class="sxs-lookup"><span data-stu-id="004cc-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="004cc-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="004cc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="004cc-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="004cc-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="004cc-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="004cc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="004cc-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="004cc-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="004cc-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="004cc-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="004cc-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="004cc-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="004cc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="004cc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="004cc-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="004cc-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="004cc-148">IID</span><span class="sxs-lookup"><span data-stu-id="004cc-148">IID</span></span><br/>                      | <span data-ttu-id="004cc-149">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="004cc-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="004cc-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="004cc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004cc-151">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="004cc-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="004cc-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="004cc-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="004cc-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="004cc-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="004cc-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="004cc-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="004cc-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="004cc-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="004cc-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="004cc-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="004cc-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="004cc-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="004cc-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="004cc-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="004cc-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="004cc-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="004cc-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="004cc-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="004cc-161">**Channel \_ DEF**</span><span class="sxs-lookup"><span data-stu-id="004cc-161">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="004cc-162">**"Kreatevirtualchannels"**</span><span class="sxs-lookup"><span data-stu-id="004cc-162">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="004cc-163">**Setvirtualchanneloptions**</span><span class="sxs-lookup"><span data-stu-id="004cc-163">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





