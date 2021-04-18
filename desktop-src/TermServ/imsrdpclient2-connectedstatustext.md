---
title: IMsRdpClient2 connectedstatustext-Eigenschaft
description: Enthält den Text, der im Client Bereich des-Steuer Elements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- Connectedstatustext-Eigenschaft Remotedesktopdienste
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
- Connectedstatustext-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, connectedstatustext-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339317"
---
# <a name="imsrdpclient2connectedstatustext-property"></a><span data-ttu-id="e5899-122">IMsRdpClient2:: connectedstatustext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e5899-122">IMsRdpClient2::ConnectedStatusText property</span></span>

<span data-ttu-id="e5899-123">Enthält den Text, der im Client Bereich des-Steuer Elements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e5899-123">Contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

<span data-ttu-id="e5899-124">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e5899-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5899-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5899-125">Syntax</span></span>


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a><span data-ttu-id="e5899-126">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e5899-126">Property value</span></span>

<span data-ttu-id="e5899-127">Die **connectedstatustext** -Eigenschaft enthält den Text, der im Client Bereich des Steuer Elements angezeigt wird, während sich das Steuerelement im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e5899-127">The **ConnectedStatusText** property contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5899-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e5899-128">Error codes</span></span>

<span data-ttu-id="e5899-129">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e5899-129">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5899-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5899-130">Remarks</span></span>

<span data-ttu-id="e5899-131">Text, der im Client Bereich des Steuer Elements angezeigt werden soll, wenn sich das Steuerelement im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="e5899-131">Text to display in the client area of the control while the control is in the connected state.</span></span> <span data-ttu-id="e5899-132">Dies ist der Text, der sichtbar ist, z. b. wenn der Benutzer das Steuerelement in einen Webbrowser in den Vollbildmodus wechselt, ein Szenario, in dem ein Teil des Steuer Elements im Browser gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="e5899-132">This is the text that is visible, for example, when the user switches the control to the full-screen mode in a web browser, a scenario that leaves a portion of the control hosted in the browser.</span></span>

<span data-ttu-id="e5899-133">Die **get \_ connectedstatustext** -Methode ordnet den für den Puffer erforderlichen Arbeitsspeicher zu, auf den der *pconnectedstatustext* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="e5899-133">The **get\_ConnectedStatusText** method allocates the memory required for the buffer pointed to by the *pConnectedStatusText* parameter.</span></span> <span data-ttu-id="e5899-134">Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5899-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="e5899-135">Dies ist für Visual Basic-und Skript Clients nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e5899-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="e5899-136">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e5899-136">This property cannot be set when the control is connected.</span></span> <span data-ttu-id="e5899-137">Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie die [**\_ verbundene imstscax:: Get**](imstscax-connected.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e5899-137">You can check if the control is connected by calling the [**IMsTscAx::get\_Connected**](imstscax-connected.md) method.</span></span>

<span data-ttu-id="e5899-138">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e5899-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5899-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5899-139">Requirements</span></span>



| <span data-ttu-id="e5899-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5899-140">Requirement</span></span> | <span data-ttu-id="e5899-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e5899-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5899-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5899-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e5899-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5899-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e5899-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5899-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e5899-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5899-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e5899-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e5899-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5899-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5899-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5899-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e5899-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5899-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5899-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5899-150">IID</span><span class="sxs-lookup"><span data-stu-id="e5899-150">IID</span></span><br/>                      | <span data-ttu-id="e5899-151">IID \_ IMsRdpClient2 ist als e7e17dc4-3b71-4ba7-a8e6-281ffadca28f definiert.</span><span class="sxs-lookup"><span data-stu-id="e5899-151">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e5899-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5899-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5899-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e5899-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e5899-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e5899-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e5899-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e5899-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e5899-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e5899-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e5899-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e5899-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e5899-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e5899-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e5899-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e5899-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e5899-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e5899-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e5899-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e5899-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

