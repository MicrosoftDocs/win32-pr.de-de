---
description: In der folgenden Tabelle werden alle HRESULT-Werte aufgelistet, die von den Methoden in der XPS Digital Signature-API zurückgegeben werden können.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: XPS-Fehler bei der digitalen Signatur-API (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348209"
---
# <a name="xps-digital-signature-api-errors"></a><span data-ttu-id="68e65-103">XPS-Fehler bei der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="68e65-103">XPS Digital Signature API Errors</span></span>

<span data-ttu-id="68e65-104">In der folgenden Tabelle werden alle **HRESULT** -Werte aufgelistet, die von den Methoden in der XPS Digital Signature-API zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="68e65-104">The following table lists all **HRESULT** values that can be returned by the methods in the XPS Digital Signature API.</span></span> <span data-ttu-id="68e65-105">Beachten Sie, dass nicht jede Methode jeden in dieser Tabelle aufgelisteten Rückgabewert zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="68e65-105">Note that not every method can return every return value listed in this table.</span></span>



| <span data-ttu-id="68e65-106">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="68e65-106">Return code/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="68e65-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68e65-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="68e65-108"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-108"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                                                                                 | <span data-ttu-id="68e65-109">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68e65-109">The method succeeded.</span></span><br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <span data-ttu-id="68e65-110"><dt>**XPS \_ E \_ ungültiges \_ signatureblock- \_ Markup**</dt> <dt>0x8052038b</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-110"><dt>**XPS\_E\_INVALID\_SIGNATUREBLOCK\_MARKUP**</dt> <dt>0x8052038b</dt></span></span> </dl> | <span data-ttu-id="68e65-111">Fehler im XML-Markup des Signatur Blocks beim Lesen des Signatur Markups.</span><span class="sxs-lookup"><span data-stu-id="68e65-111">Encountered an error in the XML markup of the signature block while the signature markup was being read.</span></span><br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <span data-ttu-id="68e65-112"><dt>**XPS \_ E \_ Markup \_ Kompatibilitäts \_ Elemente**</dt> <dt>0x80520389</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-112"><dt>**XPS\_E\_MARKUP\_COMPATIBILITY\_ELEMENTS**</dt> <dt>0x80520389</dt></span></span> </dl> | <span data-ttu-id="68e65-113">Der Wert für die [**XPS- \_ Signier \_ Flags**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) hat angegeben, dass keine Markup Kompatibilitäts Elemente erwartet wurden, aber es wurden Markup Kompatibilitäts Elemente gefunden.</span><span class="sxs-lookup"><span data-stu-id="68e65-113">The [**XPS\_SIGN\_FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) value specified that no markup compatibility elements were expected; however, markup compatibility elements were found.</span></span><br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <span data-ttu-id="68e65-114"><dt>**XPS \_ E- \_ Objekt \_ getrennt**</dt> <dt>0x8052038a</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-114"><dt>**XPS\_E\_OBJECT\_DETACHED**</dt> <dt>0x8052038a</dt></span></span> </dl>                                            | <span data-ttu-id="68e65-115">Die Schnittstelle ist nicht dem Signatur-Manager zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="68e65-115">The interface is not associated with the signature manager.</span></span><br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <span data-ttu-id="68e65-116"><dt>**XPS \_ E- \_ Paket \_ bereits \_ geöffnet**</dt> <dt>0x80520387</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-116"><dt>**XPS\_E\_PACKAGE\_ALREADY\_OPENED**</dt> <dt>0x80520387</dt></span></span> </dl>                      | <span data-ttu-id="68e65-117">Ein XPS-Paket wurde bereits im Signatur-Manager geöffnet.</span><span class="sxs-lookup"><span data-stu-id="68e65-117">An XPS package has already been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <span data-ttu-id="68e65-118"><dt>**XPS \_ E- \_ Paket \_ nicht \_ geöffnet**</dt> <dt>0x80520386</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-118"><dt>**XPS\_E\_PACKAGE\_NOT\_OPENED**</dt> <dt>0x80520386</dt></span></span> </dl>                                  | <span data-ttu-id="68e65-119">Ein XPS-Paket wurde noch nicht im Signatur-Manager geöffnet.</span><span class="sxs-lookup"><span data-stu-id="68e65-119">An XPS package has not yet been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <span data-ttu-id="68e65-120"><dt>**XPS \_ E \_ signatureId \_ DUP**</dt> <dt>0x80520388</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-120"><dt>**XPS\_E\_SIGNATUREID\_DUP**</dt> <dt>0x80520388</dt></span></span> </dl>                                            | <span data-ttu-id="68e65-121">Mindestens zwei Signaturen haben dieselbe ID.</span><span class="sxs-lookup"><span data-stu-id="68e65-121">Two or more signatures have the same ID.</span></span><br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <span data-ttu-id="68e65-122"><dt>**XPS \_ E \_ sigrequestid \_ DUP**</dt> <dt>0x80520385</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-122"><dt>**XPS\_E\_SIGREQUESTID\_DUP**</dt> <dt>0x80520385</dt></span></span> </dl>                                         | <span data-ttu-id="68e65-123">Die ID der Signatur Anforderung ist innerhalb des Signatur Blocks nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="68e65-123">The signature request ID is not unique within the signature block.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="68e65-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68e65-124">Remarks</span></span>

<span data-ttu-id="68e65-125">Einige Methoden der digitalen XPS-Signatur-API führen Aufrufe an die [Paketierungs](/previous-versions/windows/desktop/opc/packaging) -API aus.</span><span class="sxs-lookup"><span data-stu-id="68e65-125">Some XPS digital signature API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="68e65-126">Informationen zu den Rückgabe Werten der Packungs-API finden Sie unter [Packen von Fehlern](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="68e65-126">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="68e65-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68e65-127">Requirements</span></span>



| <span data-ttu-id="68e65-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68e65-128">Requirement</span></span> | <span data-ttu-id="68e65-129">Wert</span><span class="sxs-lookup"><span data-stu-id="68e65-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68e65-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68e65-130">Minimum supported client</span></span><br/> | <span data-ttu-id="68e65-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68e65-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="68e65-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68e65-132">Minimum supported server</span></span><br/> | <span data-ttu-id="68e65-133">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68e65-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="68e65-134">Header</span><span class="sxs-lookup"><span data-stu-id="68e65-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="68e65-135"><dt>XpsDigitalSignature. h</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-135"><dt>Xpsdigitalsignature.h</dt></span></span> </dl>   |
| <span data-ttu-id="68e65-136">IDL</span><span class="sxs-lookup"><span data-stu-id="68e65-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68e65-137"><dt>XpsDigitalSignature. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68e65-137"><dt>XpsDigitalSignature.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e65-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68e65-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e65-139">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="68e65-139">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="68e65-140">Paketfehler</span><span class="sxs-lookup"><span data-stu-id="68e65-140">Packaging Errors</span></span>](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[<span data-ttu-id="68e65-141">Kryptografierückgabetwerte</span><span class="sxs-lookup"><span data-stu-id="68e65-141">Cryptography Return Values</span></span>](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

