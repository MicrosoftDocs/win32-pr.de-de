---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 9000-11999 und ist für Entwickler bestimmt.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: System Fehler Codes (9000-11999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748377"
---
# <a name="system-error-codes-9000-11999"></a><span data-ttu-id="ba809-103">System Fehler Codes (9000-11999)</span><span class="sxs-lookup"><span data-stu-id="ba809-103">System Error Codes (9000-11999)</span></span>

> [!NOTE]
> <span data-ttu-id="ba809-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="ba809-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="ba809-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ba809-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="ba809-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 9000 bis 11999) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ba809-106">The following list describes [system error codes](system-error-codes.md) (errors 9000 to 11999).</span></span> <span data-ttu-id="ba809-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="ba809-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="ba809-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="ba809-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="ba809-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS- \_ Fehler \_ RCODE- \_ Format \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS\_ERROR\_RCODE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-110">9001 (0x2329)</span><span class="sxs-lookup"><span data-stu-id="ba809-110">9001 (0x2329)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-111">Der DNS-Server kann das Format nicht interpretieren.</span><span class="sxs-lookup"><span data-stu-id="ba809-111">DNS server unable to interpret format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS- \_ Fehler \_ RCODE- \_ Server Fehler \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS\_ERROR\_RCODE\_SERVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-113">9002 (0x232a)</span><span class="sxs-lookup"><span data-stu-id="ba809-113">9002 (0x232A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-114">DNS-Server Fehler</span><span class="sxs-lookup"><span data-stu-id="ba809-114">DNS server failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS- \_ Fehler \_ RCODE- \_ namens \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS\_ERROR\_RCODE\_NAME\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-116">9003 (0x232b)</span><span class="sxs-lookup"><span data-stu-id="ba809-116">9003 (0x232B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-117">Der DNS-Name ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-117">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS- \_ Fehler- \_ RCODE \_ nicht \_ implementiert**</span><span class="sxs-lookup"><span data-stu-id="ba809-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS\_ERROR\_RCODE\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-119">9004 (0x232c)</span><span class="sxs-lookup"><span data-stu-id="ba809-119">9004 (0x232C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-120">Die DNS-Anforderung wird vom Namen Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ba809-120">DNS request not supported by name server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS- \_ Fehler \_ RCODE wurde \_ verweigert.**</span><span class="sxs-lookup"><span data-stu-id="ba809-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS\_ERROR\_RCODE\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-122">9005 (0x232d)</span><span class="sxs-lookup"><span data-stu-id="ba809-122">9005 (0x232D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-123">Der DNS-Vorgang wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="ba809-123">DNS operation refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS- \_ Fehler \_ RCODE \_ yxdomain**</span><span class="sxs-lookup"><span data-stu-id="ba809-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS\_ERROR\_RCODE\_YXDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-125">9006 (0x232e)</span><span class="sxs-lookup"><span data-stu-id="ba809-125">9006 (0x232E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-126">Der DNS-Name, der nicht vorhanden sein sollte, ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-126">DNS name that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS- \_ Fehler \_ RCODE \_ yxrrset**</span><span class="sxs-lookup"><span data-stu-id="ba809-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS\_ERROR\_RCODE\_YXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-128">9007 (0x232f)</span><span class="sxs-lookup"><span data-stu-id="ba809-128">9007 (0x232F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-129">Der DNS-RR-Satz, der nicht vorhanden sein sollte, ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-129">DNS RR set that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS- \_ Fehler \_ RCODE \_ nxrrset**</span><span class="sxs-lookup"><span data-stu-id="ba809-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS\_ERROR\_RCODE\_NXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-131">9008 (0x2330)</span><span class="sxs-lookup"><span data-stu-id="ba809-131">9008 (0x2330)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-132">Der DNS-RR-Satz, der vorhanden sein sollte, ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-132">DNS RR set that ought to exist, does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS- \_ Fehler \_ RCODE \_ notauth**</span><span class="sxs-lookup"><span data-stu-id="ba809-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS\_ERROR\_RCODE\_NOTAUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-134">9009 (0x2331)</span><span class="sxs-lookup"><span data-stu-id="ba809-134">9009 (0x2331)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-135">DNS-Server ist für die Zone nicht autorisierend.</span><span class="sxs-lookup"><span data-stu-id="ba809-135">DNS server not authoritative for zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS- \_ Fehler \_ RCODE \_ notzone**</span><span class="sxs-lookup"><span data-stu-id="ba809-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS\_ERROR\_RCODE\_NOTZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-137">9010 (0x2332)</span><span class="sxs-lookup"><span data-stu-id="ba809-137">9010 (0x2332)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-138">Der DNS-Name in Update oder Prereq ist nicht in der Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-138">DNS name in update or prereq is not in zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS- \_ Fehler \_ RCODE \_ BadSig**</span><span class="sxs-lookup"><span data-stu-id="ba809-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS\_ERROR\_RCODE\_BADSIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-140">9016 (0x2338)</span><span class="sxs-lookup"><span data-stu-id="ba809-140">9016 (0x2338)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-141">Fehler beim Überprüfen der DNS-Signatur.</span><span class="sxs-lookup"><span data-stu-id="ba809-141">DNS signature failed to verify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS- \_ Fehler \_ RCODE \_ badkey**</span><span class="sxs-lookup"><span data-stu-id="ba809-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS\_ERROR\_RCODE\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-143">9017 (0x2339)</span><span class="sxs-lookup"><span data-stu-id="ba809-143">9017 (0x2339)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-144">Ungültiger DNS-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ba809-144">DNS bad key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS- \_ Fehler \_ RCODE \_ badtime**</span><span class="sxs-lookup"><span data-stu-id="ba809-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS\_ERROR\_RCODE\_BADTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-146">9018 (0x233a)</span><span class="sxs-lookup"><span data-stu-id="ba809-146">9018 (0x233A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-147">Gültigkeit der DNS-Signatur ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ba809-147">DNS signature validity expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS- \_ Fehler \_ keymaster \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ba809-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS\_ERROR\_KEYMASTER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-149">9101 (0x238d)</span><span class="sxs-lookup"><span data-stu-id="ba809-149">9101 (0x238D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-150">Dieser Vorgang kann nur von dem DNS-Server durchgeführt werden, der als Schlüssel Master für die Zone fungiert.</span><span class="sxs-lookup"><span data-stu-id="ba809-150">Only the DNS server acting as the key master for the zone may perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS- \_ Fehler ist \_ \_ \_ in der \_ signierten \_ Zone nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_SIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-152">9102 (0x238e)</span><span class="sxs-lookup"><span data-stu-id="ba809-152">9102 (0x238E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-153">Dieser Vorgang ist für eine signierte oder signierte Zone nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba809-153">This operation is not allowed on a zone that is signed or has signing keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS- \_ Fehler \_ NSEC3 nicht \_ kompatibel \_ mit \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="ba809-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS\_ERROR\_NSEC3\_INCOMPATIBLE\_WITH\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-155">9103 (0x238f)</span><span class="sxs-lookup"><span data-stu-id="ba809-155">9103 (0x238F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-156">NSEC3 ist nicht kompatibel mit dem RSA-SHA-1-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="ba809-156">NSEC3 is not compatible with the RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="ba809-157">Wählen Sie einen anderen Algorithmus aus, oder verwenden Sie nsec.</span><span class="sxs-lookup"><span data-stu-id="ba809-157">Choose a different algorithm or use NSEC.</span></span>

<span data-ttu-id="ba809-158">Dieser Wert wurde auch als **DNS- \_ Fehler \_ ungültig \_ NSEC3 \_ Parameter** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba809-158">This value was also named **DNS\_ERROR\_INVALID\_NSEC3\_PARAMETERS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS- \_ Fehler \_ nicht \_ genug \_ Signatur \_ Schlüssel \_ Deskriptoren**</span><span class="sxs-lookup"><span data-stu-id="ba809-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS\_ERROR\_NOT\_ENOUGH\_SIGNING\_KEY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-160">9104 (0x2390)</span><span class="sxs-lookup"><span data-stu-id="ba809-160">9104 (0x2390)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-161">Die Zone verfügt nicht über genügend Signatur Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="ba809-161">The zone does not have enough signing keys.</span></span> <span data-ttu-id="ba809-162">Es muss mindestens ein Schlüssel Signatur Schlüssel (Key Signing Key, KSK) und mindestens ein Zonen Signatur Schlüssel (ZSK) vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ba809-162">There must be at least one key signing key (KSK) and at least one zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_ \_ nicht unterstützter DNS-Fehler \_ Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="ba809-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS\_ERROR\_UNSUPPORTED\_ALGORITHM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-164">9105 (0x2391)</span><span class="sxs-lookup"><span data-stu-id="ba809-164">9105 (0x2391)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-165">Der angegebene Algorithmus wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ba809-165">The specified algorithm is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS- \_ Fehler \_ ungültige \_ Schlüssel \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="ba809-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS\_ERROR\_INVALID\_KEY\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-167">9106 (0x2392)</span><span class="sxs-lookup"><span data-stu-id="ba809-167">9106 (0x2392)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-168">Die angegebene Schlüsselgröße wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ba809-168">The specified key size is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**der DNS- \_ Fehler \_ Signatur \_ Schlüssel ist \_ nicht \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="ba809-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**DNS\_ERROR\_SIGNING\_KEY\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-170">9107 (0x2393)</span><span class="sxs-lookup"><span data-stu-id="ba809-170">9107 (0x2393)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-171">Der DNS-Server kann auf mindestens einen der Signatur Schlüssel für eine Zone nicht zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ba809-171">One or more of the signing keys for a zone are not accessible to the DNS server.</span></span> <span data-ttu-id="ba809-172">Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-172">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS- \_ Fehler \_ KSP \_ bietet \_ keine \_ Unterstützung \_ für den Schutz**</span><span class="sxs-lookup"><span data-stu-id="ba809-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS\_ERROR\_KSP\_DOES\_NOT\_SUPPORT\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-174">9108 (0x2394)</span><span class="sxs-lookup"><span data-stu-id="ba809-174">9108 (0x2394)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-175">Der angegebene Schlüsselspeicher Anbieter unterstützt nicht DPAPI + +-Datenschutz.</span><span class="sxs-lookup"><span data-stu-id="ba809-175">The specified key storage provider does not support DPAPI++ data protection.</span></span> <span data-ttu-id="ba809-176">Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-176">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**\_unerwarteter DNS-Fehler beim \_ \_ Schutz von Daten \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="ba809-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS\_ERROR\_UNEXPECTED\_DATA\_PROTECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-178">9109 (0x2395)</span><span class="sxs-lookup"><span data-stu-id="ba809-178">9109 (0x2395)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-179">Ein unerwarteter DPAPI + +-Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ba809-179">An unexpected DPAPI++ error was encountered.</span></span> <span data-ttu-id="ba809-180">Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-180">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**\_ \_ unerwarteter \_ CNG- \_ Fehler bei DNS-Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS\_ERROR\_UNEXPECTED\_CNG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-182">9110 (0x2396)</span><span class="sxs-lookup"><span data-stu-id="ba809-182">9110 (0x2396)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-183">Ein unerwarteter Kryptografiefehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ba809-183">An unexpected crypto error was encountered.</span></span> <span data-ttu-id="ba809-184">Die Zonen Signierung ist möglicherweise erst funktionstüchtig, wenn dieser Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-184">Zone signing may not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS- \_ Fehler bei \_ unbekannter \_ Signatur \_ Parameter \_ Version.**</span><span class="sxs-lookup"><span data-stu-id="ba809-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS\_ERROR\_UNKNOWN\_SIGNING\_PARAMETER\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-186">9111 (0x2397)</span><span class="sxs-lookup"><span data-stu-id="ba809-186">9111 (0x2397)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-187">Der DNS-Server hat einen Signatur Schlüssel mit einer unbekannten Version gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-187">The DNS server encountered a signing key with an unknown version.</span></span> <span data-ttu-id="ba809-188">Die Zonen Signierung ist erst dann betriebsbereit, wenn der Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-188">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS- \_ Fehler- \_ KSP \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="ba809-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS\_ERROR\_KSP\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-190">9112 (0x2398)</span><span class="sxs-lookup"><span data-stu-id="ba809-190">9112 (0x2398)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-191">Der angegebene Schlüsseldienst Anbieter kann nicht vom DNS-Server geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-191">The specified key service provider cannot be opened by the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS- \_ Fehler \_ zu \_ viele \_ SKDS**</span><span class="sxs-lookup"><span data-stu-id="ba809-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS\_ERROR\_TOO\_MANY\_SKDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-193">9113 (0x2399)</span><span class="sxs-lookup"><span data-stu-id="ba809-193">9113 (0x2399)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-194">Der DNS-Server kann keine weiteren Signatur Schlüssel mit dem angegebenen Algorithmus und dem KSK-Flagwert für diese Zone akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="ba809-194">The DNS server cannot accept any more signing keys with the specified algorithm and KSK flag value for this zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS- \_ Fehler bei \_ ungültigem \_ rolloverzeitraum \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS\_ERROR\_INVALID\_ROLLOVER\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-196">9114 (0x239a)</span><span class="sxs-lookup"><span data-stu-id="ba809-196">9114 (0x239A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-197">Der angegebene rolloverzeitraum ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ba809-197">The specified rollover period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS- \_ Fehler beim \_ \_ anfänglichen \_ rolloveroffset. \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS\_ERROR\_INVALID\_INITIAL\_ROLLOVER\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-199">9115 (0x239b)</span><span class="sxs-lookup"><span data-stu-id="ba809-199">9115 (0x239B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-200">Der angegebene anfängliche rolloveroffset ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ba809-200">The specified initial rollover offset is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS \_ - \_ fehlerrollover wird ausgeführt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS\_ERROR\_ROLLOVER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-202">9116 (0x239c)</span><span class="sxs-lookup"><span data-stu-id="ba809-202">9116 (0x239C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-203">Der angegebene Signatur Schlüssel ist bereits im Prozess des Rollbacks von Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="ba809-203">The specified signing key is already in process of rolling over keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS- \_ Fehler \_ Standby- \_ Schlüssel \_ nicht \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="ba809-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS\_ERROR\_STANDBY\_KEY\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-205">9117 (0x239d)</span><span class="sxs-lookup"><span data-stu-id="ba809-205">9117 (0x239D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-206">Der angegebene Signatur Schlüssel hat keine Standby-Taste, die widerrufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba809-206">The specified signing key does not have a standby key to revoke.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS- \_ Fehler ist \_ \_ \_ für \_ ZSK nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ZSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-208">9118 (0x239e)</span><span class="sxs-lookup"><span data-stu-id="ba809-208">9118 (0x239E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-209">Dieser Vorgang ist für einen Zonen Signatur Schlüssel (ZSK) nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba809-209">This operation is not allowed on a zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS- \_ Fehler ist \_ \_ \_ für \_ aktive \_ SKD nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ACTIVE\_SKD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-211">9119 (0x239f)</span><span class="sxs-lookup"><span data-stu-id="ba809-211">9119 (0x239F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-212">Dieser Vorgang ist für einen aktiven Signatur Schlüssel nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba809-212">This operation is not allowed on an active signing key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS \_ - \_ fehlerrollover bereits in die \_ \_ Warteschlange eingereiht**</span><span class="sxs-lookup"><span data-stu-id="ba809-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS\_ERROR\_ROLLOVER\_ALREADY\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-214">9120 (0x23a0)</span><span class="sxs-lookup"><span data-stu-id="ba809-214">9120 (0x23A0)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-215">Der angegebene Signatur Schlüssel befindet sich bereits in der Warteschlange für einen Rollover.</span><span class="sxs-lookup"><span data-stu-id="ba809-215">The specified signing key is already queued for rollover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS- \_ Fehler \_ in nicht \_ \_ \_ signierter \_ Zone nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_UNSIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-217">9121 (0x23a1)</span><span class="sxs-lookup"><span data-stu-id="ba809-217">9121 (0x23A1)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-218">Dieser Vorgang ist in einer nicht signierten Zone nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba809-218">This operation is not allowed on an unsigned zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS- \_ Fehler fehlerhafter \_ \_ keymaster**</span><span class="sxs-lookup"><span data-stu-id="ba809-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS\_ERROR\_BAD\_KEYMASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-220">9122 (0x23a2)</span><span class="sxs-lookup"><span data-stu-id="ba809-220">9122 (0x23A2)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-221">Dieser Vorgang konnte nicht abgeschlossen werden, da der DNS-Server, der als aktueller Schlüssel Master für diese Zone aufgeführt ist, nicht oder falsch konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ba809-221">This operation could not be completed because the DNS server listed as the current key master for this zone is down or misconfigured.</span></span> <span data-ttu-id="ba809-222">Beheben Sie das Problem auf dem aktuellen Schlüssel Master für diese Zone, oder verwenden Sie einen anderen DNS-Server, um die Schlüssel Master Rolle zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="ba809-222">Resolve the problem on the current key master for this zone or use another DNS server to seize the key master role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS- \_ Fehler \_ ungültige \_ Signatur \_ Gültigkeits \_ Dauer.**</span><span class="sxs-lookup"><span data-stu-id="ba809-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS\_ERROR\_INVALID\_SIGNATURE\_VALIDITY\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-224">9123 (0x23a3)</span><span class="sxs-lookup"><span data-stu-id="ba809-224">9123 (0x23A3)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-225">Der angegebene Gültigkeits Zeitraum der Signatur ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ba809-225">The specified signature validity period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS- \_ Fehler \_ ungültige \_ NSEC3 \_ iterations \_ Anzahl**</span><span class="sxs-lookup"><span data-stu-id="ba809-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS\_ERROR\_INVALID\_NSEC3\_ITERATION\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-227">9124 (0x23a4)</span><span class="sxs-lookup"><span data-stu-id="ba809-227">9124 (0x23A4)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-228">Die angegebene Anzahl von NSEC3 Iterationen ist höher als die zulässige Mindestschlüssellänge in der Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-228">The specified NSEC3 iteration count is higher than allowed by the minimum key length used in the zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS- \_ Fehler \_ DNSSEC \_ ist \_ deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ba809-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS\_ERROR\_DNSSEC\_IS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-230">9125 (0x23a5)</span><span class="sxs-lookup"><span data-stu-id="ba809-230">9125 (0x23A5)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-231">Dieser Vorgang konnte nicht abgeschlossen werden, da der DNS-Server mit deaktivierten DNSSEC-Funktionen konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-231">This operation could not be completed because the DNS server has been configured with DNSSEC features disabled.</span></span> <span data-ttu-id="ba809-232">Aktivieren Sie DNSSEC auf dem DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="ba809-232">Enable DNSSEC on the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS- \_ Fehler \_ ungültiges \_ XML.**</span><span class="sxs-lookup"><span data-stu-id="ba809-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS\_ERROR\_INVALID\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-234">9126 (0x23a6)</span><span class="sxs-lookup"><span data-stu-id="ba809-234">9126 (0x23A6)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-235">Dieser Vorgang konnte nicht abgeschlossen werden, da der empfangene XML-Datenstrom leer oder syntaktisch ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="ba809-235">This operation could not be completed because the XML stream received is empty or syntactically invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS- \_ Fehler \_ keine \_ gültigen \_ Vertrauens \_ Anker**</span><span class="sxs-lookup"><span data-stu-id="ba809-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS\_ERROR\_NO\_VALID\_TRUST\_ANCHORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-237">9127 (0x23a7)</span><span class="sxs-lookup"><span data-stu-id="ba809-237">9127 (0x23A7)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-238">Dieser Vorgang wurde abgeschlossen, aber es wurden keine Vertrauensanker hinzugefügt, da alle empfangenen Vertrauensanker entweder ungültig, nicht unterstützt, abgelaufen sind oder in weniger als 30 Tagen nicht gültig werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-238">This operation completed, but no trust anchors were added because all of the trust anchors received were either invalid, unsupported, expired, or would not become valid in less than 30 days.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS \_ - \_ fehlerrollover nicht in den \_ \_ Besitz**</span><span class="sxs-lookup"><span data-stu-id="ba809-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS\_ERROR\_ROLLOVER\_NOT\_POKEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-240">9128 (0x23a8)</span><span class="sxs-lookup"><span data-stu-id="ba809-240">9128 (0x23A8)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-241">Der angegebene Signatur Schlüssel wartet nicht auf das Update der Eltern-DS.</span><span class="sxs-lookup"><span data-stu-id="ba809-241">The specified signing key is not waiting for parental DS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS- \_ Fehler \_ NSEC3 \_ namens \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="ba809-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS\_ERROR\_NSEC3\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-243">9129 (0x23a9)</span><span class="sxs-lookup"><span data-stu-id="ba809-243">9129 (0x23A9)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-244">Hash Kollision während der NSEC3-Signierung erkannt.</span><span class="sxs-lookup"><span data-stu-id="ba809-244">Hash collision detected during NSEC3 signing.</span></span> <span data-ttu-id="ba809-245">Geben Sie einen anderen vom Benutzer bereitgestellten Salt an, oder verwenden Sie einen zufällig generierten Salt-Typ, und versuchen Sie erneut, die Zone zu signieren.</span><span class="sxs-lookup"><span data-stu-id="ba809-245">Specify a different user-provided salt, or use a randomly generated salt, and attempt to sign the zone again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS- \_ Fehler \_ nsec nicht \_ kompatibel \_ mit \_ NSEC3 \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="ba809-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS\_ERROR\_NSEC\_INCOMPATIBLE\_WITH\_NSEC3\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-247">9130 (0x23aa)</span><span class="sxs-lookup"><span data-stu-id="ba809-247">9130 (0x23AA)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-248">Nsec ist nicht kompatibel mit dem NSEC3-RSA-SHA-1-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="ba809-248">NSEC is not compatible with the NSEC3-RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="ba809-249">Wählen Sie einen anderen Algorithmus aus, oder verwenden Sie NSEC3.</span><span class="sxs-lookup"><span data-stu-id="ba809-249">Choose a different algorithm or use NSEC3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS- \_ Info \_ keine \_ Datensätze**</span><span class="sxs-lookup"><span data-stu-id="ba809-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS\_INFO\_NO\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-251">9501 (0x251d)</span><span class="sxs-lookup"><span data-stu-id="ba809-251">9501 (0x251D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-252">Bei der DNS-Abfrage wurden keine Einträge gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-252">No records found for given DNS query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS \_ - \_ Fehler \_ Paket**</span><span class="sxs-lookup"><span data-stu-id="ba809-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS\_ERROR\_BAD\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-254">9502 (0x251e)</span><span class="sxs-lookup"><span data-stu-id="ba809-254">9502 (0x251E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-255">Ungültiges DNS-Paket.</span><span class="sxs-lookup"><span data-stu-id="ba809-255">Bad DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS- \_ Fehler " \_ kein \_ Paket"**</span><span class="sxs-lookup"><span data-stu-id="ba809-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS\_ERROR\_NO\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-257">9503 (0x251f)</span><span class="sxs-lookup"><span data-stu-id="ba809-257">9503 (0x251F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-258">Kein DNS-Paket.</span><span class="sxs-lookup"><span data-stu-id="ba809-258">No DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS- \_ Fehler- \_ RCODE**</span><span class="sxs-lookup"><span data-stu-id="ba809-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS\_ERROR\_RCODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-260">9504 (0x2520)</span><span class="sxs-lookup"><span data-stu-id="ba809-260">9504 (0x2520)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-261">DNS-Fehler, überprüfen Sie RCODE.</span><span class="sxs-lookup"><span data-stu-id="ba809-261">DNS error, check rcode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**unsichere DNS- \_ Fehler \_ \_ Paket**</span><span class="sxs-lookup"><span data-stu-id="ba809-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS\_ERROR\_UNSECURE\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-263">9505 (0x2521)</span><span class="sxs-lookup"><span data-stu-id="ba809-263">9505 (0x2521)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-264">Ungesichertes DNS-Paket.</span><span class="sxs-lookup"><span data-stu-id="ba809-264">Unsecured DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**ausstehende DNS- \_ Anforderung \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-266">9506 (0x2522)</span><span class="sxs-lookup"><span data-stu-id="ba809-266">9506 (0x2522)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-267">Die DNS-Abfrage Anforderung steht aus.</span><span class="sxs-lookup"><span data-stu-id="ba809-267">DNS query request is pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_ \_ Ungültiger DNS- \_ Fehlertyp**</span><span class="sxs-lookup"><span data-stu-id="ba809-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS\_ERROR\_INVALID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-269">9551 (0x254f)</span><span class="sxs-lookup"><span data-stu-id="ba809-269">9551 (0x254F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-270">Ungültiger DNS-Typ.</span><span class="sxs-lookup"><span data-stu-id="ba809-270">Invalid DNS type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS \_ \_ -Fehler ungültige \_ IP- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="ba809-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS\_ERROR\_INVALID\_IP\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-272">9552 (0x2550)</span><span class="sxs-lookup"><span data-stu-id="ba809-272">9552 (0x2550)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-273">Ungültige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="ba809-273">Invalid IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_Fehler bei \_ Ungültiger DNS- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="ba809-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS\_ERROR\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-275">9553 (0x2551)</span><span class="sxs-lookup"><span data-stu-id="ba809-275">9553 (0x2551)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-276">Ungültige Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ba809-276">Invalid property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS \_ - \_ Fehler \_ später erneut versuchen \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS\_ERROR\_TRY\_AGAIN\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-278">9554 (0x2552)</span><span class="sxs-lookup"><span data-stu-id="ba809-278">9554 (0x2552)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-279">Versuchen Sie den DNS-Vorgang später erneut.</span><span class="sxs-lookup"><span data-stu-id="ba809-279">Try DNS operation again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS- \_ Fehler ist \_ nicht \_ eindeutig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-281">9555 (0x2553)</span><span class="sxs-lookup"><span data-stu-id="ba809-281">9555 (0x2553)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-282">Der Datensatz für den angegebenen Namen und Typ ist nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ba809-282">Record for given name and type is not unique.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS- \_ Fehler \_ nicht RFC- \_ \_ Name**</span><span class="sxs-lookup"><span data-stu-id="ba809-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS\_ERROR\_NON\_RFC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-284">9556 (0x2554)</span><span class="sxs-lookup"><span data-stu-id="ba809-284">9556 (0x2554)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-285">Der DNS-Name entspricht nicht den RFC-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="ba809-285">DNS name does not comply with RFC specifications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS- \_ Status- \_ FQDN**</span><span class="sxs-lookup"><span data-stu-id="ba809-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS\_STATUS\_FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-287">9557 (0x2555)</span><span class="sxs-lookup"><span data-stu-id="ba809-287">9557 (0x2555)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-288">Der DNS-Name ist ein voll qualifizierter DNS-Name.</span><span class="sxs-lookup"><span data-stu-id="ba809-288">DNS name is a fully-qualified DNS name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS- \_ Status Punkt \_ \_ Name**</span><span class="sxs-lookup"><span data-stu-id="ba809-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS\_STATUS\_DOTTED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-290">9558 (0x2556)</span><span class="sxs-lookup"><span data-stu-id="ba809-290">9558 (0x2556)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-291">Der DNS-Name ist gepunktet (mehrfach Bezeichnung).</span><span class="sxs-lookup"><span data-stu-id="ba809-291">DNS name is dotted (multi-label).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS- \_ Status \_ einzelner \_ Teil \_ Name**</span><span class="sxs-lookup"><span data-stu-id="ba809-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS\_STATUS\_SINGLE\_PART\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-293">9559 (0x2557)</span><span class="sxs-lookup"><span data-stu-id="ba809-293">9559 (0x2557)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-294">Der DNS-Name ist ein einteilige Name.</span><span class="sxs-lookup"><span data-stu-id="ba809-294">DNS name is a single-part name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS- \_ Fehler \_ ungültiger \_ Name \_ Char**</span><span class="sxs-lookup"><span data-stu-id="ba809-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS\_ERROR\_INVALID\_NAME\_CHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-296">9560 (0x2558)</span><span class="sxs-lookup"><span data-stu-id="ba809-296">9560 (0x2558)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-297">Der DNS-Name enthält ein ungültiges Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ba809-297">DNS name contains an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ numerischer \_ Name des DNS-Fehlers**</span><span class="sxs-lookup"><span data-stu-id="ba809-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS\_ERROR\_NUMERIC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-299">9561 (0x2559)</span><span class="sxs-lookup"><span data-stu-id="ba809-299">9561 (0x2559)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-300">Der DNS-Name ist vollständig numerisch.</span><span class="sxs-lookup"><span data-stu-id="ba809-300">DNS name is entirely numeric.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS-Fehler ist auf dem Stamm \_ \_ \_ \_ \_ \_ Server nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ROOT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-302">9562 (0x255 a)</span><span class="sxs-lookup"><span data-stu-id="ba809-302">9562 (0x255A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-303">Der angeforderte Vorgang ist auf einem DNS-Stamm Server nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba809-303">The operation requested is not permitted on a DNS root server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS \_ - \_ Fehler \_ \_ bei \_ Delegierung nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DELEGATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-305">9563 (0x255 b)</span><span class="sxs-lookup"><span data-stu-id="ba809-305">9563 (0x255B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-306">Der Datensatz konnte nicht erstellt werden, da dieser Teil des DNS-Namespace an einen anderen Server delegiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-306">The record could not be created because this part of the DNS namespace has been delegated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS-Fehler beim finden von Stamm \_ \_ \_ \_ hinweisen nicht gefunden \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS\_ERROR\_CANNOT\_FIND\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-308">9564 (0x255 c)</span><span class="sxs-lookup"><span data-stu-id="ba809-308">9564 (0x255C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-309">Der DNS-Server konnte einen Satz von Stamm hinweisen nicht finden.</span><span class="sxs-lookup"><span data-stu-id="ba809-309">The DNS server could not find a set of root hints.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS- \_ Fehler \_ inkonsistente Stamm \_ \_ Hinweise**</span><span class="sxs-lookup"><span data-stu-id="ba809-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS\_ERROR\_INCONSISTENT\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-311">9565 (0x255 d)</span><span class="sxs-lookup"><span data-stu-id="ba809-311">9565 (0x255D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-312">Der DNS-Server hat Stamm Hinweise gefunden, aber er war für alle Adapter nicht konsistent.</span><span class="sxs-lookup"><span data-stu-id="ba809-312">The DNS server found root hints but they were not consistent across all adapters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS- \_ Fehler \_ DWORD- \_ Wert \_ zu \_ klein**</span><span class="sxs-lookup"><span data-stu-id="ba809-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-314">9566 (0x255 e)</span><span class="sxs-lookup"><span data-stu-id="ba809-314">9566 (0x255E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-315">Der angegebene Wert ist für diesen Parameter zu klein.</span><span class="sxs-lookup"><span data-stu-id="ba809-315">The specified value is too small for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS- \_ Fehler \_ DWORD-Wert ist \_ \_ zu \_ groß.**</span><span class="sxs-lookup"><span data-stu-id="ba809-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-317">9567 (0x255 f)</span><span class="sxs-lookup"><span data-stu-id="ba809-317">9567 (0x255F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-318">Der angegebene Wert ist zu groß für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="ba809-318">The specified value is too large for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS- \_ Fehler beim \_ Laden im Hintergrund \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS\_ERROR\_BACKGROUND\_LOADING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-320">9568 (0x2560)</span><span class="sxs-lookup"><span data-stu-id="ba809-320">9568 (0x2560)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-321">Dieser Vorgang ist nicht zulässig, wenn der DNS-Server Zonen im Hintergrund lädt.</span><span class="sxs-lookup"><span data-stu-id="ba809-321">This operation is not allowed while the DNS server is loading zones in the background.</span></span> <span data-ttu-id="ba809-322">Versuchen Sie es später noch mal.</span><span class="sxs-lookup"><span data-stu-id="ba809-322">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS- \_ Fehler ist \_ auf dem \_ \_ \_ RODC nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_RODC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-324">9569 (0x2561)</span><span class="sxs-lookup"><span data-stu-id="ba809-324">9569 (0x2561)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-325">Der angeforderte Vorgang ist für einen DNS-Server, der auf einem schreibgeschützten Domänen Controller ausgeführt wird, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba809-325">The operation requested is not permitted on against a DNS server running on a read-only DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS- \_ Fehler ist \_ \_ \_ unter \_ dname nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="ba809-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-327">9570 (0x2562)</span><span class="sxs-lookup"><span data-stu-id="ba809-327">9570 (0x2562)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-328">Unterhalb eines dname-Einsatzes dürfen keine Daten vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ba809-328">No data is allowed to exist underneath a DNAME record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS- \_ Fehler \_ Delegierung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ba809-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS\_ERROR\_DELEGATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-330">9571 (0x2563)</span><span class="sxs-lookup"><span data-stu-id="ba809-330">9571 (0x2563)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-331">Dieser Vorgang erfordert die Delegierung von Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="ba809-331">This operation requires credentials delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_ \_ ungültige \_ Richtlinien \_ Tabelle für DNS-Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS\_ERROR\_INVALID\_POLICY\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-333">9572 (0x2564)</span><span class="sxs-lookup"><span data-stu-id="ba809-333">9572 (0x2564)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-334">Die Richtlinien Tabelle für die Namensauflösung ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ba809-334">Name resolution policy table has been corrupted.</span></span> <span data-ttu-id="ba809-335">Die DNS-Auflösung schlägt fehl, bis Sie korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba809-335">DNS resolution will fail until it is fixed.</span></span> <span data-ttu-id="ba809-336">Wenden Sie sich an den Netzwerkadministrator.</span><span class="sxs-lookup"><span data-stu-id="ba809-336">Contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**die DNS- \_ Fehler \_ Zone \_ ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS\_ERROR\_ZONE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-338">9601 (0x2581)</span><span class="sxs-lookup"><span data-stu-id="ba809-338">9601 (0x2581)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-339">Die DNS-Zone ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-339">DNS zone does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS- \_ Fehler \_ ohne \_ Zonen \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="ba809-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS\_ERROR\_NO\_ZONE\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-341">9602 (0x2582)</span><span class="sxs-lookup"><span data-stu-id="ba809-341">9602 (0x2582)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-342">Es sind keine DNS-Zonen Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba809-342">DNS zone information not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS- \_ Fehler \_ ungültiger \_ Zonen \_ Vorgang.**</span><span class="sxs-lookup"><span data-stu-id="ba809-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS\_ERROR\_INVALID\_ZONE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-344">9603 (0x2583)</span><span class="sxs-lookup"><span data-stu-id="ba809-344">9603 (0x2583)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-345">Ungültiger Vorgang für die DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-345">Invalid operation for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS- \_ Fehler \_ Zonen- \_ Konfigurations \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS\_ERROR\_ZONE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-347">9604 (0x2584)</span><span class="sxs-lookup"><span data-stu-id="ba809-347">9604 (0x2584)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-348">Ungültige DNS-Zonen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ba809-348">Invalid DNS zone configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS- \_ Fehler \_ Zone \_ weist \_ keinen SOA- \_ \_ Datensatz auf.**</span><span class="sxs-lookup"><span data-stu-id="ba809-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_SOA\_RECORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-350">9605 (0x2585)</span><span class="sxs-lookup"><span data-stu-id="ba809-350">9605 (0x2585)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-351">Die DNS-Zone hat keinen Start-of-Authority-Datensatz (SOA).</span><span class="sxs-lookup"><span data-stu-id="ba809-351">DNS zone has no start of authority (SOA) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS- \_ Fehler \_ Zone \_ enthält \_ keine NS- \_ \_ Einträge.**</span><span class="sxs-lookup"><span data-stu-id="ba809-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_NS\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-353">9606 (0x2586)</span><span class="sxs-lookup"><span data-stu-id="ba809-353">9606 (0x2586)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-354">Die DNS-Zone hat keinen Name Server-Datensatz (NS).</span><span class="sxs-lookup"><span data-stu-id="ba809-354">DNS zone has no Name Server (NS) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS- \_ Fehler \_ Zone \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="ba809-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS\_ERROR\_ZONE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-356">9607 (0x2587)</span><span class="sxs-lookup"><span data-stu-id="ba809-356">9607 (0x2587)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-357">Die DNS-Zone ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="ba809-357">DNS zone is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**Fehler beim Erstellen der DNS- \_ Fehler \_ Zone \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**DNS\_ERROR\_ZONE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-359">9608 (0x2588)</span><span class="sxs-lookup"><span data-stu-id="ba809-359">9608 (0x2588)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-360">Fehler beim Erstellen der DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-360">DNS zone creation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS- \_ Fehler \_ Zone \_ bereits \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="ba809-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS\_ERROR\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-362">9609 (0x2589)</span><span class="sxs-lookup"><span data-stu-id="ba809-362">9609 (0x2589)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-363">Die DNS-Zone ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-363">DNS zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS \_ - \_ fehlerautozone ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS\_ERROR\_AUTOZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-365">9610 (0x258a)</span><span class="sxs-lookup"><span data-stu-id="ba809-365">9610 (0x258A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-366">Die automatische DNS-Zone ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-366">DNS automatic zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS- \_ Fehler \_ ungültiger \_ \_ Zonentyp.**</span><span class="sxs-lookup"><span data-stu-id="ba809-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS\_ERROR\_INVALID\_ZONE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-368">9611 (0x258b)</span><span class="sxs-lookup"><span data-stu-id="ba809-368">9611 (0x258B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-369">Ungültiger DNS-Zonentyp.</span><span class="sxs-lookup"><span data-stu-id="ba809-369">Invalid DNS zone type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS \_ \_ -Fehler Sekundär \_ erfordert \_ Master \_ -IP**</span><span class="sxs-lookup"><span data-stu-id="ba809-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS\_ERROR\_SECONDARY\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-371">9612 (0x258c)</span><span class="sxs-lookup"><span data-stu-id="ba809-371">9612 (0x258C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-372">Die sekundäre DNS-Zone erfordert die Master-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="ba809-372">Secondary DNS zone requires master IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS- \_ Fehler \_ Zone \_ nicht \_ Sekundär**</span><span class="sxs-lookup"><span data-stu-id="ba809-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS\_ERROR\_ZONE\_NOT\_SECONDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-374">9613 (0x258d)</span><span class="sxs-lookup"><span data-stu-id="ba809-374">9613 (0x258D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-375">DNS-Zone ist nicht sekundär.</span><span class="sxs-lookup"><span data-stu-id="ba809-375">DNS zone not secondary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS- \_ Fehler bei \_ Bedarf \_ Sekundär \_ Adressen**</span><span class="sxs-lookup"><span data-stu-id="ba809-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS\_ERROR\_NEED\_SECONDARY\_ADDRESSES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-377">9614 (0x258e)</span><span class="sxs-lookup"><span data-stu-id="ba809-377">9614 (0x258E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-378">Sekundäre IP-Adresse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba809-378">Need secondary IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS \_ - \_ Fehler \_ WINS \_ -Initialisierungsfehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS\_ERROR\_WINS\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-380">9615 (0x258f)</span><span class="sxs-lookup"><span data-stu-id="ba809-380">9615 (0x258F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-381">Fehler bei der WINS-Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="ba809-381">WINS initialization failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS- \_ Fehler bei \_ WINS- \_ \_ Servern**</span><span class="sxs-lookup"><span data-stu-id="ba809-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS\_ERROR\_NEED\_WINS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-383">9616 (0x2590)</span><span class="sxs-lookup"><span data-stu-id="ba809-383">9616 (0x2590)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-384">Sie benötigen WINS-Server.</span><span class="sxs-lookup"><span data-stu-id="ba809-384">Need WINS servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS- \_ Fehler \_ bei NBSTAT- \_ Init \_ .**</span><span class="sxs-lookup"><span data-stu-id="ba809-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS\_ERROR\_NBSTAT\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-386">9617 (0x2591)</span><span class="sxs-lookup"><span data-stu-id="ba809-386">9617 (0x2591)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-387">Fehler beim nbtstat-Initialisierungs Rückruf.</span><span class="sxs-lookup"><span data-stu-id="ba809-387">NBTSTAT initialization call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS- \_ Fehler- \_ SOA- \_ Löschung \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="ba809-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS\_ERROR\_SOA\_DELETE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-389">9618 (0x2592)</span><span class="sxs-lookup"><span data-stu-id="ba809-389">9618 (0x2592)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-390">Ungültiges Löschen von Autoritäts Anfang (SOA).</span><span class="sxs-lookup"><span data-stu-id="ba809-390">Invalid delete of start of authority (SOA).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**die DNS- \_ Fehler \_ Weiterleitung ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS\_ERROR\_FORWARDER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-392">9619 (0x2593)</span><span class="sxs-lookup"><span data-stu-id="ba809-392">9619 (0x2593)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-393">Für diesen Namen ist bereits eine bedingte Weiterleitungs Zone vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-393">A conditional forwarding zone already exists for that name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS \_ \_ -Fehler Zone \_ erfordert \_ Master \_ -IP**</span><span class="sxs-lookup"><span data-stu-id="ba809-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS\_ERROR\_ZONE\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-395">9620 (0x2594)</span><span class="sxs-lookup"><span data-stu-id="ba809-395">9620 (0x2594)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-396">Diese Zone muss mit mindestens einer Master-DNS-Server-IP-Adresse konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-396">This zone must be configured with one or more master DNS server IP addresses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS- \_ Fehler \_ Zone \_ wird \_ heruntergefahren**</span><span class="sxs-lookup"><span data-stu-id="ba809-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS\_ERROR\_ZONE\_IS\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-398">9621 (0x2595)</span><span class="sxs-lookup"><span data-stu-id="ba809-398">9621 (0x2595)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-399">Der Vorgang kann nicht ausgeführt werden, da diese Zone heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="ba809-399">The operation cannot be performed because this zone is shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS \_ - \_ Fehler \_ Zone \_ für \_ Signierung gesperrt**</span><span class="sxs-lookup"><span data-stu-id="ba809-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS\_ERROR\_ZONE\_LOCKED\_FOR\_SIGNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-401">9622 (0x2596)</span><span class="sxs-lookup"><span data-stu-id="ba809-401">9622 (0x2596)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-402">Dieser Vorgang kann nicht ausgeführt werden, da die Zone derzeit signiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba809-402">This operation cannot be performed because the zone is currently being signed.</span></span> <span data-ttu-id="ba809-403">Versuchen Sie es später noch mal.</span><span class="sxs-lookup"><span data-stu-id="ba809-403">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS- \_ Fehler \_ primär \_ erfordert \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="ba809-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS\_ERROR\_PRIMARY\_REQUIRES\_DATAFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-405">9651 (0x25b3)</span><span class="sxs-lookup"><span data-stu-id="ba809-405">9651 (0x25B3)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-406">Die primäre DNS-Zone erfordert "DataFile".</span><span class="sxs-lookup"><span data-stu-id="ba809-406">Primary DNS zone requires datafile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS- \_ Fehler \_ ungültiger \_ DataFile- \_ Name.**</span><span class="sxs-lookup"><span data-stu-id="ba809-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS\_ERROR\_INVALID\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-408">9652 (0x25b4)</span><span class="sxs-lookup"><span data-stu-id="ba809-408">9652 (0x25B4)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-409">Ungültiger Datendatei-Name für die DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-409">Invalid datafile name for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**\_Fehler beim \_ Öffnen der Daten \_ Datei \_ im DNS-Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS\_ERROR\_DATAFILE\_OPEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-411">9653 (0x25b5)</span><span class="sxs-lookup"><span data-stu-id="ba809-411">9653 (0x25B5)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-412">Fehler beim Öffnen der Datendatei für die DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-412">Failed to open datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**Fehler beim Rück Schreiben der DNS- \_ Fehler \_ Datei. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS\_ERROR\_FILE\_WRITEBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-414">9654 (0x25b6)</span><span class="sxs-lookup"><span data-stu-id="ba809-414">9654 (0x25B6)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-415">Fehler beim Schreiben der Datendatei für die DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-415">Failed to write datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS- \_ Fehler \_ Datendatei \_ -Verarbeitung**</span><span class="sxs-lookup"><span data-stu-id="ba809-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS\_ERROR\_DATAFILE\_PARSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-417">9655 (0x25b7)</span><span class="sxs-lookup"><span data-stu-id="ba809-417">9655 (0x25B7)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-418">Fehler beim Lesen der Datendatei für die DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-418">Failure while reading datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**der DNS- \_ Fehler \_ Daten Satz \_ ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS\_ERROR\_RECORD\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-420">9701 (0x25e5)</span><span class="sxs-lookup"><span data-stu-id="ba809-420">9701 (0x25E5)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-421">Der DNS-Datensatz ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-421">DNS record does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS- \_ Fehler \_ Daten Satz \_ Format**</span><span class="sxs-lookup"><span data-stu-id="ba809-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS\_ERROR\_RECORD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-423">9702 (0x25e6)</span><span class="sxs-lookup"><span data-stu-id="ba809-423">9702 (0x25E6)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-424">Fehler im DNS-Daten Satz Format.</span><span class="sxs-lookup"><span data-stu-id="ba809-424">DNS record format error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**Fehler bei der DNS- \_ Fehler \_ Knoten \_ Erstellung \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**DNS\_ERROR\_NODE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-426">9703 (0x25e7)</span><span class="sxs-lookup"><span data-stu-id="ba809-426">9703 (0x25E7)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-427">Fehler bei der Knoten Erstellung in DNS.</span><span class="sxs-lookup"><span data-stu-id="ba809-427">Node creation failure in DNS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**Unbekannter DNS- \_ Fehler \_ \_ Daten Satz \_ .**</span><span class="sxs-lookup"><span data-stu-id="ba809-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS\_ERROR\_UNKNOWN\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-429">9704 (0x25e8)</span><span class="sxs-lookup"><span data-stu-id="ba809-429">9704 (0x25E8)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-430">Unbekannter DNS-Daten eingabentyp.</span><span class="sxs-lookup"><span data-stu-id="ba809-430">Unknown DNS record type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**Timeout beim DNS- \_ Fehler \_ Daten Satz. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS\_ERROR\_RECORD\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-432">9705 (0x25e9)</span><span class="sxs-lookup"><span data-stu-id="ba809-432">9705 (0x25E9)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-433">Timeout beim DNS-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="ba809-433">DNS record timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS- \_ Fehler \_ Name \_ nicht \_ in \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="ba809-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS\_ERROR\_NAME\_NOT\_IN\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-435">9706 (0x25ea)</span><span class="sxs-lookup"><span data-stu-id="ba809-435">9706 (0x25EA)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-436">Der Name ist nicht in der DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-436">Name not in DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS- \_ Fehler \_ CNAME- \_ Schleife**</span><span class="sxs-lookup"><span data-stu-id="ba809-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS\_ERROR\_CNAME\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-438">9707 (0x25eb)</span><span class="sxs-lookup"><span data-stu-id="ba809-438">9707 (0x25EB)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-439">CNAME-Schleife erkannt.</span><span class="sxs-lookup"><span data-stu-id="ba809-439">CNAME loop detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS- \_ Fehler \_ Knoten ist " \_ \_ CNAME"**</span><span class="sxs-lookup"><span data-stu-id="ba809-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS\_ERROR\_NODE\_IS\_CNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-441">9708 (0x25ec)</span><span class="sxs-lookup"><span data-stu-id="ba809-441">9708 (0x25EC)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-442">Knoten ist ein CNAME-DNS-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="ba809-442">Node is a CNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS- \_ Fehler \_ CNAME- \_ Kollision**</span><span class="sxs-lookup"><span data-stu-id="ba809-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS\_ERROR\_CNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-444">9709 (0x25ed)</span><span class="sxs-lookup"><span data-stu-id="ba809-444">9709 (0x25ED)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-445">Für den angegebenen Namen ist bereits ein CNAME-Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-445">A CNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS- \_ Fehler \_ Daten Satz \_ nur \_ in \_ Zonenstamm \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS\_ERROR\_RECORD\_ONLY\_AT\_ZONE\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-447">9710 (0x25ee)</span><span class="sxs-lookup"><span data-stu-id="ba809-447">9710 (0x25EE)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-448">Nur in DNS-Zonen Stamm aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="ba809-448">Record only at DNS zone root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS- \_ Fehler \_ Daten Satz ist \_ bereits \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="ba809-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS\_ERROR\_RECORD\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-450">9711 (0x25ef)</span><span class="sxs-lookup"><span data-stu-id="ba809-450">9711 (0x25EF)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-451">Der DNS-Datensatz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-451">DNS record already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**sekundäre DNS- \_ Fehler \_ \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="ba809-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS\_ERROR\_SECONDARY\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-453">9712 (0x25f 0)</span><span class="sxs-lookup"><span data-stu-id="ba809-453">9712 (0x25F0)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-454">Daten der sekundären DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="ba809-454">Secondary DNS zone data error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS- \_ Fehler \_ No \_ Create \_ Cache \_ Data**</span><span class="sxs-lookup"><span data-stu-id="ba809-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS\_ERROR\_NO\_CREATE\_CACHE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-456">9713 (0x25f 1)</span><span class="sxs-lookup"><span data-stu-id="ba809-456">9713 (0x25F1)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-457">Es konnten keine DNS-Cache Daten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-457">Could not create DNS cache data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**der DNS- \_ Fehler \_ Name \_ ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS\_ERROR\_NAME\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-459">9714 (0x25f 2)</span><span class="sxs-lookup"><span data-stu-id="ba809-459">9714 (0x25F2)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-460">Der DNS-Name ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-460">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**Fehler beim Erstellen der DNS- \_ Warnung \_ ptr. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS\_WARNING\_PTR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-462">9715 (0x25f)</span><span class="sxs-lookup"><span data-stu-id="ba809-462">9715 (0x25F3)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-463">Der Zeiger (PTR)-Datensatz konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-463">Could not create pointer (PTR) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS- \_ Warn \_ Domäne \_ nicht gelöscht**</span><span class="sxs-lookup"><span data-stu-id="ba809-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS\_WARNING\_DOMAIN\_UNDELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-465">9716 (0x25f 4)</span><span class="sxs-lookup"><span data-stu-id="ba809-465">9716 (0x25F4)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-466">Die DNS-Domäne wurde wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="ba809-466">DNS domain was undeleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS- \_ Fehler- \_ DS nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="ba809-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS\_ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-468">9717 (0x25f)</span><span class="sxs-lookup"><span data-stu-id="ba809-468">9717 (0x25F5)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-469">Der Verzeichnisdienst ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba809-469">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS- \_ Fehler- \_ DS- \_ Zone \_ bereits \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="ba809-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS\_ERROR\_DS\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-471">9718 (0x25f 6)</span><span class="sxs-lookup"><span data-stu-id="ba809-471">9718 (0x25F6)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-472">Die DNS-Zone ist im Verzeichnisdienst bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-472">DNS zone already exists in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS- \_ Fehler \_ keine \_ BootFile, \_ Wenn DS- \_ \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="ba809-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS\_ERROR\_NO\_BOOTFILE\_IF\_DS\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-474">9719 (0x25f)</span><span class="sxs-lookup"><span data-stu-id="ba809-474">9719 (0x25F7)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-475">Der DNS-Server erstellt oder liest die Startdatei für die integrierte DNS-Zone des Verzeichnis Dienstanbieter nicht.</span><span class="sxs-lookup"><span data-stu-id="ba809-475">DNS server not creating or reading the boot file for the directory service integrated DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS- \_ Fehler \_ Knoten ist " \_ \_ DName"**</span><span class="sxs-lookup"><span data-stu-id="ba809-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS\_ERROR\_NODE\_IS\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-477">9720 (0x25f 8)</span><span class="sxs-lookup"><span data-stu-id="ba809-477">9720 (0x25F8)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-478">Knoten ist ein DNS-Datensatz mit dname.</span><span class="sxs-lookup"><span data-stu-id="ba809-478">Node is a DNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS- \_ Fehler \_ dname- \_ Kollision**</span><span class="sxs-lookup"><span data-stu-id="ba809-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS\_ERROR\_DNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-480">9721 (0x25f)</span><span class="sxs-lookup"><span data-stu-id="ba809-480">9721 (0x25F9)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-481">Für den angegebenen Namen ist bereits ein DNAME-Datensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-481">A DNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS \_ - \_ fehleralias \_ Schleife**</span><span class="sxs-lookup"><span data-stu-id="ba809-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS\_ERROR\_ALIAS\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-483">9722 (0x25fa)</span><span class="sxs-lookup"><span data-stu-id="ba809-483">9722 (0x25FA)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-484">Eine Alias Schleife wurde mit CNAME-oder dname-Einträgen erkannt.</span><span class="sxs-lookup"><span data-stu-id="ba809-484">An alias loop has been detected with either CNAME or DNAME records.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS- \_ Info- \_ AXFR \_ fertiggestellt**</span><span class="sxs-lookup"><span data-stu-id="ba809-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS\_INFO\_AXFR\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-486">9751 (0x2617)</span><span class="sxs-lookup"><span data-stu-id="ba809-486">9751 (0x2617)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-487">DNS AXFR (Zonen Übertragung) ist fertiggestellt.</span><span class="sxs-lookup"><span data-stu-id="ba809-487">DNS AXFR (zone transfer) complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS- \_ Fehler \_ AXFR**</span><span class="sxs-lookup"><span data-stu-id="ba809-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS\_ERROR\_AXFR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-489">9752 (0x2618)</span><span class="sxs-lookup"><span data-stu-id="ba809-489">9752 (0x2618)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-490">Fehler bei der DNS-Zonen Übertragung.</span><span class="sxs-lookup"><span data-stu-id="ba809-490">DNS zone transfer failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS- \_ Info \_ hinzugefügter \_ lokaler \_ WINS**</span><span class="sxs-lookup"><span data-stu-id="ba809-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS\_INFO\_ADDED\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-492">9753 (0x2619)</span><span class="sxs-lookup"><span data-stu-id="ba809-492">9753 (0x2619)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-493">Lokaler WINS-Server wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ba809-493">Added local WINS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS- \_ Status \_ fortsetzen \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="ba809-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS\_STATUS\_CONTINUE\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-495">9801 (0x2649)</span><span class="sxs-lookup"><span data-stu-id="ba809-495">9801 (0x2649)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-496">Der sichere Aktualisierungs Vorgang muss die Aktualisierungs Anforderung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="ba809-496">Secure update call needs to continue update request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS- \_ Fehler \_ No \_ tcpip**</span><span class="sxs-lookup"><span data-stu-id="ba809-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS\_ERROR\_NO\_TCPIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-498">9851 (0x267b)</span><span class="sxs-lookup"><span data-stu-id="ba809-498">9851 (0x267B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-499">Das TCP/IP-Netzwerkprotokoll ist nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="ba809-499">TCP/IP network protocol not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS- \_ Fehler \_ keine DNS- \_ \_ Server**</span><span class="sxs-lookup"><span data-stu-id="ba809-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS\_ERROR\_NO\_DNS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-501">9852 (0x267c)</span><span class="sxs-lookup"><span data-stu-id="ba809-501">9852 (0x267C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-502">Für das lokale System sind keine DNS-Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ba809-502">No DNS servers configured for local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS- \_ Fehler- \_ DP \_ ist \_ nicht \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS\_ERROR\_DP\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-504">9901 (0x26ad)</span><span class="sxs-lookup"><span data-stu-id="ba809-504">9901 (0x26AD)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-505">Die angegebene Verzeichnis Partition ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-505">The specified directory partition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS- \_ Fehler- \_ DP \_ bereits \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="ba809-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS\_ERROR\_DP\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-507">9902 (0x26ae)</span><span class="sxs-lookup"><span data-stu-id="ba809-507">9902 (0x26AE)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-508">Die angegebene Verzeichnis Partition ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-508">The specified directory partition already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS- \_ Fehler- \_ DP \_ nicht \_ eingetragen**</span><span class="sxs-lookup"><span data-stu-id="ba809-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS\_ERROR\_DP\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-510">9903 (0x26af)</span><span class="sxs-lookup"><span data-stu-id="ba809-510">9903 (0x26AF)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-511">Dieser DNS-Server ist nicht in der angegebenen Verzeichnis Partition eingetragen.</span><span class="sxs-lookup"><span data-stu-id="ba809-511">This DNS server is not enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS- \_ Fehler- \_ DP \_ bereits \_ eingetragen**</span><span class="sxs-lookup"><span data-stu-id="ba809-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS\_ERROR\_DP\_ALREADY\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-513">9904 (0x26b0)</span><span class="sxs-lookup"><span data-stu-id="ba809-513">9904 (0x26B0)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-514">Dieser DNS-Server ist bereits in der angegebenen Verzeichnis Partition eingetragen.</span><span class="sxs-lookup"><span data-stu-id="ba809-514">This DNS server is already enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS- \_ Fehler- \_ DP \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="ba809-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS\_ERROR\_DP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-516">9905 (0x26b1)</span><span class="sxs-lookup"><span data-stu-id="ba809-516">9905 (0x26B1)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-517">Die Verzeichnis Partition ist zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba809-517">The directory partition is not available at this time.</span></span> <span data-ttu-id="ba809-518">Bitte warten Sie einige Minuten, und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="ba809-518">Please wait a few minutes and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS- \_ Fehler bei \_ DP- \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS\_ERROR\_DP\_FSMO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-520">9906 (0x26b2)</span><span class="sxs-lookup"><span data-stu-id="ba809-520">9906 (0x26B2)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-521">Der Vorgang ist fehlgeschlagen, da die Domänen Namen-Master-Rolle nicht erreicht werden konnte.</span><span class="sxs-lookup"><span data-stu-id="ba809-521">The operation failed because the domain naming master FSMO role could not be reached.</span></span> <span data-ttu-id="ba809-522">Der Domänen Controller mit der FSMO-Rolle "Domänen Namen Master" ist nicht in der Lage, die Anforderung zu bedienen, oder er führt nicht Windows Server 2003 oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="ba809-522">The domain controller holding the domain naming master FSMO role is down or unable to service the request or is not running Windows Server 2003 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="ba809-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-524">10004 (0x2714)</span><span class="sxs-lookup"><span data-stu-id="ba809-524">10004 (0x2714)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-525">Ein Blockierungs Vorgang wurde durch einen wsacancelblockingstatement-Aufrufvorgang unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="ba809-525">A blocking operation was interrupted by a call to WSACancelBlockingCall.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**Wsaebadf**</span><span class="sxs-lookup"><span data-stu-id="ba809-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-527">10009 (0x2719)</span><span class="sxs-lookup"><span data-stu-id="ba809-527">10009 (0x2719)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-528">Das angegebene Datei Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ba809-528">The file handle supplied is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="ba809-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-530">10013 (0x271d)</span><span class="sxs-lookup"><span data-stu-id="ba809-530">10013 (0x271D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-531">Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ba809-531">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**Wsaefault**</span><span class="sxs-lookup"><span data-stu-id="ba809-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-533">10014 (0x271e)</span><span class="sxs-lookup"><span data-stu-id="ba809-533">10014 (0x271E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-534">Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.</span><span class="sxs-lookup"><span data-stu-id="ba809-534">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="ba809-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-536">10022 (0x2726)</span><span class="sxs-lookup"><span data-stu-id="ba809-536">10022 (0x2726)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-537">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba809-537">An invalid argument was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**Wsaemfile**</span><span class="sxs-lookup"><span data-stu-id="ba809-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-539">10024 (0x2728)</span><span class="sxs-lookup"><span data-stu-id="ba809-539">10024 (0x2728)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-540">Zu viele geöffnete Sockets.</span><span class="sxs-lookup"><span data-stu-id="ba809-540">Too many open sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span><span class="sxs-lookup"><span data-stu-id="ba809-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-542">10035 (0x2733)</span><span class="sxs-lookup"><span data-stu-id="ba809-542">10035 (0x2733)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-543">Ein nicht blockierender Socketvorgang konnte nicht sofort abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-543">A non-blocking socket operation could not be completed immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="ba809-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-545">10036 (0x2734)</span><span class="sxs-lookup"><span data-stu-id="ba809-545">10036 (0x2734)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-546">Ein Blockierungsvorgang wird momentan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba809-546">A blocking operation is currently executing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**Wsaebereits**</span><span class="sxs-lookup"><span data-stu-id="ba809-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-548">10037 (0x2735)</span><span class="sxs-lookup"><span data-stu-id="ba809-548">10037 (0x2735)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-549">Es wurde versucht, für einen nicht blockierenden Socket, für den bereits ein Vorgang ausgeführt wurde, einen weiteren Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ba809-549">An operation was attempted on a non-blocking socket that already had an operation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="ba809-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-551">10038 (0x2736)</span><span class="sxs-lookup"><span data-stu-id="ba809-551">10038 (0x2736)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-552">Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.</span><span class="sxs-lookup"><span data-stu-id="ba809-552">An operation was attempted on something that is not a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span><span class="sxs-lookup"><span data-stu-id="ba809-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-554">10039 (0x2737)</span><span class="sxs-lookup"><span data-stu-id="ba809-554">10039 (0x2737)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-555">Eine erforderliche Adresse wurde bei einem Vorgang für einen Socket ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="ba809-555">A required address was omitted from an operation on a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**Wsaemsgsize**</span><span class="sxs-lookup"><span data-stu-id="ba809-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-557">10040 (0x2738)</span><span class="sxs-lookup"><span data-stu-id="ba809-557">10040 (0x2738)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-558">Eine Nachricht, die über einen Datagrammsocket gesendet wurde, war für den internen Nachrichtenpuffer oder ein anderes Netzwerklimit zu groß, oder der Puffer für den Datagrammempfang war für das Datagramm zu klein.</span><span class="sxs-lookup"><span data-stu-id="ba809-558">A message sent on a datagram socket was larger than the internal message buffer or some other network limit, or the buffer used to receive a datagram into was smaller than the datagram itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span><span class="sxs-lookup"><span data-stu-id="ba809-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-560">10041 (0x2739)</span><span class="sxs-lookup"><span data-stu-id="ba809-560">10041 (0x2739)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-561">Im Socket-Funktions Aufrufwert wurde ein Protokoll angegeben, das die Semantik des angeforderten Sockettyps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ba809-561">A protocol was specified in the socket function call that does not support the semantics of the socket type requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="ba809-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-563">10042 (0x273a)</span><span class="sxs-lookup"><span data-stu-id="ba809-563">10042 (0x273A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-564">Eine unbekannte, ungültige oder nicht unterstützte Option oder Ebene wurde in einem getsockopt-oder setsockopt-Befehl angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba809-564">An unknown, invalid, or unsupported option or level was specified in a getsockopt or setsockopt call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**Wsaeprotonosupport**</span><span class="sxs-lookup"><span data-stu-id="ba809-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-566">10043 (0x273b)</span><span class="sxs-lookup"><span data-stu-id="ba809-566">10043 (0x273B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-567">Das angeforderte Protokoll wurde nicht im System konfiguriert, oder es ist keine Implementierung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-567">The requested protocol has not been configured into the system, or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**Wsaesocktnosupport**</span><span class="sxs-lookup"><span data-stu-id="ba809-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-569">10044 (0x273c)</span><span class="sxs-lookup"><span data-stu-id="ba809-569">10044 (0x273C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-570">In dieser Adressfamilie ist die Unterstützung für den angegebenen Sockettyp nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-570">The support for the specified socket type does not exist in this address family.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="ba809-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-572">10045 (0x273d)</span><span class="sxs-lookup"><span data-stu-id="ba809-572">10045 (0x273D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-573">Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ba809-573">The attempted operation is not supported for the type of object referenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**Wsaepf NoSupport**</span><span class="sxs-lookup"><span data-stu-id="ba809-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-575">10046 (0x273e)</span><span class="sxs-lookup"><span data-stu-id="ba809-575">10046 (0x273E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-576">Die Protokollfamilie wurde nicht im System konfiguriert, oder es ist keine Implementierung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-576">The protocol family has not been configured into the system or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="ba809-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-578">10047 (0x273f)</span><span class="sxs-lookup"><span data-stu-id="ba809-578">10047 (0x273F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-579">Es wurde eine Adresse verwendet, die nicht mit dem angeforderten Protokoll kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="ba809-579">An address incompatible with the requested protocol was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span><span class="sxs-lookup"><span data-stu-id="ba809-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-581">10048 (0x2740)</span><span class="sxs-lookup"><span data-stu-id="ba809-581">10048 (0x2740)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span><span class="sxs-lookup"><span data-stu-id="ba809-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**Wsaeaddrnotavail**</span><span class="sxs-lookup"><span data-stu-id="ba809-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-584">10049 (0x2741)</span><span class="sxs-lookup"><span data-stu-id="ba809-584">10049 (0x2741)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-585">Die angeforderte Adresse ist im Kontext nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="ba809-585">The requested address is not valid in its context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**Wsaaufetdown**</span><span class="sxs-lookup"><span data-stu-id="ba809-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-587">10050 (0x2742)</span><span class="sxs-lookup"><span data-stu-id="ba809-587">10050 (0x2742)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-588">Bei einem Socketvorgang war das Netzwerk inaktiv.</span><span class="sxs-lookup"><span data-stu-id="ba809-588">A socket operation encountered a dead network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**Wsaumetunreach**</span><span class="sxs-lookup"><span data-stu-id="ba809-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-590">10051 (0x2743)</span><span class="sxs-lookup"><span data-stu-id="ba809-590">10051 (0x2743)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-591">Es wurde versucht, ein Socketvorgang in ein nicht erreichbares Netzwerk auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ba809-591">A socket operation was attempted to an unreachable network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**Wsaenetreset**</span><span class="sxs-lookup"><span data-stu-id="ba809-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-593">10052 (0x2744)</span><span class="sxs-lookup"><span data-stu-id="ba809-593">10052 (0x2744)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-594">Die Verbindung wurde unterbrochen, weil eine Keep-Alive-Aktivität einen Fehler erkannt hat, während der Vorgang ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-594">The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span><span class="sxs-lookup"><span data-stu-id="ba809-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-596">10053 (0x2745)</span><span class="sxs-lookup"><span data-stu-id="ba809-596">10053 (0x2745)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-597">Eine hergestellte Verbindung wurde durch die Software auf dem Hostcomputer abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="ba809-597">An established connection was aborted by the software in your host machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span><span class="sxs-lookup"><span data-stu-id="ba809-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-599">10054 (0x2746)</span><span class="sxs-lookup"><span data-stu-id="ba809-599">10054 (0x2746)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-600">An existing connection was forcibly closed by the remote host.</span><span class="sxs-lookup"><span data-stu-id="ba809-600">An existing connection was forcibly closed by the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="ba809-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-602">10055 (0x2747)</span><span class="sxs-lookup"><span data-stu-id="ba809-602">10055 (0x2747)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-603">Ein Vorgang für einen Socket konnte nicht durchgeführt werden, da das System nicht genügend Pufferspeicher hatte oder weil eine Warteschlange voll war.</span><span class="sxs-lookup"><span data-stu-id="ba809-603">An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**Wsaeisconn**</span><span class="sxs-lookup"><span data-stu-id="ba809-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-605">10056 (0x2748)</span><span class="sxs-lookup"><span data-stu-id="ba809-605">10056 (0x2748)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-606">Eine Verbindungsanforderung wurde an einem bereits verbundenen Socket vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="ba809-606">A connect request was made on an already connected socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**Wsaumotconn**</span><span class="sxs-lookup"><span data-stu-id="ba809-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-608">10057 (0x2749)</span><span class="sxs-lookup"><span data-stu-id="ba809-608">10057 (0x2749)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-609">Eine Anforderung zum Senden oder Empfangen von Daten war unzulässig, weil der Socket nicht verbunden ist und (beim Senden über einen Datagrammsocket mithilfe eines sendto-Aufrufs) keine Adresse bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-609">A request to send or receive data was disallowed because the socket is not connected and (when sending on a datagram socket using a sendto call) no address was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span><span class="sxs-lookup"><span data-stu-id="ba809-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-611">10058 (0x274a)</span><span class="sxs-lookup"><span data-stu-id="ba809-611">10058 (0x274A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-612">Eine Anforderung zum Senden oder Empfangen von Daten wurde nicht zugelassen, da der Socket in die entsprechende Richtung bereits durch einen vorangegangenen shutdown-Aufruf heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-612">A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**Wsaetoomanyrefs**</span><span class="sxs-lookup"><span data-stu-id="ba809-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-614">10059 (0x274b)</span><span class="sxs-lookup"><span data-stu-id="ba809-614">10059 (0x274B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-615">Zu viele Verweise auf ein Kernel Objekt.</span><span class="sxs-lookup"><span data-stu-id="ba809-615">Too many references to some kernel object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="ba809-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-617">10060 (0x274c)</span><span class="sxs-lookup"><span data-stu-id="ba809-617">10060 (0x274C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-618">Ein Verbindungsversuch ist fehlgeschlagen, weil die verbundene Partei nach einem bestimmten Zeitraum nicht ordnungsgemäß reagiert hat, oder eine Verbindung konnte nicht hergestellt werden, da der verbundene Host nicht reagiert hat.</span><span class="sxs-lookup"><span data-stu-id="ba809-618">A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**Wsaeconnabgelehnte**</span><span class="sxs-lookup"><span data-stu-id="ba809-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-620">10061 (0x274d)</span><span class="sxs-lookup"><span data-stu-id="ba809-620">10061 (0x274D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-621">Es konnte keine Verbindung hergestellt werden, da diese vom Zielcomputer aktiv verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-621">No connection could be made because the target machine actively refused it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**Wsaeloop**</span><span class="sxs-lookup"><span data-stu-id="ba809-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-623">10062 (0x274e)</span><span class="sxs-lookup"><span data-stu-id="ba809-623">10062 (0x274E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-624">Der Name kann nicht übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-624">Cannot translate name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**Wsaenametoolong**</span><span class="sxs-lookup"><span data-stu-id="ba809-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-626">10063 (0x274f)</span><span class="sxs-lookup"><span data-stu-id="ba809-626">10063 (0x274F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-627">Die namens Komponente oder der Name ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="ba809-627">Name component or name was too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**Wsaehostdown**</span><span class="sxs-lookup"><span data-stu-id="ba809-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-629">10064 (0x2750)</span><span class="sxs-lookup"><span data-stu-id="ba809-629">10064 (0x2750)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-630">Ein Socketvorgang ist fehlgeschlagen, da der Zielhost ausgefallen ist.</span><span class="sxs-lookup"><span data-stu-id="ba809-630">A socket operation failed because the destination host was down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**Wsaehostunreach**</span><span class="sxs-lookup"><span data-stu-id="ba809-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-632">10065 (0x2751)</span><span class="sxs-lookup"><span data-stu-id="ba809-632">10065 (0x2751)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-633">Versuch eines Socketvorgangs für einen nicht erreichbaren Host.</span><span class="sxs-lookup"><span data-stu-id="ba809-633">A socket operation was attempted to an unreachable host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**Wsaenotempty**</span><span class="sxs-lookup"><span data-stu-id="ba809-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-635">10066 (0x2752)</span><span class="sxs-lookup"><span data-stu-id="ba809-635">10066 (0x2752)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-636">Ein nicht leeres Verzeichnis kann nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-636">Cannot remove a directory that is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**Wsaeproclim**</span><span class="sxs-lookup"><span data-stu-id="ba809-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-638">10067 (0x2753)</span><span class="sxs-lookup"><span data-stu-id="ba809-638">10067 (0x2753)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-639">Eine Windows Sockets-Implementierung kann eine Beschränkung für die Anzahl der Anwendungen aufweisen, die Sie gleichzeitig verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ba809-639">A Windows Sockets implementation may have a limit on the number of applications that may use it simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**Wsaeusers**</span><span class="sxs-lookup"><span data-stu-id="ba809-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-641">10068 (0x2754)</span><span class="sxs-lookup"><span data-stu-id="ba809-641">10068 (0x2754)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-642">Das Kontingent ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="ba809-642">Ran out of quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**Wsaedquot**</span><span class="sxs-lookup"><span data-stu-id="ba809-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-644">10069 (0x2755)</span><span class="sxs-lookup"><span data-stu-id="ba809-644">10069 (0x2755)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-645">Nicht genügend Datenträger Kontingent.</span><span class="sxs-lookup"><span data-stu-id="ba809-645">Ran out of disk quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**Wsaestale**</span><span class="sxs-lookup"><span data-stu-id="ba809-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-647">10070 (0x2756)</span><span class="sxs-lookup"><span data-stu-id="ba809-647">10070 (0x2756)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-648">Der Datei Handle-Verweis ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba809-648">File handle reference is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**Wsaeremote**</span><span class="sxs-lookup"><span data-stu-id="ba809-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-650">10071 (0x2757)</span><span class="sxs-lookup"><span data-stu-id="ba809-650">10071 (0x2757)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-651">Das Element ist nicht lokal verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba809-651">Item is not available locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**Wsasysnotready**</span><span class="sxs-lookup"><span data-stu-id="ba809-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-653">10091 (0x276b)</span><span class="sxs-lookup"><span data-stu-id="ba809-653">10091 (0x276B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-654">WSAStartup funktioniert zurzeit nicht, da das zugrunde liegende System, das zur Bereitstellung von Netzwerkdiensten verwendet wird, zurzeit nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba809-654">WSAStartup cannot function at this time because the underlying system it uses to provide network services is currently unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**Wsavernotsupported**</span><span class="sxs-lookup"><span data-stu-id="ba809-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-656">10092 (0x276c)</span><span class="sxs-lookup"><span data-stu-id="ba809-656">10092 (0x276C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-657">Die angeforderte Windows Sockets-Version wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ba809-657">The Windows Sockets version requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**Wsanotinitialisiert**</span><span class="sxs-lookup"><span data-stu-id="ba809-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-659">10093 (0x276d)</span><span class="sxs-lookup"><span data-stu-id="ba809-659">10093 (0x276D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-660">Entweder hat die Anwendung nicht WSAStartup aufgerufen, oder WSAStartup ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="ba809-660">Either the application has not called WSAStartup, or WSAStartup failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**Wsaediscon**</span><span class="sxs-lookup"><span data-stu-id="ba809-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-662">10101 (0x2775)</span><span class="sxs-lookup"><span data-stu-id="ba809-662">10101 (0x2775)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-663">Wird von WSARecv oder WSARecvFrom zurückgegeben, um anzugeben, dass die Remote Partei eine ordnungsgemäße Herunterfahr Sequenz initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="ba809-663">Returned by WSARecv or WSARecvFrom to indicate the remote party has initiated a graceful shutdown sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**Wsaeromore**</span><span class="sxs-lookup"><span data-stu-id="ba809-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-665">10102 (0x2776)</span><span class="sxs-lookup"><span data-stu-id="ba809-665">10102 (0x2776)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-666">Von WSALookupServiceNext können keine weiteren Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-666">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**Wsaecancelled**</span><span class="sxs-lookup"><span data-stu-id="ba809-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-668">10103 (0x2777)</span><span class="sxs-lookup"><span data-stu-id="ba809-668">10103 (0x2777)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-669">Es wurde ein WSALookupServiceEnd aufgerufen, während dieser Rückruf noch verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-669">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="ba809-670">Der-Rückruf wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="ba809-670">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**Wsaeinvalidproctable**</span><span class="sxs-lookup"><span data-stu-id="ba809-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-672">10104 (0x2778)</span><span class="sxs-lookup"><span data-stu-id="ba809-672">10104 (0x2778)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-673">Die Prozedur "calltable" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ba809-673">The procedure call table is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**Wsaeinvalidprovider**</span><span class="sxs-lookup"><span data-stu-id="ba809-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-675">10105 (0x2779)</span><span class="sxs-lookup"><span data-stu-id="ba809-675">10105 (0x2779)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-676">Der angeforderte Dienstanbieter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ba809-676">The requested service provider is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**Wsaeproviderfailedinit**</span><span class="sxs-lookup"><span data-stu-id="ba809-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-678">10106 (0x277a)</span><span class="sxs-lookup"><span data-stu-id="ba809-678">10106 (0x277A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-679">Der angeforderte Dienstanbieter konnte nicht geladen oder initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-679">The requested service provider could not be loaded or initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span><span class="sxs-lookup"><span data-stu-id="ba809-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-681">10107 (0x277b)</span><span class="sxs-lookup"><span data-stu-id="ba809-681">10107 (0x277B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-682">Fehler beim System Aufruf.</span><span class="sxs-lookup"><span data-stu-id="ba809-682">A system call has failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**wsaservice \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-684">10108 (0x277c)</span><span class="sxs-lookup"><span data-stu-id="ba809-684">10108 (0x277C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-685">Dieser Dienst ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="ba809-685">No such service is known.</span></span> <span data-ttu-id="ba809-686">Der Dienst wurde im angegebenen Namespace nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-686">The service cannot be found in the specified name space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**wsatype \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="ba809-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-688">10109 (0x277d)</span><span class="sxs-lookup"><span data-stu-id="ba809-688">10109 (0x277D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-689">Die angegebene Klasse wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-689">The specified class was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ nicht \_ mehr**</span><span class="sxs-lookup"><span data-stu-id="ba809-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA\_E\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-691">10110 (0x277e)</span><span class="sxs-lookup"><span data-stu-id="ba809-691">10110 (0x277E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-692">Von WSALookupServiceNext können keine weiteren Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-692">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="ba809-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA\_E\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-694">10111 (0x277f)</span><span class="sxs-lookup"><span data-stu-id="ba809-694">10111 (0x277F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-695">Es wurde ein WSALookupServiceEnd aufgerufen, während dieser Rückruf noch verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-695">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="ba809-696">Der-Rückruf wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="ba809-696">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**Wsaerefused**</span><span class="sxs-lookup"><span data-stu-id="ba809-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-698">10112 (0x2780)</span><span class="sxs-lookup"><span data-stu-id="ba809-698">10112 (0x2780)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-699">Eine Datenbankabfrage ist fehlgeschlagen, da Sie aktiv abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba809-699">A database query failed because it was actively refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**wsahost \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-701">11001 (0x2af9)</span><span class="sxs-lookup"><span data-stu-id="ba809-701">11001 (0x2AF9)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-702">Ein solcher Host ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="ba809-702">No such host is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**wsatry \_ erneut**</span><span class="sxs-lookup"><span data-stu-id="ba809-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-704">11002 (0x2afa)</span><span class="sxs-lookup"><span data-stu-id="ba809-704">11002 (0x2AFA)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-705">Hierbei handelt es sich in der Regel um einen temporären Fehler, der während der Auflösung von Hostnamen auftritt und einen Hinweis darauf liefert, dass der lokale Server keine Antwort von einem autorisierenden Server erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="ba809-705">This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**wsano- \_ Wiederherstellung**</span><span class="sxs-lookup"><span data-stu-id="ba809-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-707">11003 (0x2afb)</span><span class="sxs-lookup"><span data-stu-id="ba809-707">11003 (0x2AFB)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-708">Beim Datenbankaufruf ist ein nicht behebbarer Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ba809-708">A non-recoverable error occurred during a database lookup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**wsano- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="ba809-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-710">11004 (0x2afc)</span><span class="sxs-lookup"><span data-stu-id="ba809-710">11004 (0x2AFC)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-711">Der angeforderte Name ist gültig, aber es wurden keine Daten vom angeforderten Typ gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-711">The requested name is valid, but no data of the requested type was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA- \_ QoS- \_ Empfänger**</span><span class="sxs-lookup"><span data-stu-id="ba809-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA\_QOS\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-713">11005 (0x2afd)</span><span class="sxs-lookup"><span data-stu-id="ba809-713">11005 (0x2AFD)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-714">Mindestens eine Reserve ist eingetroffen.</span><span class="sxs-lookup"><span data-stu-id="ba809-714">At least one reserve has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA- \_ QoS- \_ Sender**</span><span class="sxs-lookup"><span data-stu-id="ba809-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA\_QOS\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-716">11006 (0x2afe)</span><span class="sxs-lookup"><span data-stu-id="ba809-716">11006 (0x2AFE)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-717">Mindestens ein Pfad ist eingetroffen.</span><span class="sxs-lookup"><span data-stu-id="ba809-717">At least one path has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA \_ QoS \_ No \_ Absenders**</span><span class="sxs-lookup"><span data-stu-id="ba809-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA\_QOS\_NO\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-719">11007 (0x2aff)</span><span class="sxs-lookup"><span data-stu-id="ba809-719">11007 (0x2AFF)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-720">Es sind keine Absender vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-720">There are no senders.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA- \_ QoS \_ keine \_ Empfänger**</span><span class="sxs-lookup"><span data-stu-id="ba809-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA\_QOS\_NO\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-722">11008 (0x2b00)</span><span class="sxs-lookup"><span data-stu-id="ba809-722">11008 (0x2B00)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-723">Es sind keine Empfänger vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ba809-723">There are no receivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA- \_ QoS- \_ Anforderung \_ bestätigt**</span><span class="sxs-lookup"><span data-stu-id="ba809-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA\_QOS\_REQUEST\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-725">11009 (0x2b01)</span><span class="sxs-lookup"><span data-stu-id="ba809-725">11009 (0x2B01)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-726">Reserve wurde bestätigt.</span><span class="sxs-lookup"><span data-stu-id="ba809-726">Reserve has been confirmed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA- \_ QoS- \_ Eintritts \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA\_QOS\_ADMISSION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-728">11010 (0x2b02)</span><span class="sxs-lookup"><span data-stu-id="ba809-728">11010 (0x2B02)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-729">Fehler aufgrund fehlender Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ba809-729">Error due to lack of resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**Fehler bei WSA- \_ QoS- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="ba809-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA\_QOS\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-731">11011 (0x2b03)</span><span class="sxs-lookup"><span data-stu-id="ba809-731">11011 (0x2B03)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-732">Aus administrativen Gründen abgelehnt-ungültige Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="ba809-732">Rejected for administrative reasons - bad credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**Ungültiger WSA- \_ QoS- \_ \_ Stil**</span><span class="sxs-lookup"><span data-stu-id="ba809-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA\_QOS\_BAD\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-734">11012 (0x2b04)</span><span class="sxs-lookup"><span data-stu-id="ba809-734">11012 (0x2B04)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-735">Unbekannter oder in Konflikt stehender Stil.</span><span class="sxs-lookup"><span data-stu-id="ba809-735">Unknown or conflicting style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**Ungültiges WSA- \_ QoS- \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="ba809-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA\_QOS\_BAD\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-737">11013 (0x2b05)</span><span class="sxs-lookup"><span data-stu-id="ba809-737">11013 (0x2B05)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-738">Problem mit einem Teil des FILTERSPEC-oder ProviderSpecific-Puffers im Allgemeinen.</span><span class="sxs-lookup"><span data-stu-id="ba809-738">Problem with some part of the filterspec or providerspecific buffer in general.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA- \_ QoS- \_ Datenverkehr \_ STRG- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA\_QOS\_TRAFFIC\_CTRL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-740">11014 (0x2b06)</span><span class="sxs-lookup"><span data-stu-id="ba809-740">11014 (0x2B06)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-741">Problem mit einem Teil der Flowspec.</span><span class="sxs-lookup"><span data-stu-id="ba809-741">Problem with some part of the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**allgemeiner WSA- \_ QoS- \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA\_QOS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-743">11015 (0x2b07)</span><span class="sxs-lookup"><span data-stu-id="ba809-743">11015 (0x2B07)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-744">Allgemeiner QOS-Fehler.</span><span class="sxs-lookup"><span data-stu-id="ba809-744">General QOS error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA \_ QoS \_ eservicetype**</span><span class="sxs-lookup"><span data-stu-id="ba809-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA\_QOS\_ESERVICETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-746">11016 (0x2b08)</span><span class="sxs-lookup"><span data-stu-id="ba809-746">11016 (0x2B08)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-747">In der Flowspec wurde ein ungültiger oder unbekannter Diensttyp gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-747">An invalid or unrecognized service type was found in the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA- \_ QoS- \_ eflowspec**</span><span class="sxs-lookup"><span data-stu-id="ba809-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA\_QOS\_EFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-749">11017 (0x2b09)</span><span class="sxs-lookup"><span data-stu-id="ba809-749">11017 (0x2B09)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-750">In der QoS-Struktur wurde eine ungültige oder inkonsistente Flowspec gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-750">An invalid or inconsistent flowspec was found in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA \_ QoS \_ eprovspecbuf**</span><span class="sxs-lookup"><span data-stu-id="ba809-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA\_QOS\_EPROVSPECBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-752">11018 (0x2b0a)</span><span class="sxs-lookup"><span data-stu-id="ba809-752">11018 (0x2B0A)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-753">Ungültiger QoS-Anbieter spezifischer Puffer.</span><span class="sxs-lookup"><span data-stu-id="ba809-753">Invalid QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA \_ QoS \_ efilterstyle**</span><span class="sxs-lookup"><span data-stu-id="ba809-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA\_QOS\_EFILTERSTYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-755">11019 (0x2b0b)</span><span class="sxs-lookup"><span data-stu-id="ba809-755">11019 (0x2B0B)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-756">Es wurde ein ungültiger QoS-Filter Stil verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba809-756">An invalid QOS filter style was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA- \_ QoS \_ efiltertype**</span><span class="sxs-lookup"><span data-stu-id="ba809-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA\_QOS\_EFILTERTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-758">11020 (0x2b0c)</span><span class="sxs-lookup"><span data-stu-id="ba809-758">11020 (0x2B0C)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-759">Es wurde ein ungültiger QoS-Filtertyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba809-759">An invalid QOS filter type was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA- \_ QoS- \_ efiltercount**</span><span class="sxs-lookup"><span data-stu-id="ba809-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA\_QOS\_EFILTERCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-761">11021 (0x2b0d)</span><span class="sxs-lookup"><span data-stu-id="ba809-761">11021 (0x2B0D)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-762">Im FLOWDESCRIPTOR wurde eine falsche Anzahl von QoS-FILTERSPECs angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba809-762">An incorrect number of QOS FILTERSPECs were specified in the FLOWDESCRIPTOR.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA- \_ QoS \_ eobjlength**</span><span class="sxs-lookup"><span data-stu-id="ba809-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA\_QOS\_EOBJLENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-764">11022 (0x2b0e)</span><span class="sxs-lookup"><span data-stu-id="ba809-764">11022 (0x2B0E)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-765">Im anbieterspezifischen QoS-Puffer wurde ein Objekt mit einem ungültigen objectlength-Feld angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba809-765">An object with an invalid ObjectLength field was specified in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA- \_ QoS- \_ eflowcount**</span><span class="sxs-lookup"><span data-stu-id="ba809-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA\_QOS\_EFLOWCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-767">11023 (0x2b0f)</span><span class="sxs-lookup"><span data-stu-id="ba809-767">11023 (0x2B0F)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-768">In der QoS-Struktur wurde eine falsche Anzahl von Fluss Deskriptoren angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba809-768">An incorrect number of flow descriptors was specified in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA \_ QoS \_ eunkownpsobj**</span><span class="sxs-lookup"><span data-stu-id="ba809-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA\_QOS\_EUNKOWNPSOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-770">11024 (0x2b10)</span><span class="sxs-lookup"><span data-stu-id="ba809-770">11024 (0x2B10)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-771">Ein unbekanntes Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-771">An unrecognized object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA \_ QoS \_ epolicyobj**</span><span class="sxs-lookup"><span data-stu-id="ba809-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA\_QOS\_EPOLICYOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-773">11025 (0x2b11)</span><span class="sxs-lookup"><span data-stu-id="ba809-773">11025 (0x2B11)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-774">Ein ungültiges Richtlinien Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-774">An invalid policy object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA \_ QoS \_ eflowde**</span><span class="sxs-lookup"><span data-stu-id="ba809-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA\_QOS\_EFLOWDESC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-776">11026 (0x2b12)</span><span class="sxs-lookup"><span data-stu-id="ba809-776">11026 (0x2B12)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-777">In der Liste der flowdeskriptoren wurde ein ungültiger QoS-Datenfluss Deskriptor gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-777">An invalid QOS flow descriptor was found in the flow descriptor list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA \_ QoS \_ epsflowspec**</span><span class="sxs-lookup"><span data-stu-id="ba809-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA\_QOS\_EPSFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-779">11027 (0x2b13)</span><span class="sxs-lookup"><span data-stu-id="ba809-779">11027 (0x2B13)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-780">Im QoS-anbieterspezifischen Puffer wurde eine ungültige oder inkonsistente Flowspec gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-780">An invalid or inconsistent flowspec was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA \_ QoS \_ epsfilterspec**</span><span class="sxs-lookup"><span data-stu-id="ba809-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA\_QOS\_EPSFILTERSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-782">11028 (0x2b14)</span><span class="sxs-lookup"><span data-stu-id="ba809-782">11028 (0x2B14)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-783">Im QoS-anbieterspezifischen Puffer wurde eine ungültige FILTERSPEC gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-783">An invalid FILTERSPEC was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA \_ QoS \_ esdmodeobj**</span><span class="sxs-lookup"><span data-stu-id="ba809-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA\_QOS\_ESDMODEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-785">11029 (0x2b15)</span><span class="sxs-lookup"><span data-stu-id="ba809-785">11029 (0x2B15)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-786">Ein ungültiges Shape-Verwerfungs Modus-Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-786">An invalid shape discard mode object was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA \_ QoS \_ eshaperateobj**</span><span class="sxs-lookup"><span data-stu-id="ba809-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA\_QOS\_ESHAPERATEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-788">11030 (0x2b16)</span><span class="sxs-lookup"><span data-stu-id="ba809-788">11030 (0x2B16)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-789">Ein ungültiges Strukturierungs Raten Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-789">An invalid shaping rate object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**reservierter "WSA \_ QoS"- \_ Peer- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="ba809-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA\_QOS\_RESERVED\_PETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-791">11031 (0x2b17)</span><span class="sxs-lookup"><span data-stu-id="ba809-791">11031 (0x2B17)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-792">Ein reserviertes Policy-Element wurde im QoS-anbieterspezifischen Puffer gefunden.</span><span class="sxs-lookup"><span data-stu-id="ba809-792">A reserved policy element was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**der sichere WSA- \_ \_ Host wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="ba809-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**WSA\_SECURE\_HOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-794">11032 (0x2b18)</span><span class="sxs-lookup"><span data-stu-id="ba809-794">11032 (0x2B18)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-795">Ein solcher Host ist nicht sicher bekannt.</span><span class="sxs-lookup"><span data-stu-id="ba809-795">No such host is known securely.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ba809-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA- \_ IPSec- \_ namens \_ Richtlinien \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ba809-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA\_IPSEC\_NAME\_POLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba809-797">11033 (0x2b19)</span><span class="sxs-lookup"><span data-stu-id="ba809-797">11033 (0x2B19)</span></span>
</dt> <dt>



<span data-ttu-id="ba809-798">Die namensbasierte IPSec-Richtlinie konnte nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ba809-798">Name based IPSEC policy could not be added.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="ba809-799">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba809-799">Requirements</span></span>



| <span data-ttu-id="ba809-800">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba809-800">Requirement</span></span> | <span data-ttu-id="ba809-801">Wert</span><span class="sxs-lookup"><span data-stu-id="ba809-801">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba809-802">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba809-802">Minimum supported client</span></span><br/> | <span data-ttu-id="ba809-803">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba809-803">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ba809-804">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba809-804">Minimum supported server</span></span><br/> | <span data-ttu-id="ba809-805">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba809-805">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba809-806">Header</span><span class="sxs-lookup"><span data-stu-id="ba809-806">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba809-807"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba809-807"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba809-808">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba809-808">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba809-809">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="ba809-809">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




