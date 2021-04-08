---
title: Imstscax-Server Eigenschaft (asptlb. h)
description: Gibt den Namen des Servers an, mit dem das aktuelle Steuerelement verbunden ist.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Server Eigenschaft
- Server Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Server Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949499"
---
# <a name="imstscaxserver-property"></a><span data-ttu-id="6b538-124">Imstscax:: Server-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6b538-124">IMsTscAx::Server property</span></span>

<span data-ttu-id="6b538-125">Gibt den Namen des Servers an, mit dem das aktuelle Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6b538-125">Specifies the name of the server to which the current control is connected.</span></span>

<span data-ttu-id="6b538-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6b538-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b538-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b538-127">Syntax</span></span>


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a><span data-ttu-id="6b538-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6b538-128">Property value</span></span>

<span data-ttu-id="6b538-129">Der Name des neuen Servers.</span><span class="sxs-lookup"><span data-stu-id="6b538-129">The new server name.</span></span> <span data-ttu-id="6b538-130">Dieser Parameter kann ein DNS-Name oder eine IP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="6b538-130">This parameter can be a DNS name or IP address.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b538-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6b538-131">Error codes</span></span>

<span data-ttu-id="6b538-132">Wenn die Methoden erfolgreich sind, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b538-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="6b538-133">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6b538-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b538-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b538-134">Remarks</span></span>

<span data-ttu-id="6b538-135">Diese Eigenschaft muss festgelegt werden, bevor die [**Connect**](imstscax-connect.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6b538-135">This property must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="6b538-136">Es ist die einzige Eigenschaft, die vor dem Herstellen einer Verbindung festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="6b538-136">It is the only property that must be set before connecting.</span></span>

<span data-ttu-id="6b538-137">Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="6b538-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="6b538-138">Diese Eigenschaft gibt **E \_ Fail** zurück, wenn Sie aufgerufen wird, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6b538-138">This property returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="6b538-139">Mithilfe der [**verbundenen**](imstscax-connected.md) Eigenschaft können Sie den Status "verbunden" überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6b538-139">You can check for the connected state by using the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="6b538-140">Mit dieser Methode wird der erforderliche Arbeitsspeicher für den Puffer zugewiesen, auf den der *pserver* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="6b538-140">This method allocates the memory required for the buffer pointed to by the *pServer* parameter.</span></span> <span data-ttu-id="6b538-141">Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6b538-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="6b538-142">Dies ist für Visual Basic-und Skript Clients nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6b538-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="6b538-143">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6b538-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b538-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b538-144">Requirements</span></span>



| <span data-ttu-id="6b538-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b538-145">Requirement</span></span> | <span data-ttu-id="6b538-146">Wert</span><span class="sxs-lookup"><span data-stu-id="6b538-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b538-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b538-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6b538-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b538-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6b538-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b538-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6b538-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b538-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6b538-151">Header</span><span class="sxs-lookup"><span data-stu-id="6b538-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b538-152"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b538-152"><dt>Asptlb.h</dt></span></span> </dl>    |
| <span data-ttu-id="6b538-153">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6b538-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b538-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b538-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b538-155">DLL</span><span class="sxs-lookup"><span data-stu-id="6b538-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b538-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b538-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b538-157">IID</span><span class="sxs-lookup"><span data-stu-id="6b538-157">IID</span></span><br/>                      | <span data-ttu-id="6b538-158">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="6b538-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6b538-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b538-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b538-160">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="6b538-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="6b538-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="6b538-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="6b538-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="6b538-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="6b538-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="6b538-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="6b538-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="6b538-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="6b538-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="6b538-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="6b538-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6b538-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6b538-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6b538-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6b538-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6b538-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6b538-169">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="6b538-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

