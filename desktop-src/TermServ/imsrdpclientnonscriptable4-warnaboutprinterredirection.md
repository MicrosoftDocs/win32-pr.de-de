---
title: IMsRdpClientNonScriptable4 warnaboutprinterredirect (Eigenschaft)
description: Steuert, ob im Dialogfeld Umleitung eine Meldung zur Drucker Umleitung angezeigt wird, bevor eine Sitzung gestartet wird.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, warnaboutprinterredirect (Eigenschaft)
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, warnaboutprinterredirect (Eigenschaft)
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
- Warnaboutprinterredirect-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, warnaboutprinterredirect-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340807"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a><span data-ttu-id="01771-116">IMsRdpClientNonScriptable4:: warnaboutprinterredirect-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="01771-116">IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection property</span></span>

<span data-ttu-id="01771-117">Steuert, ob im Dialogfeld Umleitung eine Meldung zur Drucker Umleitung angezeigt wird, bevor eine Sitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="01771-117">Controls whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span>

<span data-ttu-id="01771-118">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="01771-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="01771-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="01771-119">Syntax</span></span>


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="01771-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="01771-120">Property value</span></span>

<span data-ttu-id="01771-121">Legt fest, ob im Dialogfeld Umleitung eine Meldung zur Drucker Umleitung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="01771-121">Sets whether the redirection dialog box displays a message about printer redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01771-122">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="01771-122">Error codes</span></span>

<span data-ttu-id="01771-123">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="01771-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="01771-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01771-124">Requirements</span></span>



| <span data-ttu-id="01771-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01771-125">Requirement</span></span> | <span data-ttu-id="01771-126">Wert</span><span class="sxs-lookup"><span data-stu-id="01771-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01771-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01771-127">Minimum supported client</span></span><br/> | <span data-ttu-id="01771-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01771-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="01771-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01771-129">Minimum supported server</span></span><br/> | <span data-ttu-id="01771-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01771-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="01771-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="01771-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="01771-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01771-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="01771-133">DLL</span><span class="sxs-lookup"><span data-stu-id="01771-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01771-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01771-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="01771-135">IID</span><span class="sxs-lookup"><span data-stu-id="01771-135">IID</span></span><br/>                      | <span data-ttu-id="01771-136">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="01771-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01771-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01771-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01771-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="01771-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="01771-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="01771-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





