---
title: IMsRdpClientNonScriptable4 launchedviaclientshellinterface (Eigenschaft)
description: Gibt an, ob der Benutzer das Client Steuerelement über die Schnittstelle Remotedesktop Webzugriff (RD Webzugriff) gestartet hat.
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, launchedviaclientshellinterface (Eigenschaft)
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, launchedviaclientshellinterface (Eigenschaft)
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, launchedviaclientshellinterface (Eigenschaft)
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, launchedviaclientshellinterface (Eigenschaft)
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, launchedviaclientshellinterface (Eigenschaft)
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, launchedviaclientshellinterface (Eigenschaft)
- Launchedviaclientshellinterface-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, launchedviaclientshellinterface (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956672"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a><span data-ttu-id="98f46-118">IMsRdpClientNonScriptable4:: launchedviaclientshellinterface (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="98f46-118">IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface property</span></span>

<span data-ttu-id="98f46-119">Gibt an, ob der Benutzer das Client Steuerelement über die Schnittstelle Remotedesktop Webzugriff (RD Webzugriff) gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="98f46-119">Specifies whether the user launched the client control by using the Remote Desktop Web Access (RD Web Access) interface.</span></span>

<span data-ttu-id="98f46-120">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="98f46-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f46-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="98f46-121">Syntax</span></span>


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a><span data-ttu-id="98f46-122">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="98f46-122">Property value</span></span>

<span data-ttu-id="98f46-123">Legt die **launchedviaclientshellinterface** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="98f46-123">Sets the **LaunchedViaClientShellInterface** property.</span></span>

## <a name="error-codes"></a><span data-ttu-id="98f46-124">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="98f46-124">Error codes</span></span>

<span data-ttu-id="98f46-125">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="98f46-125">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f46-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98f46-126">Requirements</span></span>



| <span data-ttu-id="98f46-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98f46-127">Requirement</span></span> | <span data-ttu-id="98f46-128">Wert</span><span class="sxs-lookup"><span data-stu-id="98f46-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f46-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98f46-129">Minimum supported client</span></span><br/> | <span data-ttu-id="98f46-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98f46-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="98f46-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98f46-131">Minimum supported server</span></span><br/> | <span data-ttu-id="98f46-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98f46-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="98f46-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="98f46-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="98f46-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98f46-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="98f46-135">DLL</span><span class="sxs-lookup"><span data-stu-id="98f46-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98f46-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98f46-136"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="98f46-137">IID</span><span class="sxs-lookup"><span data-stu-id="98f46-137">IID</span></span><br/>                      | <span data-ttu-id="98f46-138">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="98f46-138">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98f46-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98f46-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f46-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="98f46-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="98f46-141">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="98f46-141">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





