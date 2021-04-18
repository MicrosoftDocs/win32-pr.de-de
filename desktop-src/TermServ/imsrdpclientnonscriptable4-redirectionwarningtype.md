---
title: IMsRdpClientNonScriptable4 redirectionwarningtype (Eigenschaft)
description: Steuert das vorhanden sein und die Darstellung des Dialog Felds, in dem der Benutzer über die Umleitung benachrichtigt wird.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
- Redirectionwarningtype-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9 Object Remotedesktopdienste, Eigenschaft redirectionwarningtype
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341396"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a><span data-ttu-id="a666e-116">IMsRdpClientNonScriptable4:: redirectionwarningtype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a666e-116">IMsRdpClientNonScriptable4::RedirectionWarningType property</span></span>

<span data-ttu-id="a666e-117">Steuert das vorhanden sein und die Darstellung des Dialog Felds, in dem der Benutzer über die Umleitung benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="a666e-117">Controls the presence and appearance of the dialog box that notifies the user about redirection.</span></span>

<span data-ttu-id="a666e-118">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a666e-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a666e-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="a666e-119">Syntax</span></span>


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a><span data-ttu-id="a666e-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a666e-120">Property value</span></span>

<span data-ttu-id="a666e-121">Legt den Typ des Dialog Felds fest, in dem der Benutzer über eine Umleitung benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="a666e-121">Sets the type of the dialog box that notifies the user of redirection.</span></span>

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span data-ttu-id="a666e-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**Redirectionwarningtypedefault** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="a666e-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="a666e-123">Das Dialogfeld ist nicht Herausgeber spezifisch.</span><span class="sxs-lookup"><span data-stu-id="a666e-123">The dialog box is not publisher specific.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span data-ttu-id="a666e-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**Redirectionwarningtypeunsigned** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="a666e-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="a666e-125">Das Dialogfeld ist für nicht signierte Dateien.</span><span class="sxs-lookup"><span data-stu-id="a666e-125">The dialog box is for unsigned files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span data-ttu-id="a666e-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**Redirectionwarningtypeunknown** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="a666e-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="a666e-127">Das Dialogfeld ist für einen unbekannten Verleger vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="a666e-127">The dialog box is for an unknown publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span data-ttu-id="a666e-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**Redirectionwarningtypeuser** (0x0003)</span><span class="sxs-lookup"><span data-stu-id="a666e-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span></span>


</dt> <dd>

<span data-ttu-id="a666e-129">Das Dialogfeld ist für die Dateien des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a666e-129">The dialog box is for the user's files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span data-ttu-id="a666e-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**Redirectionwarningtypethirdpartysigned** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="a666e-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span></span>


</dt> <dd>

<span data-ttu-id="a666e-131">Das Dialogfeld wird für Drittanbieter-zertifizierte signierte Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a666e-131">The dialog box is displayed for third-party-certified, signed files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span data-ttu-id="a666e-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**Redirectionwarningtypetrusted** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="a666e-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="a666e-133">Das Dialogfeld wird nicht angezeigt, da die Anwendung von einem vertrauenswürdigen Herausgeber veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="a666e-133">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span data-ttu-id="a666e-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**Redirectionwarningtypemax** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="a666e-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="a666e-135">Das Dialogfeld wird nicht angezeigt, da die Anwendung von einem vertrauenswürdigen Herausgeber veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="a666e-135">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="a666e-136">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a666e-136">Error codes</span></span>

<span data-ttu-id="a666e-137">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a666e-137">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a666e-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a666e-138">Remarks</span></span>

<span data-ttu-id="a666e-139">Der Wert **redirectionwarningtypedefault**, bei dem es sich um den Standardwert dieser Eigenschaft handelt, wirkt sich nicht auf das Dialogfeld aus.</span><span class="sxs-lookup"><span data-stu-id="a666e-139">The value **RedirectionWarningTypeDefault**, which is the default value of this property, exerts no control over the dialog box.</span></span> <span data-ttu-id="a666e-140">Die steuernde Eigenschaft ist in diesem Fall " [**showredirectionwarningdialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) " in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span><span class="sxs-lookup"><span data-stu-id="a666e-140">The controlling property in this case is [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a666e-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a666e-141">Requirements</span></span>



| <span data-ttu-id="a666e-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a666e-142">Requirement</span></span> | <span data-ttu-id="a666e-143">Wert</span><span class="sxs-lookup"><span data-stu-id="a666e-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a666e-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a666e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a666e-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a666e-145">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a666e-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a666e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a666e-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a666e-147">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a666e-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a666e-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="a666e-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a666e-149"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a666e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a666e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a666e-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a666e-151"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a666e-152">IID</span><span class="sxs-lookup"><span data-stu-id="a666e-152">IID</span></span><br/>                      | <span data-ttu-id="a666e-153">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="a666e-153">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a666e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a666e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a666e-155">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a666e-155">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="a666e-156">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a666e-156">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





