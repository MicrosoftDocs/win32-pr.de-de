---
title: Verbundene imstscax-Eigenschaft ("tvirtualchannels. h")
description: Ruft den Verbindungsstatus des aktuellen Steuer Elements ab.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Verbundene Eigenschaften Remotedesktopdienste
- Verbundene Eigenschaften Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
- Verbundene Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, verbundene Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339603"
---
# <a name="imstscaxconnected-property"></a><span data-ttu-id="55d07-124">Imstscax:: Connected-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55d07-124">IMsTscAx::Connected property</span></span>

<span data-ttu-id="55d07-125">Ruft den Verbindungsstatus des aktuellen Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="55d07-125">Retrieves the connection state of the current control.</span></span>

<span data-ttu-id="55d07-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="55d07-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d07-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="55d07-127">Syntax</span></span>


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a><span data-ttu-id="55d07-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="55d07-128">Property value</span></span>

<span data-ttu-id="55d07-129">Gibt den Verbindungsstatus des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="55d07-129">Indicates the connection state of the control.</span></span> <span data-ttu-id="55d07-130">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="55d07-130">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="55d07-131">0</span><span class="sxs-lookup"><span data-stu-id="55d07-131">0</span></span>
</dt> <dd>

<span data-ttu-id="55d07-132">Das Steuerelement ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="55d07-132">The control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="55d07-133">1</span><span class="sxs-lookup"><span data-stu-id="55d07-133">1</span></span>
</dt> <dd>

<span data-ttu-id="55d07-134">Das Steuerelement ist verbunden.</span><span class="sxs-lookup"><span data-stu-id="55d07-134">The control is connected.</span></span>

</dd> <dt>

<span data-ttu-id="55d07-135">2</span><span class="sxs-lookup"><span data-stu-id="55d07-135">2</span></span>
</dt> <dd>

<span data-ttu-id="55d07-136">Das-Steuerelement stellt eine Verbindung her.</span><span class="sxs-lookup"><span data-stu-id="55d07-136">The control is establishing a connection.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="55d07-137">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="55d07-137">Error codes</span></span>

<span data-ttu-id="55d07-138">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="55d07-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d07-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55d07-139">Remarks</span></span>

<span data-ttu-id="55d07-140">Die bevorzugte Methode zum Ermitteln des Verbindungs Zustands des Steuer Elements besteht darin, auf die Verbindungs Ereignisse in [**imstscaxevents**](imstscaxevents-interface.md)zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="55d07-140">The preferred way to determine the control's connection state is to respond to the connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span></span>

<span data-ttu-id="55d07-141">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="55d07-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55d07-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55d07-142">Requirements</span></span>



| <span data-ttu-id="55d07-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55d07-143">Requirement</span></span> | <span data-ttu-id="55d07-144">Wert</span><span class="sxs-lookup"><span data-stu-id="55d07-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d07-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55d07-145">Minimum supported client</span></span><br/> | <span data-ttu-id="55d07-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55d07-146">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="55d07-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55d07-147">Minimum supported server</span></span><br/> | <span data-ttu-id="55d07-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55d07-148">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="55d07-149">Header</span><span class="sxs-lookup"><span data-stu-id="55d07-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d07-150"><dt>"Tvirtualchannels. h"</dt></span><span class="sxs-lookup"><span data-stu-id="55d07-150"><dt>Tsvirtualchannels.h</dt></span></span> </dl> |
| <span data-ttu-id="55d07-151">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="55d07-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="55d07-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d07-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="55d07-153">DLL</span><span class="sxs-lookup"><span data-stu-id="55d07-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55d07-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d07-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="55d07-155">IID</span><span class="sxs-lookup"><span data-stu-id="55d07-155">IID</span></span><br/>                      | <span data-ttu-id="55d07-156">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="55d07-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="55d07-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55d07-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d07-158">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="55d07-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="55d07-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="55d07-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="55d07-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="55d07-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="55d07-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="55d07-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="55d07-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="55d07-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="55d07-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="55d07-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="55d07-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="55d07-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="55d07-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="55d07-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="55d07-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="55d07-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="55d07-167">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="55d07-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





