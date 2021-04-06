---
title: IMsRdpClientNonScriptable3 redirectdynamicdrives (Eigenschaft)
description: Gibt an, ob dynamisch angefügte Plug & Play (PNP) Laufwerke, die während einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind, oder ruft Sie ab.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
- Redirectdynamicdrives-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, redirectdynamicdrives (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743648"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a><span data-ttu-id="40afa-120">IMsRdpClientNonScriptable3:: redirectdynamicdrives (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="40afa-120">IMsRdpClientNonScriptable3::RedirectDynamicDrives property</span></span>

<span data-ttu-id="40afa-121">Gibt an, ob dynamisch angefügte Plug & Play (PNP) Laufwerke, die während einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="40afa-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) drives that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="40afa-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="40afa-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="40afa-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="40afa-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a><span data-ttu-id="40afa-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="40afa-124">Property value</span></span>

<span data-ttu-id="40afa-125">Gibt an, ob dynamisch angefügte PNP-Laufwerke, die in einer Sitzung aufgelistet sind, für die Umleitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="40afa-125">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="40afa-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40afa-126">Requirements</span></span>



| <span data-ttu-id="40afa-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40afa-127">Requirement</span></span> | <span data-ttu-id="40afa-128">Wert</span><span class="sxs-lookup"><span data-stu-id="40afa-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40afa-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40afa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40afa-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40afa-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="40afa-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40afa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40afa-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40afa-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="40afa-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="40afa-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="40afa-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40afa-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="40afa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="40afa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40afa-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40afa-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="40afa-137">IID</span><span class="sxs-lookup"><span data-stu-id="40afa-137">IID</span></span><br/>                      | <span data-ttu-id="40afa-138">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="40afa-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40afa-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40afa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40afa-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="40afa-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="40afa-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="40afa-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="40afa-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="40afa-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





