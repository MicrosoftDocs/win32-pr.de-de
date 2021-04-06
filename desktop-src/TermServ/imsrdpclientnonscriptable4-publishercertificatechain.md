---
title: IMsRdpClientNonScriptable4 publishercertificatechain (Eigenschaft)
description: Steuert die Herausgeber Zertifikat Kette. Die Kette wird in einer Variante vom Typ VT \_ ByRef gespeichert, die einen Zeiger auf eine Struktur der Zertifikat \_ Ketten \_ Kontext enthält. Weitere Informationen zu VT \_ -ByRef-Strukturen finden Sie unter Variant und VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Publishercertificatechain-Eigenschaft Remotedesktopdienste
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, publishercertificatechain (Eigenschaft)
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, publishercertificatechain (Eigenschaft)
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
- Publishercertificatechain-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, publishercertificatechain-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859034"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a><span data-ttu-id="53448-118">IMsRdpClientNonScriptable4::P ublishercertificatechain-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="53448-118">IMsRdpClientNonScriptable4::PublisherCertificateChain property</span></span>

<span data-ttu-id="53448-119">Steuert die Herausgeber Zertifikat Kette.</span><span class="sxs-lookup"><span data-stu-id="53448-119">Controls the publisher certificate chain.</span></span> <span data-ttu-id="53448-120">Die Kette wird in einer Variante vom Typ **VT \_ ByRef** gespeichert, die einen Zeiger auf eine Struktur der [**Zertifikat \_ Ketten \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) enthält.</span><span class="sxs-lookup"><span data-stu-id="53448-120">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span> <span data-ttu-id="53448-121">Weitere Informationen zu **VT- \_ ByRef** -Strukturen finden Sie unter [Variant und VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="53448-121">For information about **VT\_BYREF** structures, see [VARIANT and VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="53448-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="53448-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="53448-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="53448-123">Syntax</span></span>


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a><span data-ttu-id="53448-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="53448-124">Property value</span></span>

<span data-ttu-id="53448-125">Legt die Herausgeber Zertifikat Kette fest.</span><span class="sxs-lookup"><span data-stu-id="53448-125">Sets the publisher certificate chain.</span></span> <span data-ttu-id="53448-126">Die Kette wird in einer Variante vom Typ **VT \_ ByRef** gespeichert, die einen Zeiger auf eine Struktur der [**Zertifikat \_ Ketten \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) enthält.</span><span class="sxs-lookup"><span data-stu-id="53448-126">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="53448-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="53448-127">Error codes</span></span>

<span data-ttu-id="53448-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="53448-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="53448-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53448-129">Requirements</span></span>



| <span data-ttu-id="53448-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53448-130">Requirement</span></span> | <span data-ttu-id="53448-131">Wert</span><span class="sxs-lookup"><span data-stu-id="53448-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="53448-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53448-132">Minimum supported client</span></span><br/> | <span data-ttu-id="53448-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53448-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="53448-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53448-134">Minimum supported server</span></span><br/> | <span data-ttu-id="53448-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53448-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="53448-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="53448-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="53448-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53448-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="53448-138">DLL</span><span class="sxs-lookup"><span data-stu-id="53448-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53448-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53448-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="53448-140">IID</span><span class="sxs-lookup"><span data-stu-id="53448-140">IID</span></span><br/>                      | <span data-ttu-id="53448-141">IMsRdpClientNonScriptable4 ist als f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb definiert.</span><span class="sxs-lookup"><span data-stu-id="53448-141">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53448-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53448-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53448-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="53448-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="53448-144">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="53448-144">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

