---
title: Imsrdpclient extendeddisconnecverrat (Eigenschaft)
description: Enthält erweiterte Informationen über den Grund für die Trennung der Verbindung.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
- Extendeddisconnecverrat-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, extendeddisconnecverrat (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518839"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a><span data-ttu-id="2990a-124">Imsrdpclient:: extendeddisconnecverrat (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2990a-124">IMsRdpClient::ExtendedDisconnectReason property</span></span>

<span data-ttu-id="2990a-125">Enthält erweiterte Informationen über den Grund für die Trennung der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="2990a-125">Contains extended information about the control's reason for disconnection.</span></span>

<span data-ttu-id="2990a-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2990a-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2990a-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="2990a-127">Syntax</span></span>


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a><span data-ttu-id="2990a-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2990a-128">Property value</span></span>

<span data-ttu-id="2990a-129">Ein Zeiger auf den [**extendeddisconnecweroncode**](extendeddisconnectreasoncode.md) -Wert, der den Grund für die Trennung der Verbindung des Clients angibt.</span><span class="sxs-lookup"><span data-stu-id="2990a-129">Pointer to the [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) value indicating the reason for disconnection of the client.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2990a-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2990a-130">Error codes</span></span>

<span data-ttu-id="2990a-131">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2990a-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="2990a-132">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2990a-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="2990a-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2990a-133">Remarks</span></span>

<span data-ttu-id="2990a-134">In der Regel wird diese Methode im [**imstscaxevents:: ongetrennte**](imstscaxevents-ondisconnected.md) -Ereignishandler aufgerufen, um zusätzliche Informationen über das Ereignis zum Trennen der Verbindung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2990a-134">Typically this method is called in the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) event handler to retrieve additional information about the disconnection event.</span></span>

<span data-ttu-id="2990a-135">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2990a-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2990a-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2990a-136">Requirements</span></span>



| <span data-ttu-id="2990a-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2990a-137">Requirement</span></span> | <span data-ttu-id="2990a-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2990a-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2990a-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2990a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2990a-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2990a-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2990a-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2990a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2990a-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2990a-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2990a-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2990a-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="2990a-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2990a-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2990a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2990a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2990a-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2990a-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2990a-147">IID</span><span class="sxs-lookup"><span data-stu-id="2990a-147">IID</span></span><br/>                      | <span data-ttu-id="2990a-148">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="2990a-148">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2990a-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2990a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2990a-150">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="2990a-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="2990a-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="2990a-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="2990a-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="2990a-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="2990a-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="2990a-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="2990a-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="2990a-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="2990a-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="2990a-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="2990a-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2990a-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2990a-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2990a-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2990a-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2990a-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2990a-159">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="2990a-159">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="2990a-160">**Imstscaxevents:: ongetrennte**</span><span class="sxs-lookup"><span data-stu-id="2990a-160">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





