---
title: IMsRdpClientNonScriptable3 connectionbartext-Eigenschaft
description: Legt den Text zum Aktualisieren der Verbindungs Leiste fest oder ruft ihn ab.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Connectionbartext-Eigenschaft Remotedesktopdienste
- Connectionbartext-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, connectionbartext-Eigenschaft
- Connectionbartext-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, connectionbartext-Eigenschaft
- Connectionbartext-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, connectionbartext-Eigenschaft
- Connectionbartext-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, connectionbartext-Eigenschaft
- Connectionbartext-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, connectionbartext-Eigenschaft
- Connectionbartext-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, connectionbartext-Eigenschaft
- Connectionbartext-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, connectionbartext-Eigenschaft
- Connectionbartext-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, connectionbartext-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743296"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a><span data-ttu-id="7eea8-120">IMsRdpClientNonScriptable3:: connectionbartext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7eea8-120">IMsRdpClientNonScriptable3::ConnectionBarText property</span></span>

<span data-ttu-id="7eea8-121">Legt den Text zum Aktualisieren der Verbindungs Leiste fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="7eea8-121">Sets or retrieves the text to update the connection bar.</span></span>

<span data-ttu-id="7eea8-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7eea8-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eea8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eea8-123">Syntax</span></span>


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a><span data-ttu-id="7eea8-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7eea8-124">Property value</span></span>

<span data-ttu-id="7eea8-125">Legt die Text Zeichenfolge fest, die auf der Verbindungs Leiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7eea8-125">Sets the text string to display on the connection bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eea8-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7eea8-126">Remarks</span></span>

<span data-ttu-id="7eea8-127">Sie müssen die **IMsRdpClientNonScriptable3::p UT \_ connectionbartext** -Methode anrufen, bevor Sie die [**imstscsecuredsettings::p UT- \_ voll Bild**](imstscsecuredsettings-fullscreen.md) Methode oder die [**imsrdpclient::p UT- \_ voll Bild**](imsrdpclient-fullscreen.md) Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7eea8-127">You must call the **IMsRdpClientNonScriptable3::put\_ConnectionBarText** method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eea8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7eea8-128">Requirements</span></span>



| <span data-ttu-id="7eea8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7eea8-129">Requirement</span></span> | <span data-ttu-id="7eea8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7eea8-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eea8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7eea8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7eea8-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eea8-132">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7eea8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7eea8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7eea8-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7eea8-134">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7eea8-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7eea8-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="7eea8-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eea8-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7eea8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7eea8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eea8-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eea8-138"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7eea8-139">IID</span><span class="sxs-lookup"><span data-stu-id="7eea8-139">IID</span></span><br/>                      | <span data-ttu-id="7eea8-140">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="7eea8-140">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7eea8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7eea8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eea8-142">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="7eea8-142">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="7eea8-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="7eea8-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="7eea8-144">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="7eea8-144">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





