---
title: IMsRdpClientNonScriptable3 redirectdynamicdevices (Eigenschaft)
description: Gibt an, ob dynamisch angefügte Plug & Play (PNP)-Geräte, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind, oder ruft Sie ab.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, Eigenschaft redirectdynamicdevices
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, Eigenschaft redirectdynamicdevices
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, Eigenschaft redirectdynamicdevices
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
- Redirectdynamicdevices-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, redirectdynamicdevices-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740400"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a><span data-ttu-id="31ea4-120">IMsRdpClientNonScriptable3:: redirectdynamicdevices (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="31ea4-120">IMsRdpClientNonScriptable3::RedirectDynamicDevices property</span></span>

<span data-ttu-id="31ea4-121">Gibt an, ob dynamisch angefügte Plug & Play (PNP)-Geräte, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="31ea4-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) devices that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="31ea4-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="31ea4-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ea4-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="31ea4-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a><span data-ttu-id="31ea4-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="31ea4-124">Property value</span></span>

<span data-ttu-id="31ea4-125">Gibt an, ob dynamisch angefügte PNP-Geräte, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="31ea4-125">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ea4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31ea4-126">Requirements</span></span>



| <span data-ttu-id="31ea4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31ea4-127">Requirement</span></span> | <span data-ttu-id="31ea4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="31ea4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ea4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31ea4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="31ea4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31ea4-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="31ea4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31ea4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="31ea4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31ea4-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="31ea4-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="31ea4-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="31ea4-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31ea4-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="31ea4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="31ea4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31ea4-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31ea4-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="31ea4-137">IID</span><span class="sxs-lookup"><span data-stu-id="31ea4-137">IID</span></span><br/>                      | <span data-ttu-id="31ea4-138">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="31ea4-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31ea4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31ea4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ea4-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="31ea4-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="31ea4-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="31ea4-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="31ea4-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="31ea4-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





