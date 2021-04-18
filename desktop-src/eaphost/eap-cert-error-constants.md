---
title: EAP- \_ CERT-Fehler Konstanten (EAPHost RoR. h)
description: Definieren von Zertifikat bezogenen Fehlern, die allen EAPHost-API-Technologien gemeinsam sind.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517516"
---
# <a name="eap_cert-error-constants"></a><span data-ttu-id="ffb03-103">EAP- \_ CERT-Fehler Konstanten</span><span class="sxs-lookup"><span data-stu-id="ffb03-103">EAP\_CERT Error Constants</span></span>

<span data-ttu-id="ffb03-104">Diese Konstanten definieren Zertifikat bezogene Fehler, die allen EAPHost-API-Technologien gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="ffb03-104">These constants define certificate-related errors common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="ffb03-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP- \_ Zertifikat \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="ffb03-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-106">0x0</span><span class="sxs-lookup"><span data-stu-id="ffb03-106">0x0</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-107">Definiert die Grenze von Fehlerberichten. ein beliebiger Zertifikat Fehler tritt zwischen dem **\_ EAP-Zertifikat \_ \_ zuerst** und dem **\_ EAP \_ \_**-Zertifikat auf.</span><span class="sxs-lookup"><span data-stu-id="ffb03-107">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP- \_ Zertifikat \_ zuletzt**</span><span class="sxs-lookup"><span data-stu-id="ffb03-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-109">0xF</span><span class="sxs-lookup"><span data-stu-id="ffb03-109">0xF</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-110">Definiert die Grenze von Fehlerberichten. ein beliebiger Zertifikat Fehler tritt zwischen dem **\_ EAP-Zertifikat \_ \_ zuerst** und dem **\_ EAP \_ \_**-Zertifikat auf.</span><span class="sxs-lookup"><span data-stu-id="ffb03-110">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP- \_ Zertifikat wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="ffb03-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-112">0x1</span><span class="sxs-lookup"><span data-stu-id="ffb03-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-113">Es wurde kein Benutzerzertifikat gefunden.</span><span class="sxs-lookup"><span data-stu-id="ffb03-113">No user certificate was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP- \_ Zertifikat \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="ffb03-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-115">0x2</span><span class="sxs-lookup"><span data-stu-id="ffb03-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-116">Das Benutzerzertifikat ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ffb03-116">The user certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP- \_ Zertifikat \_ abgelaufen**</span><span class="sxs-lookup"><span data-stu-id="ffb03-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-118">0x3</span><span class="sxs-lookup"><span data-stu-id="ffb03-118">0x3</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-119">Das Benutzerzertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ffb03-119">The user certificate has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP- \_ Zertifikat gesperrt \_**</span><span class="sxs-lookup"><span data-stu-id="ffb03-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-121">0x4</span><span class="sxs-lookup"><span data-stu-id="ffb03-121">0x4</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-122">Das Benutzerzertifikat wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="ffb03-122">The user certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_anderer EAP- \_ CERT- \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ffb03-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-124">0x5</span><span class="sxs-lookup"><span data-stu-id="ffb03-124">0x5</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-125">Unbekannter Zertifikat bezogener Fehler.</span><span class="sxs-lookup"><span data-stu-id="ffb03-125">There is an unknown certificate related error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP- \_ Zertifikat \_ abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="ffb03-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP\_CERT\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-127">0x6</span><span class="sxs-lookup"><span data-stu-id="ffb03-127">0x6</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-128">Das Benutzerzertifikat wurde zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="ffb03-128">The user certificate was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP- \_ Zertifikat \_ Name \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ffb03-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-130">0x7</span><span class="sxs-lookup"><span data-stu-id="ffb03-130">0x7</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-131">Das Benutzerzertifikat erfordert einen Namen.</span><span class="sxs-lookup"><span data-stu-id="ffb03-131">The user certificate requires a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP ( \_ Allgemein) \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="ffb03-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP\_GENERAL\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-133">0x10</span><span class="sxs-lookup"><span data-stu-id="ffb03-133">0x10</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-134">Definiert die Grenze von Fehlerberichten. alle allgemeinen EAP-Fehler treten zwischen **\_ EAP \_ General \_ First** und **\_ EAP \_ General \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="ffb03-134">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffb03-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP \_ Allgemein (allgemein) \_**</span><span class="sxs-lookup"><span data-stu-id="ffb03-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP\_GENERAL\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffb03-136">0x3F</span><span class="sxs-lookup"><span data-stu-id="ffb03-136">0x3F</span></span>
</dt> <dt>



<span data-ttu-id="ffb03-137">Definiert die Grenze von Fehlerberichten. alle allgemeinen EAP-Fehler treten zwischen **\_ EAP \_ General \_ First** und **\_ EAP \_ General \_ Last** auf.</span><span class="sxs-lookup"><span data-stu-id="ffb03-137">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffb03-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffb03-138">Requirements</span></span>



| <span data-ttu-id="ffb03-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffb03-139">Requirement</span></span> | <span data-ttu-id="ffb03-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ffb03-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb03-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffb03-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb03-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffb03-142">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ffb03-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffb03-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb03-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffb03-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ffb03-145">Header</span><span class="sxs-lookup"><span data-stu-id="ffb03-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffb03-146"><dt>EAPHost RoR. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb03-146"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb03-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffb03-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb03-148">Allgemeine EAPHost-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ffb03-148">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

 





