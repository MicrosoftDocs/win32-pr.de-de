---
title: IMsRdpClientNonScriptable4-Eigenschaft "Treuhänder-OneSite"
description: Gibt an, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites auf dem Client Computer des Benutzers enthalten ist.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
- Eigenschaft "Treuhänder-OneSite" Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, Eigenschaft "Treuhänder-OneSite"
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392029"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a><span data-ttu-id="71255-116">IMsRdpClientNonScriptable4:: treuhändzonesite-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="71255-116">IMsRdpClientNonScriptable4::TrustedZoneSite property</span></span>

<span data-ttu-id="71255-117">Gibt an, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites auf dem Client Computer des Benutzers enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="71255-117">Specifies whether the website from which the user launched the connection is in the trusted sites list of the user's client computer.</span></span>

<span data-ttu-id="71255-118">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="71255-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="71255-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="71255-119">Syntax</span></span>


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a><span data-ttu-id="71255-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="71255-120">Property value</span></span>

<span data-ttu-id="71255-121">Legt die Eigenschaft "Treuhänder-OneSite" fest.</span><span class="sxs-lookup"><span data-stu-id="71255-121">Sets the TrustedZoneSite property.</span></span> <span data-ttu-id="71255-122">Diese Methode wirkt sich nicht darauf aus, ob die Website, von der der Benutzer die Verbindung gestartet hat, in der Liste der vertrauenswürdigen Sites des Client Computers enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="71255-122">This method has no effect on whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71255-123">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="71255-123">Error codes</span></span>

<span data-ttu-id="71255-124">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="71255-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="71255-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71255-125">Requirements</span></span>



| <span data-ttu-id="71255-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71255-126">Requirement</span></span> | <span data-ttu-id="71255-127">Wert</span><span class="sxs-lookup"><span data-stu-id="71255-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71255-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71255-128">Minimum supported client</span></span><br/> | <span data-ttu-id="71255-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71255-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="71255-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71255-130">Minimum supported server</span></span><br/> | <span data-ttu-id="71255-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71255-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="71255-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="71255-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="71255-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71255-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="71255-134">DLL</span><span class="sxs-lookup"><span data-stu-id="71255-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71255-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71255-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="71255-136">IID</span><span class="sxs-lookup"><span data-stu-id="71255-136">IID</span></span><br/>                      | <span data-ttu-id="71255-137">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="71255-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71255-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71255-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71255-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="71255-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="71255-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="71255-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





