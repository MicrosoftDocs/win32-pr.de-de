---
title: Imstscax-Methode der Methode "foratevirtualchannels"
description: Erstellt ein Client seitiges virtuelles Channel-Objekt für jeden angegebenen virtuellen Kanalnamen.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste "der Methode" "," imstscax "-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "" der Methode "imsrdpclient"
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient2",-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient3",-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient4",-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient5",-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient6",-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient7",-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient8",-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
- Methode Remotedesktopdienste der Methode "IMsRdpClient9",-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, Methode "kreatevirtualchannels"
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477733"
---
# <a name="imstscaxcreatevirtualchannels-method"></a><span data-ttu-id="c7462-124">Imstscax:: foratevirtualchannels-Methode</span><span class="sxs-lookup"><span data-stu-id="c7462-124">IMsTscAx::CreateVirtualChannels method</span></span>

<span data-ttu-id="c7462-125">Erstellt ein Client seitiges virtuelles Channel-Objekt für jeden angegebenen virtuellen Kanalnamen.</span><span class="sxs-lookup"><span data-stu-id="c7462-125">Creates a client-side virtual channel object for each specified virtual channel name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7462-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7462-126">Syntax</span></span>


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="c7462-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7462-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7462-128">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7462-128">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7462-129">Eine durch Trennzeichen getrennte Liste gültiger virtueller Channelnamen.</span><span class="sxs-lookup"><span data-stu-id="c7462-129">A comma-separated list of valid virtual channel names.</span></span> <span data-ttu-id="c7462-130">Die Länge der einzelnen Namen in dieser Liste kann mindestens eins und maximal sieben alphabetischer Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="c7462-130">The length of each name in this list can be a minimum of one and a maximum of seven alphabetical characters.</span></span> <span data-ttu-id="c7462-131">Die Länge der gesamten Zeichenfolge kann mindestens eins und maximal 300 alphabetischer Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="c7462-131">The length of the entire string can be a minimum of one and a maximum of 300 alphabetical characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7462-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7462-132">Return value</span></span>

<span data-ttu-id="c7462-133">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c7462-133">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="c7462-134">Gibt **E \_ invalidArg** zurück, wenn der übergebenen Parameter nicht die angegebenen Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="c7462-134">Returns **E\_INVALIDARG** if the parameter that is passed does not meet the criteria that is specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7462-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7462-135">Remarks</span></span>

<span data-ttu-id="c7462-136">Rufen Sie diese Methode auf, bevor Sie die [**Connect**](imstscax-connect.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c7462-136">Call this method before calling the [**Connect**](imstscax-connect.md) method.</span></span>

<span data-ttu-id="c7462-137">Informationen zu Benennungs Einschränkungen für virtuelle Kanäle finden Sie unter [Virtual Channel Client-Registrierung](virtual-channel-client-registration.md) .</span><span class="sxs-lookup"><span data-stu-id="c7462-137">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="c7462-138">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c7462-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7462-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7462-139">Requirements</span></span>



| <span data-ttu-id="c7462-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7462-140">Requirement</span></span> | <span data-ttu-id="c7462-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c7462-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7462-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7462-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c7462-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7462-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c7462-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7462-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c7462-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7462-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c7462-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c7462-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7462-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7462-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7462-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c7462-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7462-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7462-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7462-150">IID</span><span class="sxs-lookup"><span data-stu-id="c7462-150">IID</span></span><br/>                      | <span data-ttu-id="c7462-151">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="c7462-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c7462-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7462-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7462-153">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="c7462-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c7462-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c7462-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c7462-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c7462-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c7462-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c7462-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c7462-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c7462-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c7462-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c7462-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c7462-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c7462-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c7462-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c7462-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c7462-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c7462-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c7462-162">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="c7462-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





