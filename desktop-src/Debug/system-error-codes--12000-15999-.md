---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 12000-1599 und ist für Entwickler bestimmt.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: System Fehler Codes (12000-15999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483323"
---
# <a name="system-error-codes-12000-15999"></a><span data-ttu-id="6ed93-103">System Fehler Codes (12000-15999)</span><span class="sxs-lookup"><span data-stu-id="6ed93-103">System Error Codes (12000-15999)</span></span>

> [!NOTE]
> <span data-ttu-id="6ed93-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="6ed93-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed93-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="6ed93-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 12000 bis 15999) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6ed93-106">The following list describes [system error codes](system-error-codes.md) (errors 12000 to 15999).</span></span> <span data-ttu-id="6ed93-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="6ed93-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="6ed93-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="6ed93-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**Fehler \_ \_Internet \** _</span><span class="sxs-lookup"><span data-stu-id="6ed93-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**ERROR\_INTERNET\_\** _</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-110">12000-12175 (0x2ee0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-110">12000 - 12175 (0x2EE0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-111">Weitere Informationen finden Sie unter [Internet-Fehler Codes](../wininet/wininet-errors.md) und Wininet. h.</span><span class="sxs-lookup"><span data-stu-id="6ed93-111">See [Internet Error Codes](../wininet/wininet-errors.md) and WinInet.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *Fehler \_ IPSec- \_ qm- \_ Richtlinie \_ vorhanden*\*</span><span class="sxs-lookup"><span data-stu-id="6ed93-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *ERROR\_IPSEC\_QM\_POLICY\_EXISTS*\*</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-113">13000 (0x32c8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-113">13000 (0x32C8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-114">Die angegebene Schnellmodus-Richtlinie ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-114">The specified quick mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**Fehler bei \_ IPSec- \_ qm- \_ Richtlinie \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR\_IPSEC\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-116">13001 (0x32c9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-116">13001 (0x32C9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-117">Die angegebene Schnellmodus-Richtlinie wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-117">The specified quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**Fehler \_ \_ \_ \_ beim \_ Verwenden der IPSec-qm-Richtlinie.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR\_IPSEC\_QM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-119">13002 (0x32ca)</span><span class="sxs-lookup"><span data-stu-id="6ed93-119">13002 (0x32CA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-120">Die angegebene Schnellmodus-Richtlinie wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-120">The specified quick mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**Fehler \_ IPSec \_ mm- \_ Richtlinie \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="6ed93-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR\_IPSEC\_MM\_POLICY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-122">13003 (0x32cb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-122">13003 (0x32CB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-123">Die angegebene Hauptmodusrichtlinie ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-123">The specified main mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**Fehler bei \_ IPSec \_ mm- \_ Richtlinie \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR\_IPSEC\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-125">13004 (0x32cc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-125">13004 (0x32CC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-126">Die angegebene Hauptmodusrichtlinie wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-126">The specified main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**Fehler \_ bei IPSec \_ mm- \_ Richtlinie wird \_ \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="6ed93-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR\_IPSEC\_MM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-128">13005 (0x32cd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-128">13005 (0x32CD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-129">Die angegebene Hauptmodusrichtlinie wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-129">The specified main mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**Fehler \_ IPSec \_ mm- \_ Filter \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="6ed93-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR\_IPSEC\_MM\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-131">13006 (0x32ce)</span><span class="sxs-lookup"><span data-stu-id="6ed93-131">13006 (0x32CE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-132">Der angegebene Hauptmodusfilter ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-132">The specified main mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**Fehler \_ IPSec \_ mm- \_ Filter wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR\_IPSEC\_MM\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-134">13007 (0x32cf)</span><span class="sxs-lookup"><span data-stu-id="6ed93-134">13007 (0x32CF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-135">Der angegebene Hauptmodusfilter wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-135">The specified main mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**\_IPSec- \_ Transport \_ Filter ist \_ bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-137">13008 (0x32d0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-137">13008 (0x32D0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-138">Der angegebene Transportmodus-Filter ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-138">The specified transport mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**Fehler beim \_ IPSec- \_ Transport \_ Filter \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-140">13009 (0x32d1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-140">13009 (0x32D1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-141">Der angegebene Transportmodus-Filter ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-141">The specified transport mode filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**Fehler bei \_ IPSec-mm-Authentifizierung \_ \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR\_IPSEC\_MM\_AUTH\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-143">13010 (0x32d2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-143">13010 (0x32D2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-144">Die angegebene hauptmodusauthentifizierungsliste ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-144">The specified main mode authentication list exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**Fehler bei \_ IPSec-mm-Authentifizierung \_ \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR\_IPSEC\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-146">13011 (0x32d3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-146">13011 (0x32D3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-147">Die angegebene hauptmodusauthentifizierungsliste wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-147">The specified main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**Fehler \_ bei IPSec mm-Authentifizierung wird \_ \_ \_ \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR\_IPSEC\_MM\_AUTH\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-149">13012 (0x32d4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-149">13012 (0x32D4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-150">Die angegebene hauptmodusauthentifizierungsliste wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-150">The specified main mode authentication list is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**Fehler \_ IPSec- \_ Standard- \_ mm- \_ Richtlinie \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="6ed93-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-152">13013 (0x32d5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-152">13013 (0x32D5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-153">Die angegebene standardmäßige Hauptmodus-Richtlinie wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-153">The specified default main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**Fehler bei \_ IPSec-Standard-mm-Authentifizierung \_ \_ \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-155">13014 (0x32d6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-155">13014 (0x32D6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-156">Die angegebene Standard Authentifizierung im hauptmodusmodus wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-156">The specified default main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**Fehler bei \_ IPSec- \_ Standard- \_ \_ Richtlinie "qm \_ \_ "**</span><span class="sxs-lookup"><span data-stu-id="6ed93-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-158">13015 (0x32d7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-158">13015 (0x32D7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-159">Die angegebene standardmäßige Schnellmodus-Richtlinie wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-159">The specified default quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**Fehler \_ IPSec- \_ Tunnel \_ Filter \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="6ed93-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-161">13016 (0x32d8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-161">13016 (0x32D8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-162">Der angegebene Tunnel Modus-Filter ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-162">The specified tunnel mode filter exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**Fehler beim \_ IPSec- \_ Tunnel \_ Filter wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-164">13017 (0x32d9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-164">13017 (0x32D9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-165">Der angegebene Tunnel Modus-Filter wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-165">The specified tunnel mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**Fehler \_ IPSec \_ mm \_ Filter \_ ausstehende \_ Löschung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR\_IPSEC\_MM\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-167">13018 (0x32da)</span><span class="sxs-lookup"><span data-stu-id="6ed93-167">13018 (0x32DA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-168">Der Hauptmodusfilter steht für den Löschvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-168">The Main Mode filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**Fehler beim \_ Löschen des IPSec- \_ Transport \_ Filters \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-170">13019 (0x32db)</span><span class="sxs-lookup"><span data-stu-id="6ed93-170">13019 (0x32DB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-171">Das Löschen des Transport Filters steht aus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-171">The transport filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**Fehler bei \_ IPSec- \_ Tunnel \_ Filter \_ ausstehende \_ Löschung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-173">13020 (0x32dc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-173">13020 (0x32DC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-174">Das Löschen des Tunnel Filters steht aus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-174">The tunnel filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**Fehler beim \_ Löschen der IPSec \_ mm- \_ Richtlinie \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR\_IPSEC\_MM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-176">13021 (0x32dd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-176">13021 (0x32DD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-177">Die Hauptmodusrichtlinie steht für den Löschvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-177">The Main Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**Fehler beim \_ Löschen der IPSec mm-Authentifizierung \_ \_ . \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR\_IPSEC\_MM\_AUTH\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-179">13022 (0x32de)</span><span class="sxs-lookup"><span data-stu-id="6ed93-179">13022 (0x32DE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-180">Das hauptmodusauthentifizierungs-Bundle steht für den Löschvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-180">The Main Mode authentication bundle is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**Fehler beim \_ Löschen der IPSec- \_ qm- \_ Richtlinie \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR\_IPSEC\_QM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-182">13023 (0x32df)</span><span class="sxs-lookup"><span data-stu-id="6ed93-182">13023 (0x32DF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-183">Das Löschen der Schnellmodus-Richtlinie steht aus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-183">The Quick Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**Warnung bei \_ IPSec- \_ mm- \_ Richtlinie \_ wurde gelöscht**</span><span class="sxs-lookup"><span data-stu-id="6ed93-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNING\_IPSEC\_MM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-185">13024 (0x32e0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-185">13024 (0x32E0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-186">Die Hauptmodus-Richtlinie wurde erfolgreich hinzugefügt, einige der angeforderten Angebote werden jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-186">The Main Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**Warnung bei \_ IPSec- \_ qm- \_ Richtlinie \_ wurde gelöscht**</span><span class="sxs-lookup"><span data-stu-id="6ed93-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNING\_IPSEC\_QM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-188">13025 (0x32e1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-188">13025 (0x32E1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-189">Die Schnellmodus-Richtlinie wurde erfolgreich hinzugefügt, einige der angeforderten Angebote werden jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-189">The Quick Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="6ed93-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-191">13800 (0x35e8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-191">13800 (0x35E8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-192">Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Begin</span><span class="sxs-lookup"><span data-stu-id="6ed93-192">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**Fehler bei \_ IPSec- \_ IKE-Authentifizierung \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR\_IPSEC\_IKE\_AUTH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-194">13801 (0x35e9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-194">13801 (0x35E9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-195">Die Anmelde Informationen für die IKE-Authentifizierung sind unzulässig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-195">IKE authentication credentials are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**Fehler bei \_ IPSec \_ IKE \_ atzb \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR\_IPSEC\_IKE\_ATTRIB\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-197">13802 (0x35ea)</span><span class="sxs-lookup"><span data-stu-id="6ed93-197">13802 (0x35EA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-198">IKE-Sicherheits Attribute sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-198">IKE security attributes are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Aushandlung \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="6ed93-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-200">13803 (0x35eb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-200">13803 (0x35EB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-201">Die IKE-Aushandlung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-201">IKE Negotiation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**Fehler bei \_ IPSec- \_ IKE \_ allgemeine \_ Verarbeitungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR\_IPSEC\_IKE\_GENERAL\_PROCESSING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-203">13804 (0x35ec)</span><span class="sxs-lookup"><span data-stu-id="6ed93-203">13804 (0x35EC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-204">Allgemeiner Verarbeitungsfehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-204">General processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**Fehler bei \_ IPSec- \_ IKE. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR\_IPSEC\_IKE\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-206">13805 (0x35ed)</span><span class="sxs-lookup"><span data-stu-id="6ed93-206">13805 (0x35ED)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-207">Timeout bei der Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-207">Negotiation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="6ed93-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-209">13806 (0x35ee)</span><span class="sxs-lookup"><span data-stu-id="6ed93-209">13806 (0x35EE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-210">IKE konnte ein gültiges Computer Zertifikat nicht finden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-210">IKE failed to find valid machine certificate.</span></span> <span data-ttu-id="6ed93-211">Wenden Sie sich an den Netzwerk Sicherheits Administrator, um ein gültiges Zertifikat im entsprechenden Zertifikat Speicher zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6ed93-211">Contact your Network Security Administrator about installing a valid certificate in the appropriate Certificate Store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**Fehler \_ IPSec- \_ IKE- \_ sa \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="6ed93-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR\_IPSEC\_IKE\_SA\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-213">13807 (0x35ef)</span><span class="sxs-lookup"><span data-stu-id="6ed93-213">13807 (0x35EF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-214">Die IKE-SA wurde vor dem Abschluss des Vorgangs von Peer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-214">IKE SA deleted by peer before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**Fehler beim Wiedergeben von \_ IPSec- \_ IKE. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR\_IPSEC\_IKE\_SA\_REAPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-216">13808 (0x35f 0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-216">13808 (0x35F0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-217">Die IKE-SA wurde vor Abschluss der Einrichtung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-217">IKE SA deleted before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**Fehler \_ IPSec \_ IKE \_ mm \_ Abrufen \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-219">13809 (0x35f 1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-219">13809 (0x35F1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-220">Die Aushandlungs Anforderung ist zu lang in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6ed93-220">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**Fehler beim Abrufen von " \_ IPSec \_ IKE \_ qm \_ \_ ".**</span><span class="sxs-lookup"><span data-stu-id="6ed93-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-222">13810 (0x35f 2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-222">13810 (0x35F2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-223">Die Aushandlungs Anforderung ist zu lang in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6ed93-223">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**Fehler beim \_ Löschen der IPSec- \_ IKE- \_ Warteschlange \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-225">13811 (0x35f 3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-225">13811 (0x35F3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-226">Die Aushandlungs Anforderung ist zu lang in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6ed93-226">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**Fehler \_ IPSec \_ IKE \_ Queue \_ Drop \_ No \_ mm**</span><span class="sxs-lookup"><span data-stu-id="6ed93-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_NO\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-228">13812 (0x35f 4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-228">13812 (0x35F4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-229">Die Aushandlungs Anforderung ist zu lang in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6ed93-229">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**Fehler \_ IPSec \_ IKE \_ Drop \_ No \_ Response**</span><span class="sxs-lookup"><span data-stu-id="6ed93-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR\_IPSEC\_IKE\_DROP\_NO\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-231">13813 (0x35f 5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-231">13813 (0x35F5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-232">Keine Antwort vom Peer.</span><span class="sxs-lookup"><span data-stu-id="6ed93-232">No response from peer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**Fehler \_ IPSec \_ IKE \_ mm \_ Delay \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="6ed93-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-234">13814 (0x35f 6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-234">13814 (0x35F6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-235">Die Aushandlung hat zu lange gedauert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-235">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**Fehler bei \_ IPSec \_ IKE \_ qm \_ Delay \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="6ed93-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-237">13815 (0x35f 7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-237">13815 (0x35F7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-238">Die Aushandlung hat zu lange gedauert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-238">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**Fehler \_ IPSec- \_ IKE- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR\_IPSEC\_IKE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-240">13816 (0x35f 8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-240">13816 (0x35F8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-241">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-241">Unknown error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**Fehler bei \_ IPSec- \_ IKE- \_ CRL. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR\_IPSEC\_IKE\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-243">13817 (0x35f 9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-243">13817 (0x35F9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-244">Fehler bei der Zertifikat Sperr Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-244">Certificate Revocation Check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ Schlüssel \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR\_IPSEC\_IKE\_INVALID\_KEY\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-246">13818 (0x35fa)</span><span class="sxs-lookup"><span data-stu-id="6ed93-246">13818 (0x35FA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-247">Ungültige Zertifikat Schlüssel Verwendung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-247">Invalid certificate key usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**Fehler \_ IPSec \_ IKE \_ ungültiger \_ CERT- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="6ed93-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-249">13819 (0x35fb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-249">13819 (0x35FB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-250">Ungültiger Zertifikattyp.</span><span class="sxs-lookup"><span data-stu-id="6ed93-250">Invalid certificate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ privater \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="6ed93-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-252">13820 (0x35fc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-252">13820 (0x35FC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-253">Fehler bei der IKE-Aushandlung, weil das verwendete Computer Zertifikat keinen privaten Schlüssel besitzt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-253">IKE negotiation failed because the machine certificate used does not have a private key.</span></span> <span data-ttu-id="6ed93-254">Für IPSec-Zertifikate ist ein privater Schlüssel erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ed93-254">IPsec certificates require a private key.</span></span> <span data-ttu-id="6ed93-255">Wenden Sie sich an den Netzwerk Sicherheitsadministrator, um durch ein Zertifikat mit einem privaten Schlüssel zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-255">Contact your Network Security administrator about replacing with a certificate that has a private key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**Fehler beim \_ \_ \_ gleichzeitigen \_ erneuten Schlüssel für IPSec-IKE**</span><span class="sxs-lookup"><span data-stu-id="6ed93-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR\_IPSEC\_IKE\_SIMULTANEOUS\_REKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-257">13821 (0x35fd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-257">13821 (0x35FD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-258">Gleichzeitige rekeys wurden erkannt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-258">Simultaneous rekeys were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**Fehler \_ IPSec \_ IKE \_ dh \_ fehlschlägt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR\_IPSEC\_IKE\_DH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-260">13822 (0x35fe)</span><span class="sxs-lookup"><span data-stu-id="6ed93-260">13822 (0x35FE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-261">Fehler bei der Diffie-Hellman Berechnung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-261">Failure in Diffie-Hellman computation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**Fehler " \_ IPSec \_ IKE \_ Critical Payload" wurde \_ \_ nicht \_ erkannt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR\_IPSEC\_IKE\_CRITICAL\_PAYLOAD\_NOT\_RECOGNIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-263">13823 (0x35ff)</span><span class="sxs-lookup"><span data-stu-id="6ed93-263">13823 (0x35FF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-264">Sie wissen nicht, wie Sie eine kritische Nutzlast verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-264">Don't know how to process critical payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**Fehler " \_ IPSec \_ IKE- \_ ungültige \_ Kopfzeile"**</span><span class="sxs-lookup"><span data-stu-id="6ed93-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-266">13824 (0x3600)</span><span class="sxs-lookup"><span data-stu-id="6ed93-266">13824 (0x3600)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-267">Ungültiger Header.</span><span class="sxs-lookup"><span data-stu-id="6ed93-267">Invalid header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**Fehler \_ IPSec \_ IKE \_ keine \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="6ed93-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-269">13825 (0x3601)</span><span class="sxs-lookup"><span data-stu-id="6ed93-269">13825 (0x3601)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-270">Keine Richtlinie konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-270">No policy configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ Signatur.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-272">13826 (0x3602)</span><span class="sxs-lookup"><span data-stu-id="6ed93-272">13826 (0x3602)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-273">Fehler beim Überprüfen der Signatur.</span><span class="sxs-lookup"><span data-stu-id="6ed93-273">Failed to verify signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Kerberos- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR\_IPSEC\_IKE\_KERBEROS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-275">13827 (0x3603)</span><span class="sxs-lookup"><span data-stu-id="6ed93-275">13827 (0x3603)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-276">Fehler beim Authentifizieren mithilfe von Kerberos.</span><span class="sxs-lookup"><span data-stu-id="6ed93-276">Failed to authenticate using Kerberos.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ öffentlicher \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="6ed93-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PUBLIC\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-278">13828 (0x3604)</span><span class="sxs-lookup"><span data-stu-id="6ed93-278">13828 (0x3604)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-279">Das Zertifikat des Peers enthielt keinen öffentlichen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6ed93-279">Peer's certificate did not have a public key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**Fehler \_ IPSec- \_ IKE- \_ Prozess \_ Err**</span><span class="sxs-lookup"><span data-stu-id="6ed93-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-281">13829 (0x3605)</span><span class="sxs-lookup"><span data-stu-id="6ed93-281">13829 (0x3605)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-282">Fehler beim Verarbeiten der Fehler Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-282">Error processing error payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**Fehler \_ IPSec \_ IKE \_ Prozess \_ Err \_ sa**</span><span class="sxs-lookup"><span data-stu-id="6ed93-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-284">13830 (0x3606)</span><span class="sxs-lookup"><span data-stu-id="6ed93-284">13830 (0x3606)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-285">Fehler beim Verarbeiten der SA-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-285">Error processing SA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err \_ Prop**</span><span class="sxs-lookup"><span data-stu-id="6ed93-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_PROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-287">13831 (0x3607)</span><span class="sxs-lookup"><span data-stu-id="6ed93-287">13831 (0x3607)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-288">Fehler beim Verarbeiten der nutzungsnutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-288">Error processing Proposal payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ Trans**</span><span class="sxs-lookup"><span data-stu-id="6ed93-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_TRANS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-290">13832 (0x3608)</span><span class="sxs-lookup"><span data-stu-id="6ed93-290">13832 (0x3608)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-291">Fehler beim Verarbeiten der Transform-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-291">Error processing Transform payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ KE**</span><span class="sxs-lookup"><span data-stu-id="6ed93-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_KE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-293">13833 (0x3609)</span><span class="sxs-lookup"><span data-stu-id="6ed93-293">13833 (0x3609)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-294">Fehler beim Verarbeiten der KE-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-294">Error processing KE payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**Fehler bei \_ IPSec \_ IKE- \_ Prozess-Err- \_ \_ ID**</span><span class="sxs-lookup"><span data-stu-id="6ed93-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-296">13834 (0x360a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-296">13834 (0x360A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-297">Fehler beim Verarbeiten der ID-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-297">Error processing ID payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="6ed93-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-299">13835 (0x360b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-299">13835 (0x360B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-300">Fehler beim Verarbeiten der Zertifikat Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-300">Error processing Cert payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err \_ CERT \_ req**</span><span class="sxs-lookup"><span data-stu-id="6ed93-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-302">13836 (0x360c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-302">13836 (0x360C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-303">Fehler beim Verarbeiten der Nutzlast von Zertifikat Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-303">Error processing Certificate Request payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**Fehler \_ IPSec \_ IKE \_ Prozess \_ Err- \_ Hash**</span><span class="sxs-lookup"><span data-stu-id="6ed93-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-305">13837 (0x360d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-305">13837 (0x360D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-306">Fehler beim Verarbeiten der Hash Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-306">Error processing Hash payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ sig**</span><span class="sxs-lookup"><span data-stu-id="6ed93-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-308">13838 (0x360e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-308">13838 (0x360E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-309">Fehler beim Verarbeiten der Signatur Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-309">Error processing Signature payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**Fehler \_ IPSec- \_ IKE- \_ Prozess \_ Err \_ Nonce**</span><span class="sxs-lookup"><span data-stu-id="6ed93-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NONCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-311">13839 (0x360f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-311">13839 (0x360F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-312">Fehler beim Verarbeiten der Nonce-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-312">Error processing Nonce payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Prozess- \_ \_ Benachrichtigung Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-314">13840 (0x3610)</span><span class="sxs-lookup"><span data-stu-id="6ed93-314">13840 (0x3610)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-315">Fehler beim Verarbeiten der Nutzlast benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-315">Error processing Notify payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="6ed93-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-317">13841 (0x3611)</span><span class="sxs-lookup"><span data-stu-id="6ed93-317">13841 (0x3611)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-318">Fehler beim Verarbeiten von Lösch Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-318">Error processing Delete Payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**Fehler \_ IPSec \_ IKE \_ Process \_ Err- \_ Hersteller**</span><span class="sxs-lookup"><span data-stu-id="6ed93-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_VENDOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-320">13842 (0x3612)</span><span class="sxs-lookup"><span data-stu-id="6ed93-320">13842 (0x3612)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-321">Fehler beim Verarbeiten der VendorID-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-321">Error processing VendorId payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**Fehler bei \_ IPSec- \_ IKE \_ ungültige \_ Nutzlast.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-323">13843 (0x3613)</span><span class="sxs-lookup"><span data-stu-id="6ed93-323">13843 (0x3613)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-324">Ungültige Nutzlast empfangen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-324">Invalid payload received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**Fehler \_ IPSec \_ IKE \_ Load \_ Soft \_ sa**</span><span class="sxs-lookup"><span data-stu-id="6ed93-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR\_IPSEC\_IKE\_LOAD\_SOFT\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-326">13844 (0x3614)</span><span class="sxs-lookup"><span data-stu-id="6ed93-326">13844 (0x3614)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-327">Soft-SA geladen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-327">Soft SA loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**Fehler "IPSec", Soft-SA, wurde \_ \_ \_ \_ \_ \_ abgebrochen.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR\_IPSEC\_IKE\_SOFT\_SA\_TORN\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-329">13845 (0x3615)</span><span class="sxs-lookup"><span data-stu-id="6ed93-329">13845 (0x3615)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-330">Weiche SA wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-330">Soft SA torn down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültiges \_ Cookie.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR\_IPSEC\_IKE\_INVALID\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-332">13846 (0x3616)</span><span class="sxs-lookup"><span data-stu-id="6ed93-332">13846 (0x3616)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-333">Ungültiges Cookie empfangen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-333">Invalid cookie received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**Fehler \_ IPSec \_ IKE \_ kein \_ Peer \_ Zertifikat**</span><span class="sxs-lookup"><span data-stu-id="6ed93-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_PEER\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-335">13847 (0x3617)</span><span class="sxs-lookup"><span data-stu-id="6ed93-335">13847 (0x3617)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-336">Der Peer konnte ein gültiges Computer Zertifikat nicht senden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-336">Peer failed to send valid machine certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Peer- \_ CRL \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR\_IPSEC\_IKE\_PEER\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-338">13848 (0x3618)</span><span class="sxs-lookup"><span data-stu-id="6ed93-338">13848 (0x3618)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-339">Fehler bei der Zertifizierungs Sperr Überprüfung des Peer Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="6ed93-339">Certification Revocation check of peer's certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Richtlinie \_ ändern**</span><span class="sxs-lookup"><span data-stu-id="6ed93-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR\_IPSEC\_IKE\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-341">13849 (0x3619)</span><span class="sxs-lookup"><span data-stu-id="6ed93-341">13849 (0x3619)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-342">Die neue Richtlinie hat eine SAS für eine alte Richtlinie ungültig gemacht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-342">New policy invalidated SAs formed with old policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**Fehler \_ IPSec \_ IKE \_ keine \_ mm- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="6ed93-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_MM\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-344">13850 (0x361a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-344">13850 (0x361A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-345">Es gibt keine verfügbare IKE-Hauptmodus-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="6ed93-345">There is no available Main Mode IKE policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**Fehler \_ IPSec \_ IKE \_ notcbpriv**</span><span class="sxs-lookup"><span data-stu-id="6ed93-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR\_IPSEC\_IKE\_NOTCBPRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-347">13851 (0x361b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-347">13851 (0x361B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-348">TCB-Berechtigung konnte nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-348">Failed to enabled TCB privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**Fehler \_ IPSec \_ IKE \_ secloadfail**</span><span class="sxs-lookup"><span data-stu-id="6ed93-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR\_IPSEC\_IKE\_SECLOADFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-350">13852 (0x361c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-350">13852 (0x361C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-351">SECURITY.DLL konnte nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-351">Failed to load SECURITY.DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**Fehler \_ IPSec \_ IKE \_ failsspinit**</span><span class="sxs-lookup"><span data-stu-id="6ed93-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR\_IPSEC\_IKE\_FAILSSPINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-353">13853 (0x361d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-353">13853 (0x361D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-354">Fehler beim Abrufen der dispatchadresse der Sicherheits Funktions Tabelle von SSPI.</span><span class="sxs-lookup"><span data-stu-id="6ed93-354">Failed to obtain security function table dispatch address from SSPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**Fehler \_ IPSec \_ IKE \_ failqueryssp**</span><span class="sxs-lookup"><span data-stu-id="6ed93-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR\_IPSEC\_IKE\_FAILQUERYSSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-356">13854 (0x361e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-356">13854 (0x361E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-357">Fehler beim Abfragen des Kerberos-Pakets zum Abrufen der maximalen Tokengröße.</span><span class="sxs-lookup"><span data-stu-id="6ed93-357">Failed to query Kerberos package to obtain max token size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**Fehler \_ IPSec \_ IKE \_ srvacqfail**</span><span class="sxs-lookup"><span data-stu-id="6ed93-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR\_IPSEC\_IKE\_SRVACQFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-359">13855 (0x361f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-359">13855 (0x361F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-360">Fehler beim Abrufen der Anmelde Informationen des Kerberos-Servers für den ISAKMP- \_ /fehleripsec- \_ IKE-Dienst.</span><span class="sxs-lookup"><span data-stu-id="6ed93-360">Failed to obtain Kerberos server credentials for ISAKMP/ERROR\_IPSEC\_IKE service.</span></span> <span data-ttu-id="6ed93-361">Die Kerberos-Authentifizierung funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-361">Kerberos authentication will not function.</span></span> <span data-ttu-id="6ed93-362">Der wahrscheinlichste Grund hierfür ist fehlende Domänen Mitgliedschaft.</span><span class="sxs-lookup"><span data-stu-id="6ed93-362">The most likely reason for this is lack of domain membership.</span></span> <span data-ttu-id="6ed93-363">Dies ist normal, wenn der Computer Mitglied einer Arbeitsgruppe ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-363">This is normal if your computer is a member of a workgroup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**Fehler \_ IPSec \_ IKE \_ srvquerykred**</span><span class="sxs-lookup"><span data-stu-id="6ed93-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR\_IPSEC\_IKE\_SRVQUERYCRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-365">13856 (0x3620)</span><span class="sxs-lookup"><span data-stu-id="6ed93-365">13856 (0x3620)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-366">Der SSPI-Prinzipal Name für den ISAKMP- \_ /fehleripsec- \_ IKE-Dienst ([**querykredentialsattributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)) konnte nicht ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-366">Failed to determine SSPI principal name for ISAKMP/ERROR\_IPSEC\_IKE service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**Fehler \_ IPSec \_ IKE \_ getspifail**</span><span class="sxs-lookup"><span data-stu-id="6ed93-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR\_IPSEC\_IKE\_GETSPIFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-368">13857 (0x3621)</span><span class="sxs-lookup"><span data-stu-id="6ed93-368">13857 (0x3621)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-369">Fehler beim Abrufen des neuen SPI für den eingehenden Datenverkehr vom IPSec-Treiber.</span><span class="sxs-lookup"><span data-stu-id="6ed93-369">Failed to obtain new SPI for the inbound SA from IPsec driver.</span></span> <span data-ttu-id="6ed93-370">Die häufigste Ursache hierfür ist, dass der Treiber nicht über den richtigen Filter verfügt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-370">The most common cause for this is that the driver does not have the correct filter.</span></span> <span data-ttu-id="6ed93-371">Überprüfen Sie die Richtlinie zum Überprüfen der Filter.</span><span class="sxs-lookup"><span data-stu-id="6ed93-371">Check your policy to verify the filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**Fehler \_ IPSec \_ IKE \_ ungültiger \_ Filter**</span><span class="sxs-lookup"><span data-stu-id="6ed93-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR\_IPSEC\_IKE\_INVALID\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-373">13858 (0x3622)</span><span class="sxs-lookup"><span data-stu-id="6ed93-373">13858 (0x3622)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-374">Der angegebene Filter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-374">Given filter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**Fehler bei \_ IPSec \_ IKE nicht genügend Arbeits \_ \_ \_ Speicher.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR\_IPSEC\_IKE\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-376">13859 (0x3623)</span><span class="sxs-lookup"><span data-stu-id="6ed93-376">13859 (0x3623)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-377">Die Speicherbelegung hat einen Fehler erzeugt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-377">Memory allocation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**Fehler beim \_ IPSec- \_ IKE- \_ \_ Update \_ Schlüssel hinzufügen \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR\_IPSEC\_IKE\_ADD\_UPDATE\_KEY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-379">13860 (0x3624)</span><span class="sxs-lookup"><span data-stu-id="6ed93-379">13860 (0x3624)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-380">Fehler beim Hinzufügen der Sicherheits Zuordnung zum IPSec-Treiber.</span><span class="sxs-lookup"><span data-stu-id="6ed93-380">Failed to add Security Association to IPsec Driver.</span></span> <span data-ttu-id="6ed93-381">Die häufigste Ursache hierfür ist, dass die IKE-Aushandlung zu lange gedauert hat.</span><span class="sxs-lookup"><span data-stu-id="6ed93-381">The most common cause for this is if the IKE negotiation took too long to complete.</span></span> <span data-ttu-id="6ed93-382">Wenn das Problem weiterhin besteht, verringern Sie die Last auf dem fehlerhaften Computer.</span><span class="sxs-lookup"><span data-stu-id="6ed93-382">If the problem persists, reduce the load on the faulting machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**\_ungültige IPSec- \_ IKE- \_ \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="6ed93-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR\_IPSEC\_IKE\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-384">13861 (0x3625 starten)</span><span class="sxs-lookup"><span data-stu-id="6ed93-384">13861 (0x3625)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-385">Ungültige Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="6ed93-385">Invalid policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**Fehler \_ IPSec \_ IKE \_ unbekannt \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR\_IPSEC\_IKE\_UNKNOWN\_DOI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-387">13862 (0x3626)</span><span class="sxs-lookup"><span data-stu-id="6ed93-387">13862 (0x3626)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-388">Ungültiger doi.</span><span class="sxs-lookup"><span data-stu-id="6ed93-388">Invalid DOI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**Fehler bei \_ IPSec- \_ IKE ( \_ ungültige \_ Situation)**</span><span class="sxs-lookup"><span data-stu-id="6ed93-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SITUATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-390">13863 (0x3627)</span><span class="sxs-lookup"><span data-stu-id="6ed93-390">13863 (0x3627)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-391">Ungültige Situation.</span><span class="sxs-lookup"><span data-stu-id="6ed93-391">Invalid situation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**Fehler bei \_ IPSec- \_ IKE- \_ dh \_ -Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR\_IPSEC\_IKE\_DH\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-393">13864 (0x3628)</span><span class="sxs-lookup"><span data-stu-id="6ed93-393">13864 (0x3628)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-394">Diffie-Hellman Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-394">Diffie-Hellman failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ Gruppe.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR\_IPSEC\_IKE\_INVALID\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-396">13865 (0x3629)</span><span class="sxs-lookup"><span data-stu-id="6ed93-396">13865 (0x3629)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-397">Ungültige Diffie-Hellman Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6ed93-397">Invalid Diffie-Hellman group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**Fehler beim \_ Verschlüsseln der IPSec- \_ IKE. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR\_IPSEC\_IKE\_ENCRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-399">13866 (0x362a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-399">13866 (0x362A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-400">Fehler beim Verschlüsseln der Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-400">Error encrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**Fehler \_ IPSec \_ IKE \_ entschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="6ed93-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR\_IPSEC\_IKE\_DECRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-402">13867 (0x362b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-402">13867 (0x362B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-403">Fehler beim Entschlüsseln von Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-403">Error decrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**\_IPSec- \_ IKE- \_ Richtlinien \_ Übereinstimmung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR\_IPSEC\_IKE\_POLICY\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-405">13868 (0x362c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-405">13868 (0x362C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-406">Fehler bei Richtlinien Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-406">Policy match error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**Fehler " \_ IPSec \_ IKE \_ nicht unterstützte \_ ID"**</span><span class="sxs-lookup"><span data-stu-id="6ed93-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR\_IPSEC\_IKE\_UNSUPPORTED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-408">13869 (0x362d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-408">13869 (0x362D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-409">Nicht unterstützte ID.</span><span class="sxs-lookup"><span data-stu-id="6ed93-409">Unsupported ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**Fehler bei \_ IPSec- \_ IKE ( \_ ungültiger \_ Hash)**</span><span class="sxs-lookup"><span data-stu-id="6ed93-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-411">13870 (0x362e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-411">13870 (0x362E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-412">Fehler bei der Hash Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-412">Hash verification failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ \_ HashAlg**</span><span class="sxs-lookup"><span data-stu-id="6ed93-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-414">13871 (0x362f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-414">13871 (0x362F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-415">Ungültiger Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-415">Invalid hash algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ \_ Hashgröße**</span><span class="sxs-lookup"><span data-stu-id="6ed93-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-417">13872 (0x3630)</span><span class="sxs-lookup"><span data-stu-id="6ed93-417">13872 (0x3630)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-418">Ungültige Hashgröße.</span><span class="sxs-lookup"><span data-stu-id="6ed93-418">Invalid hash size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**Fehler \_ IPSec \_ IKE \_ ungültig \_ verschlüsseln ( \_ ALG)**</span><span class="sxs-lookup"><span data-stu-id="6ed93-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_ENCRYPT\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-420">13873 (0x3631)</span><span class="sxs-lookup"><span data-stu-id="6ed93-420">13873 (0x3631)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-421">Ungültiger Verschlüsselungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-421">Invalid encryption algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ auth \_ alg**</span><span class="sxs-lookup"><span data-stu-id="6ed93-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-423">13874 (0x3632)</span><span class="sxs-lookup"><span data-stu-id="6ed93-423">13874 (0x3632)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-424">Ungültiger Authentifizierungsalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-424">Invalid authentication algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ sig**</span><span class="sxs-lookup"><span data-stu-id="6ed93-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-426">13875 (0x3633)</span><span class="sxs-lookup"><span data-stu-id="6ed93-426">13875 (0x3633)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-427">Ungültige Zertifikat Signatur.</span><span class="sxs-lookup"><span data-stu-id="6ed93-427">Invalid certificate signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**Fehler beim \_ Laden der IPSec- \_ IKE. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR\_IPSEC\_IKE\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-429">13876 (0x3634)</span><span class="sxs-lookup"><span data-stu-id="6ed93-429">13876 (0x3634)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-430">Fehler beim Laden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-430">Load failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**Fehler \_ IPSec \_ IKE \_ RPC \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="6ed93-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR\_IPSEC\_IKE\_RPC\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-432">13877 (0x3635)</span><span class="sxs-lookup"><span data-stu-id="6ed93-432">13877 (0x3635)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-433">Gelöscht per RPC-Aufruf.</span><span class="sxs-lookup"><span data-stu-id="6ed93-433">Deleted via RPC call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**Fehler \_ IPSec- \_ IKE ist \_ fehlerhaft \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR\_IPSEC\_IKE\_BENIGN\_REINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-435">13878 (0x3636)</span><span class="sxs-lookup"><span data-stu-id="6ed93-435">13878 (0x3636)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-436">Temporärer Zustand, der zum Ausführen der erneuten Initialisierung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed93-436">Temporary state created to perform reinitialization.</span></span> <span data-ttu-id="6ed93-437">Dies ist kein echter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-437">This is not a real failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Benachrichtigung für ungültige \_ Antwort \_ \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="6ed93-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR\_IPSEC\_IKE\_INVALID\_RESPONDER\_LIFETIME\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-439">13879 (0x3637)</span><span class="sxs-lookup"><span data-stu-id="6ed93-439">13879 (0x3637)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-440">Der in der Benachrichtigungs Lebensdauer-Benachrichtigung empfangene Lebensdauer Wert liegt unterhalb des konfigurierten Mindestwerts von Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="6ed93-440">The lifetime value received in the Responder Lifetime Notify is below the Windows 2000 configured minimum value.</span></span> <span data-ttu-id="6ed93-441">Korrigieren Sie die Richtlinie auf dem Peer Computer.</span><span class="sxs-lookup"><span data-stu-id="6ed93-441">Please fix the policy on the peer machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**Fehler bei \_ IPSec \_ IKE \_ ungültige \_ Haupt \_ Version.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MAJOR\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-443">13880 (0x3638)</span><span class="sxs-lookup"><span data-stu-id="6ed93-443">13880 (0x3638)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-444">Der Empfänger kann die im-Header angegebene Version von IKE nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-444">The recipient cannot handle version of IKE specified in the header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ CERT \_ keylen.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_KEYLEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-446">13881 (0x3639)</span><span class="sxs-lookup"><span data-stu-id="6ed93-446">13881 (0x3639)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-447">Die Schlüssellänge im Zertifikat ist zu klein für konfigurierte Sicherheitsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-447">Key length in certificate is too small for configured security requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**Fehler \_ IPSec \_ IKE \_ mm \_ Limit**</span><span class="sxs-lookup"><span data-stu-id="6ed93-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR\_IPSEC\_IKE\_MM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-449">13882 (0x363a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-449">13882 (0x363A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-450">Die maximal zulässige Anzahl von festgelegten mm-SAS-überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-450">Max number of established MM SAs to peer exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**Fehler bei der \_ IPSec- \_ IKE- \_ Aushandlung \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-452">13883 (0x363b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-452">13883 (0x363B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-453">IKE hat eine Richtlinie zum Deaktivieren der Aushandlung erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-453">IKE received a policy that disables negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**\_IPSec- \_ IKE- \_ qm- \_ Grenzwert (Fehler)**</span><span class="sxs-lookup"><span data-stu-id="6ed93-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR\_IPSEC\_IKE\_QM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-455">13884 (0x363c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-455">13884 (0x363C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-456">Die maximale schnellmodusbeschränkung für den Hauptmodus wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-456">Reached maximum quick mode limit for the main mode.</span></span> <span data-ttu-id="6ed93-457">Der neue Hauptmodus wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-457">New main mode will be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**Fehler \_ IPSec \_ IKE \_ mm ist \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR\_IPSEC\_IKE\_MM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-459">13885 (0x363d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-459">13885 (0x363D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-460">Die Lebensdauer der Hauptmodus-SA ist abgelaufen</span><span class="sxs-lookup"><span data-stu-id="6ed93-460">Main mode SA lifetime expired or peer sent a main mode delete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**Fehler \_ IPSec \_ IKE- \_ Peer \_ mm hat \_ \_ ungültig angenommen.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR\_IPSEC\_IKE\_PEER\_MM\_ASSUMED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-462">13886 (0x363e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-462">13886 (0x363E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-463">Der Hauptmodus-SA ist ungültig, da der Peer nicht mehr antwortet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-463">Main mode SA assumed to be invalid because peer stopped responding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**Fehler bei \_ IPSec-Richtlinien für die \_ \_ Zertifikat \_ Ketten \_ Richtlinie \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR\_IPSEC\_IKE\_CERT\_CHAIN\_POLICY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-465">13887 (0x363f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-465">13887 (0x363F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-466">Das Zertifikat wird nicht zu einem vertrauenswürdigen Stamm in der IPSec-Richtlinie verkettet</span><span class="sxs-lookup"><span data-stu-id="6ed93-466">Certificate doesn't chain to a trusted root in IPsec policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**Fehler " \_ IPSec \_ IKE \_ unerwartete Nachrichten- \_ \_ ID"**</span><span class="sxs-lookup"><span data-stu-id="6ed93-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR\_IPSEC\_IKE\_UNEXPECTED\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-468">13888 (0x3640)</span><span class="sxs-lookup"><span data-stu-id="6ed93-468">13888 (0x3640)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-469">Unerwartete Nachrichten-ID empfangen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-469">Received unexpected message ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**Fehler bei \_ IPSec- \_ IKE \_ ungültige Authentifizierungs \_ \_ Nutzlast.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-471">13889 (0x3641)</span><span class="sxs-lookup"><span data-stu-id="6ed93-471">13889 (0x3641)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-472">Es wurden ungültige Authentifizierungs Angebote empfangen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-472">Received invalid authentication offers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**Fehler \_ IPSec- \_ IKE- \_ DOS- \_ Cookie \_ gesendet**</span><span class="sxs-lookup"><span data-stu-id="6ed93-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR\_IPSEC\_IKE\_DOS\_COOKIE\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-474">13890 (0x3642)</span><span class="sxs-lookup"><span data-stu-id="6ed93-474">13890 (0x3642)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-475">An Initiator gesendete DOS-Cookie benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-475">Sent DoS cookie notify to initiator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**Fehler beim Herunterfahren der \_ IPSec- \_ IKE. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR\_IPSEC\_IKE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-477">13891 (0x3643)</span><span class="sxs-lookup"><span data-stu-id="6ed93-477">13891 (0x3643)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-478">Der IKE-Dienst wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="6ed93-478">IKE service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**Fehler bei \_ IPSec \_ IKE \_ CGA-Authentifizierung \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR\_IPSEC\_IKE\_CGA\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-480">13892 (0x3644)</span><span class="sxs-lookup"><span data-stu-id="6ed93-480">13892 (0x3644)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-481">Die Bindung zwischen der CGA-Adresse und dem Zertifikat konnte nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-481">Could not verify binding between CGA address and certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**Fehler \_ IPSec \_ IKE- \_ Prozess \_ Err \_ NatOA**</span><span class="sxs-lookup"><span data-stu-id="6ed93-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NATOA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-483">13893 (0x3645)</span><span class="sxs-lookup"><span data-stu-id="6ed93-483">13893 (0x3645)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-484">Fehler beim Verarbeiten der NatOA-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="6ed93-484">Error processing NatOA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**Fehler \_ IPSec \_ IKE \_ ungültige \_ mm \_ für \_ qm**</span><span class="sxs-lookup"><span data-stu-id="6ed93-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MM\_FOR\_QM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-486">13894 (0x3646)</span><span class="sxs-lookup"><span data-stu-id="6ed93-486">13894 (0x3646)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-487">Die Parameter des Hauptmodus sind für diesen Schnellmodus ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-487">Parameters of the main mode are invalid for this quick mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**Fehler \_ IPSec \_ IKE \_ qm ist \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR\_IPSEC\_IKE\_QM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-489">13895 (0x3647)</span><span class="sxs-lookup"><span data-stu-id="6ed93-489">13895 (0x3647)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-490">Der Schnellmodus-SA war vom IPSec-Treiber abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-490">Quick mode SA was expired by IPsec driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**Fehler \_ IPSec \_ IKE \_ zu \_ viele \_ Filter**</span><span class="sxs-lookup"><span data-stu-id="6ed93-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR\_IPSEC\_IKE\_TOO\_MANY\_FILTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-492">13896 (0x3648)</span><span class="sxs-lookup"><span data-stu-id="6ed93-492">13896 (0x3648)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-493">Es wurden zu viele dynamisch hinzugefügte IKEEXT-Filter erkannt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-493">Too many dynamically added IKEEXT filters were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="6ed93-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-495">13897 (0x3649)</span><span class="sxs-lookup"><span data-stu-id="6ed93-495">13897 (0x3649)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-496">Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ Ende</span><span class="sxs-lookup"><span data-stu-id="6ed93-496">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**Fehler \_ IPSec \_ IKE \_ Kill \_ Dummy- \_ NAP- \_ Tunnel**</span><span class="sxs-lookup"><span data-stu-id="6ed93-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR\_IPSEC\_IKE\_KILL\_DUMMY\_NAP\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-498">13898 (0x364a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-498">13898 (0x364A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-499">NAP-reauth war erfolgreich und muss den Dummy-NAP-IKEv2-Tunnel löschen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-499">NAP reauth succeeded and must delete the dummy NAP IKEv2 tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**Fehler bei \_ IPSec \_ \_ -internen \_ IP- \_ Zuweisungs \_ Fehlern**</span><span class="sxs-lookup"><span data-stu-id="6ed93-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR\_IPSEC\_IKE\_INNER\_IP\_ASSIGNMENT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-501">13899 (0x364b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-501">13899 (0x364B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-502">Fehler beim Zuweisen der inneren IP-Adresse zum Initiator im Tunnel Modus.</span><span class="sxs-lookup"><span data-stu-id="6ed93-502">Error in assigning inner IP address to initiator in tunnel mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**Fehler \_ IPSec \_ IKE \_ erfordert keine \_ CP- \_ Nutzlast \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR\_IPSEC\_IKE\_REQUIRE\_CP\_PAYLOAD\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-504">13900 (0x364c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-504">13900 (0x364C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-505">Erforderliche Konfigurations Nutzlast fehlt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-505">Require configuration payload missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**Fehler bei der \_ IPSec-Schlüsselmodul-Identitätswechsel \_ \_ \_ \_ Aushandlung \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="6ed93-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR\_IPSEC\_KEY\_MODULE\_IMPERSONATION\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-507">13901 (0x364d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-507">13901 (0x364D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-508">Eine Aushandlung, die als Sicherheitsprinzip ausgeführt wird, das die Verbindung ausgegeben hat, wird gerade ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-508">A negotiation running as the security principle who issued the connection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**Fehler \_ IPSec- \_ IKE- \_ Koexistenz unter \_ drücken**</span><span class="sxs-lookup"><span data-stu-id="6ed93-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR\_IPSEC\_IKE\_COEXISTENCE\_SUPPRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-510">13902 (0x364e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-510">13902 (0x364E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-511">Die SA wurde aufgrund von ikev1/AuthIP-koexistenzunterdrücküberprüfung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-511">SA was deleted due to IKEv1/AuthIP co-existence suppress check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**Fehler \_ IPSec \_ IKE \_ ratelimit \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="6ed93-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR\_IPSEC\_IKE\_RATELIMIT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-513">13903 (0x364f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-513">13903 (0x364F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-514">Die eingehende SA-Anforderung wurde aufgrund der Peer-IP-Adress Raten Begrenzung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-514">Incoming SA request was dropped due to peer IP address rate limiting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**Fehler \_ IPSec \_ IKE- \_ Peer \_ \_ unterstützt \_ MOBIKE nicht**</span><span class="sxs-lookup"><span data-stu-id="6ed93-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR\_IPSEC\_IKE\_PEER\_DOESNT\_SUPPORT\_MOBIKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-516">13904 (0x3650)</span><span class="sxs-lookup"><span data-stu-id="6ed93-516">13904 (0x3650)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-517">Der Peer unterstützt MOBIKE nicht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-517">Peer does not support MOBIKE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**Fehler bei \_ IPSec- \_ IKE- \_ Autorisierung \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-519">13905 (0x3651)</span><span class="sxs-lookup"><span data-stu-id="6ed93-519">13905 (0x3651)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-520">Die Einrichtung der Sicherheitszuordnung ist nicht autorisiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-520">SA establishment is not authorized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**Fehler beim \_ \_ \_ \_ \_ Autorisierungs \_ Fehler bei IPSec-IKE (Strong).**</span><span class="sxs-lookup"><span data-stu-id="6ed93-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-522">13906 (0x3652)</span><span class="sxs-lookup"><span data-stu-id="6ed93-522">13906 (0x3652)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-523">Die Einrichtung der SA ist nicht autorisiert, da es keine ausreichend starken PKINIT-basierten Anmelde Informationen gibt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-523">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**Fehler \_ bei IPSec- \_ IKE- \_ Autorisierung \_ \_ mit \_ optionalem \_ Wiederholungsversuch**</span><span class="sxs-lookup"><span data-stu-id="6ed93-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE\_WITH\_OPTIONAL\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-525">13907 (0x3653)</span><span class="sxs-lookup"><span data-stu-id="6ed93-525">13907 (0x3653)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-526">Die Einrichtung der Sicherheitszuordnung ist nicht autorisiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-526">SA establishment is not authorized.</span></span> <span data-ttu-id="6ed93-527">Möglicherweise müssen Sie aktualisierte oder andere Anmelde Informationen eingeben, z. b. eine Smartcard.</span><span class="sxs-lookup"><span data-stu-id="6ed93-527">You may need to enter updated or different credentials such as a smartcard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**Fehler bei \_ IPSec \_ -IKE \_ \_ -Autorisierung (Strong) \_ \_ und \_ certmap- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_AND\_CERTMAP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-529">13908 (0x3654)</span><span class="sxs-lookup"><span data-stu-id="6ed93-529">13908 (0x3654)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-530">Die Einrichtung der SA ist nicht autorisiert, da es keine ausreichend starken PKINIT-basierten Anmelde Informationen gibt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-530">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span> <span data-ttu-id="6ed93-531">Dies kann sich auf den Fehler bei der Zuordnung von Zertifikaten für das SA-Konto beziehen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-531">This might be related to certificate-to-account mapping failure for the SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ erweitert \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-533">13909 (0x3655)</span><span class="sxs-lookup"><span data-stu-id="6ed93-533">13909 (0x3655)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-534">Fehler \_ IPSec \_ IKE \_ NETg \_ Status \_ erweitert \_</span><span class="sxs-lookup"><span data-stu-id="6ed93-534">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**Fehler \_ IPSec \_ Bad \_ SPI**</span><span class="sxs-lookup"><span data-stu-id="6ed93-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR\_IPSEC\_BAD\_SPI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-536">13910 (0x3656)</span><span class="sxs-lookup"><span data-stu-id="6ed93-536">13910 (0x3656)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-537">Die SPI im Paket entspricht keiner gültigen IPSec-SA.</span><span class="sxs-lookup"><span data-stu-id="6ed93-537">The SPI in the packet does not match a valid IPsec SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**Fehler bei IPSec-SA-Gültigkeits \_ \_ \_ Dauer \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR\_IPSEC\_SA\_LIFETIME\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-539">13911 (0x3657)</span><span class="sxs-lookup"><span data-stu-id="6ed93-539">13911 (0x3657)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-540">Das Paket wurde über eine IPSec-SA empfangen, deren Lebensdauer abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-540">Packet was received on an IPsec SA whose lifetime has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**Fehler \_ IPSec \_ falsche \_ sa**</span><span class="sxs-lookup"><span data-stu-id="6ed93-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR\_IPSEC\_WRONG\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-542">13912 (0x3658)</span><span class="sxs-lookup"><span data-stu-id="6ed93-542">13912 (0x3658)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-543">Das Paket wurde über eine IPSec-SA empfangen, die nicht den Paket Merkmalen entspricht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-543">Packet was received on an IPsec SA that does not match the packet characteristics.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**Fehler beim \_ \_ \_ Überprüfen der IPSec-Wiedergabe \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR\_IPSEC\_REPLAY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-545">13913 (0x3659)</span><span class="sxs-lookup"><span data-stu-id="6ed93-545">13913 (0x3659)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-546">Fehler bei der Wiedergabe Überprüfung der Paket Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="6ed93-546">Packet sequence number replay check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**Fehler bei \_ IPSec \_ ungültiges \_ Paket.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR\_IPSEC\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-548">13914 (0x365a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-548">13914 (0x365A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-549">Der IPSec-Header und/oder-Nachspann im Paket ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-549">IPsec header and/or trailer in the packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**Fehler bei der \_ IPSec- \_ Integritäts \_ Überprüfung \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR\_IPSEC\_INTEGRITY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-551">13915 (0x365b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-551">13915 (0x365B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-552">Fehler bei der IPSec-Integritäts Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-552">IPsec integrity check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**Fehler beim \_ \_ Löschen von \_ Text in IPSec \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR\_IPSEC\_CLEAR\_TEXT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-554">13916 (0x365c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-554">13916 (0x365C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-555">IPSec hat ein Klartext-Paket gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-555">IPsec dropped a clear text packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**Fehler beim \_ Löschen der IPSec-Authentifizierungs \_ \_ Firewall \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR\_IPSEC\_AUTH\_FIREWALL\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-557">13917 (0x365d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-557">13917 (0x365D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-558">IPSec hat ein eingehender ESP-Paket im authentifizierten Firewallmodus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-558">IPsec dropped an incoming ESP packet in authenticated firewall mode.</span></span> <span data-ttu-id="6ed93-559">Diese Ablage ist unbedenklich.</span><span class="sxs-lookup"><span data-stu-id="6ed93-559">This drop is benign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**Fehler bei der \_ IPSec- \_ Drosselung \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR\_IPSEC\_THROTTLE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-561">13918 (0x365e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-561">13918 (0x365E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-562">IPSec hat ein Paket aufgrund der DOS-Drosselung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-562">IPsec dropped a packet due to DoS throttling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**Fehler \_ IPSec- \_ DoSP- \_ Block**</span><span class="sxs-lookup"><span data-stu-id="6ed93-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR\_IPSEC\_DOSP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-564">13925 (0x3665)</span><span class="sxs-lookup"><span data-stu-id="6ed93-564">13925 (0x3665)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-565">Der IPSec-DOS-Schutz entsprach einer expliziten blockregel.</span><span class="sxs-lookup"><span data-stu-id="6ed93-565">IPsec DoS Protection matched an explicit block rule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**Fehler \_ IPSec- \_ DoSP- \_ \_ Multicast empfangen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR\_IPSEC\_DOSP\_RECEIVED\_MULTICAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-567">13926 (0x3666)</span><span class="sxs-lookup"><span data-stu-id="6ed93-567">13926 (0x3666)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-568">IPSec-DOS-Schutz hat ein IPSec-spezifisches Multicast Paket empfangen, das nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-568">IPsec DoS Protection received an IPsec specific multicast packet which is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**Fehler bei \_ IPSec- \_ DoSP- \_ Paket ist ungültig \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR\_IPSEC\_DOSP\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-570">13927 (0x3667)</span><span class="sxs-lookup"><span data-stu-id="6ed93-570">13927 (0x3667)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-571">Der IPSec-DOS-Schutz hat ein falsch formatiertes Paket empfangen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-571">IPsec DoS Protection received an incorrectly formatted packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**Fehler bei der \_ IPSec- \_ DoSP- \_ Status \_ Suche \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR\_IPSEC\_DOSP\_STATE\_LOOKUP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-573">13928 (0x3668)</span><span class="sxs-lookup"><span data-stu-id="6ed93-573">13928 (0x3668)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-574">Der IPSec-DOS-Schutz konnte den Status nicht nachschlagen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-574">IPsec DoS Protection failed to look up state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**Fehler bei \_ IPSec- \_ DoSP- \_ maximalen \_ Einträgen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR\_IPSEC\_DOSP\_MAX\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-576">13929 (0x3669)</span><span class="sxs-lookup"><span data-stu-id="6ed93-576">13929 (0x3669)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-577">Der IPSec-DOS-Schutz konnte den Status nicht erstellen, da die maximale Anzahl von Einträgen, die von der Richtlinie zugelassen werden, erreicht</span><span class="sxs-lookup"><span data-stu-id="6ed93-577">IPsec DoS Protection failed to create state because the maximum number of entries allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**Fehler \_ IPSec \_ DoSP \_ keymod ist \_ nicht \_ zulässig.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR\_IPSEC\_DOSP\_KEYMOD\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-579">13930 (0x366a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-579">13930 (0x366A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-580">IPSec-DOS-Schutz hat ein IPSec-Aushandlungs Paket für ein Schlüssel Verwaltungsmodul empfangen, das von der Richtlinie nicht zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="6ed93-580">IPsec DoS Protection received an IPsec negotiation packet for a keying module which is not allowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**Fehler beim \_ Installieren von IPSec- \_ DoSP. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR\_IPSEC\_DOSP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-582">13931 (0x366b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-582">13931 (0x366B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-583">IPSec-DOS-Schutz wurde nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-583">IPsec DoS Protection has not been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**Fehler \_ IPSec \_ DoSP \_ Max \_ pro \_ IP- \_ \_ Warteschlangen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR\_IPSEC\_DOSP\_MAX\_PER\_IP\_RATELIMIT\_QUEUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-585">13932 (0x366c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-585">13932 (0x366C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-586">Der IPSec-DOS-Schutz konnte eine interne IP-Raten Limit-Warteschlange nicht erstellen, da die von der Richtlinie zugelassene maximale Anzahl von Warteschlangen erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed93-586">IPsec DoS Protection failed to create a per internal IP rate limit queue because the maximum number of queues allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**Fehler \_ SxS- \_ Abschnitt \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERROR\_SXS\_SECTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-588">14000 (0x36b0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-588">14000 (0x36B0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-589">Der angeforderte Abschnitt war im Aktivierungs Kontext nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-589">The requested section was not present in the activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**Fehler \_ SxS \_ cant \_ gen \_ ActCtx**</span><span class="sxs-lookup"><span data-stu-id="6ed93-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR\_SXS\_CANT\_GEN\_ACTCTX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-591">14001 (0x36b1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-591">14001 (0x36B1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-592">Die Anwendung konnte nicht gestartet werden, da die Seite-an-Seite-Konfiguration nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-592">The application has failed to start because its side-by-side configuration is incorrect.</span></span> <span data-ttu-id="6ed93-593">Ausführlichere Informationen finden Sie im Anwendungs Ereignisprotokoll, oder verwenden Sie das Befehlszeilen sxstrace.exe-Tool.</span><span class="sxs-lookup"><span data-stu-id="6ed93-593">Please see the application event log or use the command-line sxstrace.exe tool for more detail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**Fehler \_ SxS \_ ungültiges \_ actctxdata- \_ Format.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR\_SXS\_INVALID\_ACTCTXDATA\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-595">14002 (0x36b2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-595">14002 (0x36B2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-596">Das Datenformat der Anwendungs Bindung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-596">The application binding data format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**Fehler \_ SxS- \_ Assembly \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-598">14003 (0x36b3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-598">14003 (0x36B3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-599">Die Assembly, auf die verwiesen wird, ist nicht auf dem System installiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-599">The referenced assembly is not installed on your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**Fehler im \_ SxS- \_ Manifest- \_ Format \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR\_SXS\_MANIFEST\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-601">14004 (0x36b4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-601">14004 (0x36B4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-602">Die Manifest-Datei beginnt nicht mit den erforderlichen Tags und Formatierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-602">The manifest file does not begin with the required tag and format information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**Fehler beim Analysieren des Fehler \_ SxS- \_ Manifests. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR\_SXS\_MANIFEST\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-604">14005 (0x36b5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-604">14005 (0x36B5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-605">Die Manifest-Datei enthält mindestens einen Syntax Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-605">The manifest file contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**Fehler \_ SxS- \_ Aktivierungs \_ Kontext \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR\_SXS\_ACTIVATION\_CONTEXT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-607">14006 (0x36b6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-607">14006 (0x36B6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-608">Die Anwendung hat versucht, einen deaktivierten Aktivierungs Kontext zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6ed93-608">The application attempted to activate a disabled activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**Fehler \_ SxS- \_ Schlüssel wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR\_SXS\_KEY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-610">14007 (0x36b7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-610">14007 (0x36B7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-611">Der angeforderte Suchschlüssel wurde in keinem aktiven Aktivierungs Kontext gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-611">The requested lookup key was not found in any active activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**Fehler \_ SxS- \_ Versions \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR\_SXS\_VERSION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-613">14008 (0x36b8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-613">14008 (0x36B8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-614">Eine Komponenten Version, die für die Anwendung erforderlich ist, steht in Konflikt mit einer anderen bereits aktiven Komponenten Version.</span><span class="sxs-lookup"><span data-stu-id="6ed93-614">A component version required by the application conflicts with another component version already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**Fehler \_ SxS- \_ falscher \_ Abschnitts \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="6ed93-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR\_SXS\_WRONG\_SECTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-616">14009 (0x36b9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-616">14009 (0x36B9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-617">Der vom Typ angeforderte Aktivierungs Kontext Abschnitt entspricht nicht der verwendeten Abfrage-API.</span><span class="sxs-lookup"><span data-stu-id="6ed93-617">The type requested activation context section does not match the query API used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**Fehler \_ SxS- \_ Thread \_ Abfragen \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR\_SXS\_THREAD\_QUERIES\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-619">14010 (0x36ba)</span><span class="sxs-lookup"><span data-stu-id="6ed93-619">14010 (0x36BA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-620">Fehlende Systemressourcen erfordern, dass die isolierte Aktivierung für den aktuellen Ausführungs Thread deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-620">Lack of system resources has required isolated activation to be disabled for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**Fehler \_ SxS- \_ Prozess \_ Standard ist \_ bereits \_ festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR\_SXS\_PROCESS\_DEFAULT\_ALREADY\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-622">14011 (0x36bb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-622">14011 (0x36BB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-623">Fehler beim Festlegen des Standard Aktivierungs Kontexts für den Prozess, weil der standardmäßige Aktivierungs Kontext der Prozesse bereits festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed93-623">An attempt to set the process default activation context failed because the process default activation context was already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**Fehler \_ SxS \_ unbekannte \_ Codierungs \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="6ed93-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-625">14012 (0x36bc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-625">14012 (0x36BC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-626">Der angegebene Codierungs Gruppen Bezeichner wurde nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-626">The encoding group identifier specified is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**Fehler \_ SxS \_ unbekannte \_ Codierung.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-628">14013 (0x36bd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-628">14013 (0x36BD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-629">Die angeforderte Codierung wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-629">The encoding requested is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**Fehler \_ SxS \_ ungültiger \_ XML- \_ Namespace- \_ URI.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR\_SXS\_INVALID\_XML\_NAMESPACE\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-631">14014 (0x36be)</span><span class="sxs-lookup"><span data-stu-id="6ed93-631">14014 (0x36BE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-632">Das Manifest enthält einen Verweis auf einen ungültigen URI.</span><span class="sxs-lookup"><span data-stu-id="6ed93-632">The manifest contains a reference to an invalid URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**Fehler \_ SxS-Stamm \_ \_ Manifest- \_ Abhängigkeit \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR\_SXS\_ROOT\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-634">14015 (0x36bf)</span><span class="sxs-lookup"><span data-stu-id="6ed93-634">14015 (0x36BF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-635">Das Anwendungs Manifest enthält einen Verweis auf eine abhängige Assembly, die nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-635">The application manifest contains a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**Fehler \_ SxS- \_ Blatt \_ Manifest- \_ Abhängigkeit \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR\_SXS\_LEAF\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-637">14016 (0x36c0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-637">14016 (0x36C0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-638">Das Manifest für eine Assembly, die von der Anwendung verwendet wird, verfügt über einen Verweis auf eine abhängige Assembly, die nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-638">The manifest for an assembly used by the application has a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**Fehler \_ SxS \_ ungültiges Attribut für Assemblyidentität. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-640">14017 (0x36c1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-640">14017 (0x36C1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-641">Das Manifest enthält ein ungültiges Attribut für die Assemblyidentität.</span><span class="sxs-lookup"><span data-stu-id="6ed93-641">The manifest contains an attribute for the assembly identity which is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**Fehler im \_ SxS- \_ Manifest \_ fehlt der \_ erforderliche \_ Standard \_ Namespace.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_MISSING\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-643">14018 (0x36c2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-643">14018 (0x36C2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-644">Im Manifest fehlt die erforderliche Standard Namespace Spezifikation für das Assemblyelement.</span><span class="sxs-lookup"><span data-stu-id="6ed93-644">The manifest is missing the required default namespace specification on the assembly element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**Fehler \_ SxS- \_ Manifest \_ ungültiger \_ Erforderlicher \_ Standard \_ Namespace**</span><span class="sxs-lookup"><span data-stu-id="6ed93-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_INVALID\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-646">14019 (0x36c3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-646">14019 (0x36C3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-647">Im Manifest ist ein Standard Namespace für das Assembly-Element angegeben, aber sein Wert ist nicht "urn: Schemas-Microsoft-com: ASM. v1".</span><span class="sxs-lookup"><span data-stu-id="6ed93-647">The manifest has a default namespace specified on the assembly element but its value is not "urn:schemas-microsoft-com:asm.v1".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**Fehler \_ SxS \_ - \_ Kreuz Pfad des privaten Manifests \_ \_ mit Analyse \_ \_ \_ Punkt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR\_SXS\_PRIVATE\_MANIFEST\_CROSS\_PATH\_WITH\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-649">14020 (0x36c4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-649">14020 (0x36C4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-650">Das überprüfte private Manifest hat einen Pfad mit einem nicht unterstützten Analyse Punkt überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-650">The private manifest probed has crossed a path with an unsupported reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**Fehler \_ SxS \_ doppelte \_ dll- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="6ed93-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR\_SXS\_DUPLICATE\_DLL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-652">14021 (0x36c5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-652">14021 (0x36C5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-653">Bei mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, sind Dateien mit demselben Namen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-653">Two or more components referenced directly or indirectly by the application manifest have files by the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**Fehler \_ SxS \_ doppelte \_ WindowClass- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="6ed93-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR\_SXS\_DUPLICATE\_WINDOWCLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-655">14022 (0x36c6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-655">14022 (0x36C6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-656">Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über Fenster Klassen mit demselben Namen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-656">Two or more components referenced directly or indirectly by the application manifest have window classes with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**Fehler \_ SxS \_ doppelte \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="6ed93-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR\_SXS\_DUPLICATE\_CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-658">14023 (0x36c7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-658">14023 (0x36C7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-659">Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über die gleichen com-Server-CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="6ed93-659">Two or more components referenced directly or indirectly by the application manifest have the same COM server CLSIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**Fehler \_ SxS \_ doppelte \_ IID.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR\_SXS\_DUPLICATE\_IID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-661">14024 (0x36c8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-661">14024 (0x36C8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-662">Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, haben Proxys für die gleichen com-Schnittstellen-IIDs.</span><span class="sxs-lookup"><span data-stu-id="6ed93-662">Two or more components referenced directly or indirectly by the application manifest have proxies for the same COM interface IIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**Fehler \_ SxS \_ doppelte \_ TLBID**</span><span class="sxs-lookup"><span data-stu-id="6ed93-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR\_SXS\_DUPLICATE\_TLBID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-664">14025 (0x36c9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-664">14025 (0x36C9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-665">Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über die gleichen com-Typbibliotheks-tlgebote.</span><span class="sxs-lookup"><span data-stu-id="6ed93-665">Two or more components referenced directly or indirectly by the application manifest have the same COM type library TLBIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**Fehler \_ SxS \_ doppelte \_ ProgID**</span><span class="sxs-lookup"><span data-stu-id="6ed93-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR\_SXS\_DUPLICATE\_PROGID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-667">14026 (0x36ca)</span><span class="sxs-lookup"><span data-stu-id="6ed93-667">14026 (0x36CA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-668">Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, verfügen über dieselben com-ProgIDs.</span><span class="sxs-lookup"><span data-stu-id="6ed93-668">Two or more components referenced directly or indirectly by the application manifest have the same COM ProgIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**Fehler \_ SxS \_ doppelte \_ AssemblyName \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR\_SXS\_DUPLICATE\_ASSEMBLY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-670">14027 (0x36cb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-670">14027 (0x36CB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-671">Mindestens zwei Komponenten, auf die direkt oder indirekt durch das Anwendungs Manifest verwiesen wird, sind unterschiedliche Versionen derselben Komponente, die nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6ed93-671">Two or more components referenced directly or indirectly by the application manifest are different versions of the same component which is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**Fehler bei \_ SxS- \_ Datei \_ Hash \_ Konflikt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR\_SXS\_FILE\_HASH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-673">14028 (0x36cc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-673">14028 (0x36CC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-674">Die Datei einer Komponente entspricht nicht den Überprüfungs Informationen, die im Komponenten Manifest vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6ed93-674">A component's file does not match the verification information present in the component manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**Fehler beim \_ Analysieren der SxS- \_ Richtlinie. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR\_SXS\_POLICY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-676">14029 (0x36cd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-676">14029 (0x36CD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-677">Das Richtlinien Manifest enthält mindestens einen Syntax Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-677">The policy manifest contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**Fehler \_ SxS \_ XML \_ E \_ missingquote**</span><span class="sxs-lookup"><span data-stu-id="6ed93-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR\_SXS\_XML\_E\_MISSINGQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-679">14030 (0x36ce)</span><span class="sxs-lookup"><span data-stu-id="6ed93-679">14030 (0x36CE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-680">Manifeste-Analysefehler: Es wurde ein Zeichenfolgenliteral erwartet, aber es wurde kein öffnendes Anführungszeichen gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-680">Manifest Parse Error : A string literal was expected, but no opening quote character was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**Fehler \_ SxS \_ XML \_ E \_ commentsyntax**</span><span class="sxs-lookup"><span data-stu-id="6ed93-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR\_SXS\_XML\_E\_COMMENTSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-682">14031 (0x36cf)</span><span class="sxs-lookup"><span data-stu-id="6ed93-682">14031 (0x36CF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-683">Fehler beim Analysieren der Manifeste: in einem Kommentar wurde eine falsche Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-683">Manifest Parse Error : Incorrect syntax was used in a comment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**Fehler \_ SxS \_ XML \_ E \_ badstartnamechar**</span><span class="sxs-lookup"><span data-stu-id="6ed93-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR\_SXS\_XML\_E\_BADSTARTNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-685">14032 (0x36d0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-685">14032 (0x36D0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-686">Fehler beim Analysieren der Manifeste: ein Name wurde mit einem ungültigen Zeichen gestartet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-686">Manifest Parse Error : A name was started with an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**Fehler \_ SxS \_ XML \_ E \_ badnamechar**</span><span class="sxs-lookup"><span data-stu-id="6ed93-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR\_SXS\_XML\_E\_BADNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-688">14033 (0x36d1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-688">14033 (0x36D1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-689">Fehler beim Analysieren der Manifeste: ein Name enthielt ein ungültiges Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-689">Manifest Parse Error : A name contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**Fehler \_ SxS \_ XML \_ E \_ badcharinstring**</span><span class="sxs-lookup"><span data-stu-id="6ed93-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR\_SXS\_XML\_E\_BADCHARINSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-691">14034 (0x36d2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-691">14034 (0x36D2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-692">Fehler beim Analysieren der Manifeste: ein zeichenfolgenal enthielt ein ungültiges Zeichen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-692">Manifest Parse Error : A string literal contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**Fehler \_ SxS \_ XML \_ E \_ xmldeclsyntax**</span><span class="sxs-lookup"><span data-stu-id="6ed93-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR\_SXS\_XML\_E\_XMLDECLSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-694">14035 (0x36d3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-694">14035 (0x36D3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-695">Fehler beim Analysieren der Manifeste: Ungültige Syntax für eine XML-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="6ed93-695">Manifest Parse Error : Invalid syntax for an xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**Fehler \_ SxS \_ XML \_ E \_ badchardata**</span><span class="sxs-lookup"><span data-stu-id="6ed93-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR\_SXS\_XML\_E\_BADCHARDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-697">14036 (0x36d4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-697">14036 (0x36D4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-698">Fehler beim Analysieren der Manifeste: im Text Inhalt wurde ein ungültiges Zeichen gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-698">Manifest Parse Error : An Invalid character was found in text content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**Fehler \_ SxS \_ XML \_ E \_ missingwhitespace**</span><span class="sxs-lookup"><span data-stu-id="6ed93-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR\_SXS\_XML\_E\_MISSINGWHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-700">14037 (0x36d5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-700">14037 (0x36D5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-701">Fehler beim Analysieren der Manifeste: erforderlicher Leerraum fehlte.</span><span class="sxs-lookup"><span data-stu-id="6ed93-701">Manifest Parse Error : Required white space was missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**Fehler \_ SxS \_ XML \_ E \_ expectingtagend**</span><span class="sxs-lookup"><span data-stu-id="6ed93-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGTAGEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-703">14038 (0x36d6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-703">14038 (0x36D6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-704">Fehler beim Analysieren der Manifeste: das Zeichen ">" wurde erwartet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-704">Manifest Parse Error : The character '>' was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**Fehler \_ SxS \_ XML \_ E \_ missingsemikolon**</span><span class="sxs-lookup"><span data-stu-id="6ed93-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR\_SXS\_XML\_E\_MISSINGSEMICOLON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-706">14039 (0x36d7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-706">14039 (0x36D7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-707">Fehler beim Analysieren der Manifeste: ein Semikolon wurde erwartet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-707">Manifest Parse Error : A semi colon character was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**Fehler \_ SxS \_ XML \_ E \_ unbalancedparser**</span><span class="sxs-lookup"><span data-stu-id="6ed93-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR\_SXS\_XML\_E\_UNBALANCEDPAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-709">14040 (0x36d8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-709">14040 (0x36D8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-710">Fehler beim Analysieren der Manifeste: Klammern sind nicht ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-710">Manifest Parse Error : Unbalanced parentheses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**Fehler \_ SxS \_ XML \_ E \_ InternalError**</span><span class="sxs-lookup"><span data-stu-id="6ed93-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR\_SXS\_XML\_E\_INTERNALERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-712">14041 (0x36d9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-712">14041 (0x36D9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-713">Fehler beim Analysieren der Manifeste: Interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-713">Manifest Parse Error : Internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**Fehler \_ SxS \_ XML \_ E \_ unerwartetes \_ Leerzeichen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_WHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-715">14042 (0x36da)</span><span class="sxs-lookup"><span data-stu-id="6ed93-715">14042 (0x36DA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-716">Fehler beim Analysieren der Manifeste: an dieser Stelle ist kein Leerzeichen zulässig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-716">Manifest Parse Error : Whitespace is not allowed at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**Fehler \_ SxS \_ XML \_ E \_ unvollständige \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR\_SXS\_XML\_E\_INCOMPLETE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-718">14043 (0x36db)</span><span class="sxs-lookup"><span data-stu-id="6ed93-718">14043 (0x36DB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-719">Fehler beim Analysieren der Manifeste: das Dateiende wurde in einem ungültigen Zustand für die aktuelle Codierung erreicht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-719">Manifest Parse Error : End of file reached in invalid state for current encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**Fehler \_ SxS \_ XML \_ E \_ fehlende \_ Parser**</span><span class="sxs-lookup"><span data-stu-id="6ed93-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR\_SXS\_XML\_E\_MISSING\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-721">14044 (0x36dc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-721">14044 (0x36DC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-722">Fehler beim Analysieren der Manifeste: Klammer fehlt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-722">Manifest Parse Error : Missing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**Fehler \_ SxS \_ XML \_ E \_ expectingclosequote**</span><span class="sxs-lookup"><span data-stu-id="6ed93-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGCLOSEQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-724">14045 (0x36dd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-724">14045 (0x36DD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-725">Fehler beim Analysieren der Manifeste: ein einzelnes oder doppeltes Schließ Endes Anführungszeichen ( \\ "or \\ ") fehlt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-725">Manifest Parse Error : A single or double closing quote character (\\' or \\") is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**Fehler \_ SxS \_ XML \_ E \_ mehrere \_ Doppelpunkte**</span><span class="sxs-lookup"><span data-stu-id="6ed93-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR\_SXS\_XML\_E\_MULTIPLE\_COLONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-727">14046 (0x36de)</span><span class="sxs-lookup"><span data-stu-id="6ed93-727">14046 (0x36DE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-728">Fehler beim Analysieren der Manifeste: mehrere Doppelpunkte sind in einem Namen nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-728">Manifest Parse Error : Multiple colons are not allowed in a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültiges \_ Dezimalzeichen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_DECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-730">14047 (0x36df)</span><span class="sxs-lookup"><span data-stu-id="6ed93-730">14047 (0x36DF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-731">Fehler beim Analysieren der Manifeste: Ungültiges Zeichen für Dezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="6ed93-731">Manifest Parse Error : Invalid character for decimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültiges \_ hexadezimal**</span><span class="sxs-lookup"><span data-stu-id="6ed93-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_HEXIDECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-733">14048 (0x36e0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-733">14048 (0x36E0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-734">Fehler beim Analysieren der Manifeste: Ungültiges Zeichen für hexadezimale Ziffer.</span><span class="sxs-lookup"><span data-stu-id="6ed93-734">Manifest Parse Error : Invalid character for hexadecimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültige \_ Unicode**</span><span class="sxs-lookup"><span data-stu-id="6ed93-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR\_SXS\_XML\_E\_INVALID\_UNICODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-736">14049 (0x36e1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-736">14049 (0x36E1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-737">Fehler beim Analysieren der Manifeste: Ungültiger Unicode-Zeichen Wert für diese Plattform.</span><span class="sxs-lookup"><span data-stu-id="6ed93-737">Manifest Parse Error : Invalid unicode character value for this platform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**Fehler \_ SxS \_ XML \_ E \_ whitespaceorfrag Mark**</span><span class="sxs-lookup"><span data-stu-id="6ed93-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR\_SXS\_XML\_E\_WHITESPACEORQUESTIONMARK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-739">14050 (0x36e2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-739">14050 (0x36E2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-740">Fehler beim Analysieren der Manifeste: Es wird ein Leerzeichen oder "?" erwartet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-740">Manifest Parse Error : Expecting whitespace or '?'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**Fehler \_ SxS \_ XML \_ E \_ unexpectedendtag**</span><span class="sxs-lookup"><span data-stu-id="6ed93-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-742">14051 (0x36e3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-742">14051 (0x36E3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-743">Fehler beim Analysieren der Manifeste: an dieser Stelle wurde kein Endtag erwartet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-743">Manifest Parse Error : End tag was not expected at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedtag**</span><span class="sxs-lookup"><span data-stu-id="6ed93-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-745">14052 (0x36e4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-745">14052 (0x36E4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-746">Fehler beim Analysieren der Manifeste: die folgenden Tags wurden nicht geschlossen: %1.</span><span class="sxs-lookup"><span data-stu-id="6ed93-746">Manifest Parse Error : The following tags were not closed: %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**Fehler \_ SxS \_ XML \_ E \_ duplicateattribute**</span><span class="sxs-lookup"><span data-stu-id="6ed93-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR\_SXS\_XML\_E\_DUPLICATEATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-748">14053 (0x36e5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-748">14053 (0x36E5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-749">Fehler beim Analysieren der Manifeste: doppeltes Attribut.</span><span class="sxs-lookup"><span data-stu-id="6ed93-749">Manifest Parse Error : Duplicate attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**Fehler \_ SxS \_ XML \_ E \_ multipleroots**</span><span class="sxs-lookup"><span data-stu-id="6ed93-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR\_SXS\_XML\_E\_MULTIPLEROOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-751">14054 (0x36e6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-751">14054 (0x36E6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-752">Fehler beim Analysieren der Manifeste: in einem XML-Dokument ist nur ein Element der obersten Ebene zulässig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-752">Manifest Parse Error : Only one top level element is allowed in an XML document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**Fehler \_ SxS \_ XML \_ E \_ invalidatrootlevel**</span><span class="sxs-lookup"><span data-stu-id="6ed93-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR\_SXS\_XML\_E\_INVALIDATROOTLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-754">14055 (0x36e7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-754">14055 (0x36E7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-755">Fehler beim Analysieren der Manifeste: auf oberster Ebene des Dokuments ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-755">Manifest Parse Error : Invalid at the top level of the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**Fehler \_ SxS \_ XML \_ E \_ badxmldecl**</span><span class="sxs-lookup"><span data-stu-id="6ed93-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR\_SXS\_XML\_E\_BADXMLDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-757">14056 (0x36e8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-757">14056 (0x36E8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-758">Fehler beim Analysieren der Manifeste: Ungültige XML-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="6ed93-758">Manifest Parse Error : Invalid xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**Fehler \_ SxS \_ XML \_ E \_ missingroot**</span><span class="sxs-lookup"><span data-stu-id="6ed93-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR\_SXS\_XML\_E\_MISSINGROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-760">14057 (0x36e9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-760">14057 (0x36E9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-761">Fehler beim Analysieren der Manifeste: das XML-Dokument muss ein Element der obersten Ebene aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-761">Manifest Parse Error : XML document must have a top level element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**Fehler \_ SxS \_ XML \_ E \_ unexpectedeof**</span><span class="sxs-lookup"><span data-stu-id="6ed93-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDEOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-763">14058 (0x36ea)</span><span class="sxs-lookup"><span data-stu-id="6ed93-763">14058 (0x36EA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-764">Fehler beim Analysieren der Manifeste: Unerwartetes Dateiende.</span><span class="sxs-lookup"><span data-stu-id="6ed93-764">Manifest Parse Error : Unexpected end of file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**Fehler \_ SxS \_ XML \_ E \_ badperefinsubset**</span><span class="sxs-lookup"><span data-stu-id="6ed93-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR\_SXS\_XML\_E\_BADPEREFINSUBSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-766">14059 (0x36eb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-766">14059 (0x36EB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-767">Fehler beim Analysieren der Manifeste: Parameter Entitäten können nicht innerhalb von Markup Deklarationen in einer internen Teilmenge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-767">Manifest Parse Error : Parameter entities cannot be used inside markup declarations in an internal subset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedstarttag**</span><span class="sxs-lookup"><span data-stu-id="6ed93-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTARTTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-769">14060 (0x36ec)</span><span class="sxs-lookup"><span data-stu-id="6ed93-769">14060 (0x36EC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-770">Fehler beim Analysieren der Manifeste: das Element wurde nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-770">Manifest Parse Error : Element was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedendtag**</span><span class="sxs-lookup"><span data-stu-id="6ed93-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-772">14061 (0x36ed)</span><span class="sxs-lookup"><span data-stu-id="6ed93-772">14061 (0x36ED)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-773">Fehler beim Analysieren der Manifeste: das Endelement hat das Zeichen ' > ' fehlt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-773">Manifest Parse Error : End element was missing the character '>'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedstring**</span><span class="sxs-lookup"><span data-stu-id="6ed93-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-775">14062 (0x36ee)</span><span class="sxs-lookup"><span data-stu-id="6ed93-775">14062 (0x36EE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-776">Fehler beim Analysieren der Manifeste: ein Zeichenfolgenliteral wurde nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-776">Manifest Parse Error : A string literal was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedcomment**</span><span class="sxs-lookup"><span data-stu-id="6ed93-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCOMMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-778">14063 (0x36ef)</span><span class="sxs-lookup"><span data-stu-id="6ed93-778">14063 (0x36EF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-779">Fehler beim Analysieren der Manifeste: ein Kommentar wurde nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-779">Manifest Parse Error : A comment was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**Fehler \_ SxS \_ XML \_ E \_ uncloseddecl**</span><span class="sxs-lookup"><span data-stu-id="6ed93-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-781">14064 (0x36f 0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-781">14064 (0x36F0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-782">Fehler beim Analysieren der Manifeste: eine Deklaration wurde nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-782">Manifest Parse Error : A declaration was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**Fehler \_ SxS \_ XML \_ E \_ unclosedcdata**</span><span class="sxs-lookup"><span data-stu-id="6ed93-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-784">14065 (0x36f 1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-784">14065 (0x36F1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-785">Fehler beim Analysieren der Manifeste: ein CDATA-Abschnitt wurde nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-785">Manifest Parse Error : A CDATA section was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**Fehler \_ SxS \_ XML \_ E \_ reservednamespace**</span><span class="sxs-lookup"><span data-stu-id="6ed93-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR\_SXS\_XML\_E\_RESERVEDNAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-787">14066 (0x36f 2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-787">14066 (0x36F2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-788">Fehler beim Analysieren der Manifeste: das Namespace Präfix darf nicht mit der reservierten Zeichenfolge "XML" beginnen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-788">Manifest Parse Error : The namespace prefix is not allowed to start with the reserved string "xml".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**Fehler \_ SxS \_ XML \_ E \_ invalidencoding**</span><span class="sxs-lookup"><span data-stu-id="6ed93-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR\_SXS\_XML\_E\_INVALIDENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-790">14067 (0x36f 3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-790">14067 (0x36F3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-791">Fehler beim Analysieren der Manifeste: das System unterstützt die angegebene Codierung nicht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-791">Manifest Parse Error : System does not support the specified encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**Fehler \_ SxS \_ XML \_ E \_ invalidswitch**</span><span class="sxs-lookup"><span data-stu-id="6ed93-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR\_SXS\_XML\_E\_INVALIDSWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-793">14068 (0x36f 4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-793">14068 (0x36F4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-794">Fehler beim Analysieren der Manifeste: der Wechsel von der aktuellen Codierung zur angegebenen Codierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-794">Manifest Parse Error : Switch from current encoding to specified encoding not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**Fehler \_ SxS \_ XML \_ E \_ badxmlcase**</span><span class="sxs-lookup"><span data-stu-id="6ed93-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR\_SXS\_XML\_E\_BADXMLCASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-796">14069 (0x36f 5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-796">14069 (0x36F5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-797">Fehler beim Analysieren der Manifeste: der Name "XML" ist reserviert und muss in Kleinbuchstaben vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-797">Manifest Parse Error : The name 'xml' is reserved and must be lower case.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültiges \_ eigenständiges**</span><span class="sxs-lookup"><span data-stu-id="6ed93-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR\_SXS\_XML\_E\_INVALID\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-799">14070 (0x36f 6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-799">14070 (0x36F6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-800">Fehler beim Analysieren der Manifeste: das eigenständige Attribut muss den Wert "yes" oder "No" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-800">Manifest Parse Error : The standalone attribute must have the value 'yes' or 'no'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**Fehler \_ SxS \_ XML \_ E \_ unerwartet \_ eigenständig**</span><span class="sxs-lookup"><span data-stu-id="6ed93-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-802">14071 (0x36f 7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-802">14071 (0x36F7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-803">Fehler beim Analysieren der Manifeste: das eigenständige Attribut kann nicht in externen Entitäten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-803">Manifest Parse Error : The standalone attribute cannot be used in external entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**Fehler \_ SxS \_ XML \_ E \_ ungültige \_ Version.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR\_SXS\_XML\_E\_INVALID\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-805">14072 (0x36f 8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-805">14072 (0x36F8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-806">Fehler beim Analysieren der Manifeste: Ungültige Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="6ed93-806">Manifest Parse Error : Invalid version number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**Fehler \_ SxS \_ XML \_ E \_ missingequals**</span><span class="sxs-lookup"><span data-stu-id="6ed93-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR\_SXS\_XML\_E\_MISSINGEQUALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-808">14073 (0x36f 9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-808">14073 (0x36F9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-809">Fehler beim Analysieren der Manifeste: Fehlendes Gleichheitszeichen zwischen Attribut und Attribut Wert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-809">Manifest Parse Error : Missing equals sign between attribute and attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**Fehler beim Wiederherstellen des \_ SxS- \_ Schutzes. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR\_SXS\_PROTECTION\_RECOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-811">14074 (0x36fa)</span><span class="sxs-lookup"><span data-stu-id="6ed93-811">14074 (0x36FA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-812">Fehler beim assemblyschutz: die angegebene Assembly kann nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-812">Assembly Protection Error : Unable to recover the specified assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**Fehler \_ SxS- \_ Schutz \_ öffentlicher \_ Schlüssel \_ zu \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="6ed93-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR\_SXS\_PROTECTION\_PUBLIC\_KEY\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-814">14075 (0x36fb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-814">14075 (0x36FB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-815">Fehler beim assemblyschutz: der öffentliche Schlüssel für eine Assembly war zu kurz, um zugelassen zu werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-815">Assembly Protection Error : The public key for an assembly was too short to be allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**Fehler \_ SxS \_ - \_ Schutz \_ Katalog \_ ungültig**</span><span class="sxs-lookup"><span data-stu-id="6ed93-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-817">14076 (0x36fc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-817">14076 (0x36FC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-818">Fehler beim assemblyschutz: der Katalog für eine Assembly ist ungültig oder entspricht nicht dem Assemblymanifest.</span><span class="sxs-lookup"><span data-stu-id="6ed93-818">Assembly Protection Error : The catalog for an assembly is not valid, or does not match the assembly's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**Fehler \_ SxS \_ nicht übersetz bares \_ HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6ed93-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR\_SXS\_UNTRANSLATABLE\_HRESULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-820">14077 (0x36fd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-820">14077 (0x36FD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-821">Ein HRESULT konnte nicht in einen entsprechenden Win32-Fehlercode übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-821">An HRESULT could not be translated to a corresponding Win32 error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**Fehler " \_ SxS \_ Protection \_ catalog \_ file" \_ fehlt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_FILE\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-823">14078 (0x36fe)</span><span class="sxs-lookup"><span data-stu-id="6ed93-823">14078 (0x36FE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-824">Fehler beim assemblyschutz: der Katalog für eine Assembly fehlt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-824">Assembly Protection Error : The catalog for an assembly is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**Fehler \_ SxS \_ fehlende \_ Assembly- \_ Identitäts \_ Attribut**</span><span class="sxs-lookup"><span data-stu-id="6ed93-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR\_SXS\_MISSING\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-826">14079 (0x36ff)</span><span class="sxs-lookup"><span data-stu-id="6ed93-826">14079 (0x36FF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-827">In der angegebenen Assemblyidentität fehlt mindestens ein Attribut, das in diesem Kontext vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="6ed93-827">The supplied assembly identity is missing one or more attributes which must be present in this context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**Fehler \_ SxS \_ Ungültiger assemblyidentitäts- \_ \_ \_ Attribut \_ Name**</span><span class="sxs-lookup"><span data-stu-id="6ed93-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-829">14080 (0x3700)</span><span class="sxs-lookup"><span data-stu-id="6ed93-829">14080 (0x3700)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-830">Die angegebene Assemblyidentität verfügt über einen oder mehrere Attributnamen, die Zeichen enthalten, die in XML-Namen nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="6ed93-830">The supplied assembly identity has one or more attribute names that contain characters not permitted in XML names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**Fehler \_ SxS- \_ Assembly \_ fehlt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR\_SXS\_ASSEMBLY\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-832">14081 (0x3701)</span><span class="sxs-lookup"><span data-stu-id="6ed93-832">14081 (0x3701)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-833">Die Assembly, auf die verwiesen wird, wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-833">The referenced assembly could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**Fehler \_ SxS \_ beschädigte \_ Aktivierungs \_ Stapel**</span><span class="sxs-lookup"><span data-stu-id="6ed93-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR\_SXS\_CORRUPT\_ACTIVATION\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-835">14082 (0x3702)</span><span class="sxs-lookup"><span data-stu-id="6ed93-835">14082 (0x3702)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-836">Der Aktivierungs Kontext-Aktivierungs Stapel für den Ausführungs Thread der Ausführung ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-836">The activation context activation stack for the running thread of execution is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**Fehler \_ SxS-Beschädigung \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR\_SXS\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-838">14083 (0x3703)</span><span class="sxs-lookup"><span data-stu-id="6ed93-838">14083 (0x3703)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-839">Die anwendungsisolations-Metadaten für diesen Prozess oder Thread sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-839">The application isolation metadata for this process or thread has become corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**Fehler \_ SxS \_ frühe \_ Deaktivierung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR\_SXS\_EARLY\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-841">14084 (0x3704)</span><span class="sxs-lookup"><span data-stu-id="6ed93-841">14084 (0x3704)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-842">Der aktivierte Aktivierungs Kontext ist nicht der zuletzt aktivierte Aktivierungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="6ed93-842">The activation context being deactivated is not the most recently activated one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**Fehler \_ SxS \_ - \_ Deaktivierung ist ungültig.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR\_SXS\_INVALID\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-844">14085 (0x3705)</span><span class="sxs-lookup"><span data-stu-id="6ed93-844">14085 (0x3705)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-845">Der aktivierte Aktivierungs Kontext ist für den aktuellen Ausführungs Thread nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="6ed93-845">The activation context being deactivated is not active for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**Fehler \_ SxS \_ Multiple \_ Deactivation**</span><span class="sxs-lookup"><span data-stu-id="6ed93-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR\_SXS\_MULTIPLE\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-847">14086 (0x3706)</span><span class="sxs-lookup"><span data-stu-id="6ed93-847">14086 (0x3706)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-848">Der aktivierte Aktivierungs Kontext wurde bereits deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-848">The activation context being deactivated has already been deactivated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**Fehler beim Beenden des \_ SxS- \_ Prozesses. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR\_SXS\_PROCESS\_TERMINATION\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-850">14087 (0x3707)</span><span class="sxs-lookup"><span data-stu-id="6ed93-850">14087 (0x3707)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-851">Eine Komponente, die von der Isolations Funktion verwendet wird, hat das Beenden des Prozesses angefordert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-851">A component used by the isolation facility has requested to terminate the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**Fehler \_ SxS \_ - \_ releaseaktivierungs- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="6ed93-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR\_SXS\_RELEASE\_ACTIVATION\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-853">14088 (0x3708)</span><span class="sxs-lookup"><span data-stu-id="6ed93-853">14088 (0x3708)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-854">Eine Kernelmoduskomponente gibt einen Verweis auf einen Aktivierungs kontextfrei.</span><span class="sxs-lookup"><span data-stu-id="6ed93-854">A kernel mode component is releasing a reference on an activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**Fehler \_ SxS- \_ System \_ Standard \_ Aktivierungs \_ Kontext \_ leer**</span><span class="sxs-lookup"><span data-stu-id="6ed93-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR\_SXS\_SYSTEM\_DEFAULT\_ACTIVATION\_CONTEXT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-856">14089 (0x3709)</span><span class="sxs-lookup"><span data-stu-id="6ed93-856">14089 (0x3709)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-857">Der Aktivierungs Kontext der Standardassembly des Systems konnte nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-857">The activation context of system default assembly could not be generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**Fehler \_ SxS \_ ungültiger \_ Identitäts \_ Attribut \_ Wert.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-859">14090 (0x370a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-859">14090 (0x370A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-860">Der Wert eines Attributs in einer Identität liegt nicht innerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="6ed93-860">The value of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**Fehler \_ SxS \_ ungültiger \_ Identitäts \_ Attribut \_ Name.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-862">14091 (0x370b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-862">14091 (0x370B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-863">Der Name eines Attributs in einer Identität liegt nicht innerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="6ed93-863">The name of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**Fehler \_ SxS- \_ Identität \_ dupliziertes \_ Attribut**</span><span class="sxs-lookup"><span data-stu-id="6ed93-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR\_SXS\_IDENTITY\_DUPLICATE\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-865">14092 (0x370c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-865">14092 (0x370C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-866">Eine Identität enthält zwei Definitionen für dasselbe Attribut.</span><span class="sxs-lookup"><span data-stu-id="6ed93-866">An identity contains two definitions for the same attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**Fehler beim Analysieren der Fehler \_ SxS- \_ Identität \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR\_SXS\_IDENTITY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-868">14093 (0x370d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-868">14093 (0x370D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-869">Die Identitäts Zeichenfolge ist falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-869">The identity string is malformed.</span></span> <span data-ttu-id="6ed93-870">Dies kann auf ein nach gestelltes Komma, mehr als zwei unbenannte Attribute, den fehlenden Attributnamen oder den fehlenden Attribut Wert zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="6ed93-870">This may be due to a trailing comma, more than two unnamed attributes, missing attribute name or missing attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**fehlerhafte Ersetzungs \_ \_ \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ed93-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR\_MALFORMED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-872">14094 (0x370e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-872">14094 (0x370E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-873">Eine Zeichenfolge mit lokalisiertem austauschbaren Inhalt ist falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-873">A string containing localized substitutable content was malformed.</span></span> <span data-ttu-id="6ed93-874">Auf ein Dollarzeichen ($) wurde etwas anderes als eine linke Klammer oder ein anderes Dollarzeichen gefolgt, oder es wurde keine Rechte Klammer gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-874">Either a dollar sign ($) was followed by something other than a left parenthesis or another dollar sign or an substitution's right parenthesis was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**Fehler \_ SxS \_ falsches \_ öffentliches \_ Schlüssel \_ Token.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR\_SXS\_INCORRECT\_PUBLIC\_KEY\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-876">14095 (0x370f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-876">14095 (0x370F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-877">Das öffentliche Schlüssel Token entspricht nicht dem angegebenen öffentlichen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6ed93-877">The public key token does not correspond to the public key specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**nicht zugeordnete Ersetzungs \_ \_ \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ed93-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR\_UNMAPPED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-879">14096 (0x3710)</span><span class="sxs-lookup"><span data-stu-id="6ed93-879">14096 (0x3710)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-880">Eine Ersatz Zeichenfolge hatte keine Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-880">A substitution string had no mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**Fehler \_ SxS- \_ Assembly \_ nicht \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-882">14097 (0x3711))</span><span class="sxs-lookup"><span data-stu-id="6ed93-882">14097 (0x3711)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-883">Die Komponente muss vor dem Ausführen der Anforderung gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-883">The component must be locked before making the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**Fehler \_ SxS- \_ Komponenten \_ Speicher \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR\_SXS\_COMPONENT\_STORE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-885">14098 (0x3712)</span><span class="sxs-lookup"><span data-stu-id="6ed93-885">14098 (0x3712)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-886">Der Komponenten Speicher ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-886">The component store has been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**Fehler beim \_ Advanced \_ Installer \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR\_ADVANCED\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-888">14099 (0x3713)</span><span class="sxs-lookup"><span data-stu-id="6ed93-888">14099 (0x3713)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-889">Ein erweiterter Installer konnte während der Einrichtung oder Wartung nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-889">An advanced installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**Fehler bei der \_ XML- \_ Codierung. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR\_XML\_ENCODING\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-891">14100 (0x3714)</span><span class="sxs-lookup"><span data-stu-id="6ed93-891">14100 (0x3714)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-892">Die Zeichencodierung in der XML-Deklaration entsprach nicht der im Dokument verwendeten Codierung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-892">The character encoding in the XML declaration did not match the encoding used in the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**Fehler \_ SxS- \_ Manifest- \_ Identität identisch, \_ \_ aber \_ \_ andere Inhalte**</span><span class="sxs-lookup"><span data-stu-id="6ed93-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR\_SXS\_MANIFEST\_IDENTITY\_SAME\_BUT\_CONTENTS\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-894">14101 (0x3715)</span><span class="sxs-lookup"><span data-stu-id="6ed93-894">14101 (0x3715)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-895">Die Identitäten der Manifeste sind identisch, aber ihre Inhalte unterscheiden sich.</span><span class="sxs-lookup"><span data-stu-id="6ed93-895">The identities of the manifests are identical but their contents are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**Fehler \_ SxS- \_ Identitäten \_ anders**</span><span class="sxs-lookup"><span data-stu-id="6ed93-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR\_SXS\_IDENTITIES\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-897">14102 (0x3716)</span><span class="sxs-lookup"><span data-stu-id="6ed93-897">14102 (0x3716)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-898">Die Komponenten Identitäten unterscheiden sich.</span><span class="sxs-lookup"><span data-stu-id="6ed93-898">The component identities are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**Fehler \_ SxS \_ - \_ Assembly \_ ist \_ keine \_ Bereitstellung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR\_SXS\_ASSEMBLY\_IS\_NOT\_A\_DEPLOYMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-900">14103 (0x3717)</span><span class="sxs-lookup"><span data-stu-id="6ed93-900">14103 (0x3717)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-901">Die Assembly ist keine Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-901">The assembly is not a deployment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**Fehler \_ SxS- \_ Datei ist \_ nicht \_ Teil \_ der \_ Assembly.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR\_SXS\_FILE\_NOT\_PART\_OF\_ASSEMBLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-903">14104 (0x3718)</span><span class="sxs-lookup"><span data-stu-id="6ed93-903">14104 (0x3718)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-904">Die Datei ist kein Teil der Assembly.</span><span class="sxs-lookup"><span data-stu-id="6ed93-904">The file is not a part of the assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**Fehler \_ SxS- \_ Manifest \_ zu \_ groß**</span><span class="sxs-lookup"><span data-stu-id="6ed93-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERROR\_SXS\_MANIFEST\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-906">14105 (0x3719)</span><span class="sxs-lookup"><span data-stu-id="6ed93-906">14105 (0x3719)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-907">Die Größe des Manifests überschreitet den zulässigen Höchstwert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-907">The size of the manifest exceeds the maximum allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**Fehler \_ SxS- \_ Einstellung \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR\_SXS\_SETTING\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-909">14106 (0x371a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-909">14106 (0x371A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-910">Die Einstellung ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-910">The setting is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**Fehler beim \_ Abschluss der SxS- \_ Transaktion \_ \_ unvollständig.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR\_SXS\_TRANSACTION\_CLOSURE\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-912">14107 (0x371b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-912">14107 (0x371B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-913">Mindestens ein erforderliches Mitglied der Transaktion ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-913">One or more required members of the transaction are not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**Fehler bei \_ SMI- \_ primitiver \_ Installer \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR\_SMI\_PRIMITIVE\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-915">14108 (0x371c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-915">14108 (0x371C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-916">Der SMI-primitive Installer ist während des Setups oder der Wartung fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-916">The SMI primitive installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**Fehler beim \_ generischen \_ Befehl. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR\_GENERIC\_COMMAND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-918">14109 (0x371d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-918">14109 (0x371D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-919">Eine generische Befehlsdatei hat ein Ergebnis zurückgegeben, das einen Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-919">A generic command executable returned a result that indicates failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**Fehler \_ SxS \_ - \_ Dateihash \_ fehlt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR\_SXS\_FILE\_HASH\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-921">14110 (0x371e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-921">14110 (0x371E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-922">In einer Komponente fehlen Informationen zur Dateiüberprüfung im Manifest.</span><span class="sxs-lookup"><span data-stu-id="6ed93-922">A component is missing file verification information in its manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**Fehler beim Auftreten eines \_ \_ ungültigen \_ Kanal \_ Pfads.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-924">15000 (0x3a98)</span><span class="sxs-lookup"><span data-stu-id="6ed93-924">15000 (0x3A98)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-925">Der angegebene Kanalpfad ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-925">The specified channel path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**Fehler beim Auftreten einer \_ \_ ungültigen \_ Abfrage**</span><span class="sxs-lookup"><span data-stu-id="6ed93-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-927">15001 (0x3a99)</span><span class="sxs-lookup"><span data-stu-id="6ed93-927">15001 (0x3A99)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-928">Die angegebene Abfrage ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-928">The specified query is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**Fehler beim Auftreten von \_ \_ Verleger \_ Metadaten \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-930">15002 (0x3a9a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-930">15002 (0x3A9A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-931">Die Verleger Metadaten wurden in der Ressource nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-931">The publisher metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**Fehler \_ Ereignis Vorlage "Fehler Ereignis" wurde \_ \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-933">15003 (0x3a9b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-933">15003 (0x3A9B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-934">Die Vorlage für eine Ereignis Definition wurde in der Ressource nicht gefunden (Fehler = %1).</span><span class="sxs-lookup"><span data-stu-id="6ed93-934">The template for an event definition cannot be found in the resource (error = %1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**\_ \_ ungültiger \_ Herausgeber \_ Name**</span><span class="sxs-lookup"><span data-stu-id="6ed93-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-936">15004 (0x3a9c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-936">15004 (0x3A9C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-937">Der angegebene Herausgeber Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-937">The specified publisher name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**Fehler beim Auftreten von \_ \_ ungültigen \_ Ereignis \_ Daten.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-939">15005 (0x3a9d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-939">15005 (0x3A9D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-940">Die Ereignisdaten, die vom Verleger ausgelöst werden, sind nicht mit der Definition der Ereignis Vorlage im Manifest des Verlegers kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6ed93-940">The event data raised by the publisher is not compatible with the event template definition in the publisher's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**Fehler beim \_ EVT- \_ Kanal \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-942">15007 (0x3a9f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-942">15007 (0x3A9F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-943">Der angegebene Kanal konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-943">The specified channel could not be found.</span></span> <span data-ttu-id="6ed93-944">Überprüfen Sie die Kanal Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6ed93-944">Check channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**fehlerhafter \_ \_ XML- \_ \_ Text Fehler.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-946">15008 (0x3aa0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-946">15008 (0x3AA0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-947">Der angegebene XML-Text war nicht wohl geformt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-947">The specified xml text was not well-formed.</span></span> <span data-ttu-id="6ed93-948">Weitere Informationen finden Sie unter Erweiterter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-948">See Extended Error for more details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**Fehler " \_ evt"- \_ Abonnement \_ für \_ direkten \_ Kanal**</span><span class="sxs-lookup"><span data-stu-id="6ed93-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-950">15009 (0x3aa1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-950">15009 (0x3AA1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-951">Der Aufrufer versucht, einen direkten Kanal zu abonnieren, der nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-951">The caller is trying to subscribe to a direct channel which is not allowed.</span></span> <span data-ttu-id="6ed93-952">Die Ereignisse für einen direkten Kanal gelangen direkt in eine Protokolldatei und können nicht abonniert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-952">The events for a direct channel go directly to a logfile and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**Fehler bei \_ EVT- \_ Konfigurations \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-954">15010 (0x3aa2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-954">15010 (0x3AA2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-955">Konfigurationsfehler.</span><span class="sxs-lookup"><span data-stu-id="6ed93-955">Configuration error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**Fehler beim auslassen der \_ \_ Abfrage \_ Ergebnisse \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-957">15011 (0x3aa3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-957">15011 (0x3AA3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-958">Das Abfrageergebnis ist veraltet/ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-958">The query result is stale / invalid.</span></span> <span data-ttu-id="6ed93-959">Dies kann darauf zurückzuführen sein, dass das Protokoll gelöscht oder ein Rollback ausgeführt wird, nachdem das Abfrageergebnis erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed93-959">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="6ed93-960">Benutzer sollten diesen Code behandeln, indem Sie das Abfrageergebnis Objekt freigeben und die Abfrage erneut ausstellen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-960">Users should handle this code by releasing the query result object and reissuing the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**Fehler bei der \_ \_ Abfrage \_ Ergebnis \_ ungültige \_ Position**</span><span class="sxs-lookup"><span data-stu-id="6ed93-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-962">15012 (0x3aa4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-962">15012 (0x3AA4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-963">Das Abfrageergebnis ist zurzeit an einer ungültigen Position.</span><span class="sxs-lookup"><span data-stu-id="6ed93-963">Query result is currently at an invalid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**Fehler beim \_ \_ nicht \_ Validieren von \_ MSXML.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-965">15013 (0x3aa5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-965">15013 (0x3AA5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-966">Registrierte MSXML unterstützt keine Validierung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-966">Registered MSXML doesn't support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**Fehler beim Filtern von " \_ \_ \_ alread-scoped".**</span><span class="sxs-lookup"><span data-stu-id="6ed93-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-968">15014 (0x3aa6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-968">15014 (0x3AA6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-969">Auf einen Ausdruck kann nur eine Änderung des Bereichs Vorgangs folgen, wenn er selbst zu einer Knotengruppe ausgewertet wird und nicht bereits Teil einer anderen Änderung des Bereichs Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-969">An expression can only be followed by a change of scope operation if it itself evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**Fehler beim \_ \_ Filtern von \_ noteltset.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-971">15015 (0x3aa7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-971">15015 (0x3AA7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-972">Ein Schritt Vorgang kann nicht von einem Begriff durchgeführt werden, der keinen Element Satz darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-972">Can't perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**Fehler " \_ EVT Filter"- \_ Filter \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-974">15016 (0x3aa8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-974">15016 (0x3AA8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-975">Linke Seiten Argumente für binäre Operatoren müssen entweder Attribute, Knoten oder Variablen sein, und Rechte Argumente müssen Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="6ed93-975">Left hand side arguments to binary operators must be either attributes, nodes or variables and right hand side arguments must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**Fehler beim \_ \_ Filter zum Filtern \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-977">15017 (0x3aa9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-977">15017 (0x3AA9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-978">Ein Schritt Vorgang muss entweder einen Knoten Test oder, im Falle eines Prädikats, einen algebraischen Ausdruck einschließen, mit dem jeder Knoten in der Knotengruppe, der durch den vorangehenden Knoten Satz identifiziert wird, getestet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ed93-978">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceeding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**\_ \_ Fehlertyp \_ Filtertyp Filtern**</span><span class="sxs-lookup"><span data-stu-id="6ed93-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-980">15018 (0x3aaa)</span><span class="sxs-lookup"><span data-stu-id="6ed93-980">15018 (0x3AAA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-981">Dieser Datentyp wird derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-981">This data type is currently unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**Fehler beim \_ \_ Filtern der \_ parameterr**</span><span class="sxs-lookup"><span data-stu-id="6ed93-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-983">15019 (0x3aab)</span><span class="sxs-lookup"><span data-stu-id="6ed93-983">15019 (0x3AAB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-984">Syntax Fehler an Position %1! d!.</span><span class="sxs-lookup"><span data-stu-id="6ed93-984">A syntax error occurred at position %1!d!.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**Fehler beim Filtern von " \_ \_ \_ unsupportedop".**</span><span class="sxs-lookup"><span data-stu-id="6ed93-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-986">15020 (0x3aac)</span><span class="sxs-lookup"><span data-stu-id="6ed93-986">15020 (0x3AAC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-987">Dieser Operator wird von dieser Implementierung des Filters nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-987">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**Fehler beim Filtern von " \_ \_ \_ unexpectedtoken".**</span><span class="sxs-lookup"><span data-stu-id="6ed93-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-989">15021 (0x3aad)</span><span class="sxs-lookup"><span data-stu-id="6ed93-989">15021 (0x3AAD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-990">Unerwartetes Token.</span><span class="sxs-lookup"><span data-stu-id="6ed93-990">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**Fehler durch \_ \_ ungültigen \_ Vorgang \_ über \_ aktiviertem \_ direkt \_ Kanal**</span><span class="sxs-lookup"><span data-stu-id="6ed93-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-992">15022 (0x3aae)</span><span class="sxs-lookup"><span data-stu-id="6ed93-992">15022 (0x3AAE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-993">Der angeforderte Vorgang kann nicht über einen aktivierten direkten Kanal ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-993">The requested operation cannot be performed over an enabled direct channel.</span></span> <span data-ttu-id="6ed93-994">Der Kanal muss zuerst deaktiviert werden, bevor der angeforderte Vorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed93-994">The channel must first be disabled before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**Error \_ EVT \_ ungültiger \_ \_ channeleigenschafts \_ Wert.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-996">15023 (0x3aaf)</span><span class="sxs-lookup"><span data-stu-id="6ed93-996">15023 (0x3AAF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-997">Kanal Eigenschaft %1! s!</span><span class="sxs-lookup"><span data-stu-id="6ed93-997">Channel property %1!s!</span></span> <span data-ttu-id="6ed93-998">enthält einen ungültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-998">contains invalid value.</span></span> <span data-ttu-id="6ed93-999">Der Wert weist einen ungültigen Typ auf, liegt außerhalb des gültigen Bereichs, kann nicht aktualisiert werden oder wird von diesem Kanaltyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-999">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**Error \_ EVT \_ ungültiger \_ Verleger \_ Eigenschafts \_ Wert.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1001">15024 (0x3ab0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1001">15024 (0x3AB0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1002">Verleger Eigenschaft %1! s!</span><span class="sxs-lookup"><span data-stu-id="6ed93-1002">Publisher property %1!s!</span></span> <span data-ttu-id="6ed93-1003">enthält einen ungültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1003">contains invalid value.</span></span> <span data-ttu-id="6ed93-1004">Der Wert weist einen ungültigen Typ auf, liegt außerhalb des gültigen Bereichs, kann nicht aktualisiert werden oder wird von diesem Typ von Verleger nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1004">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**\_fehlerevt- \_ Kanal \_ kann nicht \_ aktiviert werden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1006">15025 (0x3ab1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1006">15025 (0x3AB1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1007">Der Kanal kann nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1007">The channel fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**Fehler beim \_ \_ Filter \_ zu \_ Komplex.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1009">15026 (0x3ab2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1009">15026 (0x3AB2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1010">Der XPath-Ausdruck hat unterstützte Komplexität überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1010">The xpath expression exceeded supported complexity.</span></span> <span data-ttu-id="6ed93-1011">Fügen Sie Sie ein, oder Teilen Sie Sie in zwei oder mehr einfache Ausdrücke auf.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1011">Please symplify it or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**Fehler \_ Meldung "evt" wurde \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1013">15027 (0x3ab3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1013">15027 (0x3AB3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1014">die Nachrichten Ressource ist vorhanden, aber die Nachricht wurde nicht in der Zeichenfolge/Nachrichten Tabelle gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1014">the message resource is present but the message is not found in the string/message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**Fehler- \_ EVT-nach \_ richten- \_ ID \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1016">15028 (0x3ab4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1016">15028 (0x3AB4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1017">Die Nachrichten-ID für die gewünschte Nachricht wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1017">The message id for the desired message could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**Fehler beim Einfügen von nicht aufgelösten \_ \_ \_ Werten. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1019">15029 (0x3ab5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1019">15029 (0x3AB5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1020">Die Ersetzungs Zeichenfolge für den Einfügeindex (%1) wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1020">The substitution string for insert index (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**Fehler beim \_ Einfügen nicht \_ aufgelöster \_ Parameter \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1022">15030 (0x3ab6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1022">15030 (0x3AB6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1023">Die Beschreibungs Zeichenfolge für den Parameter Verweis (%1) wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1023">The description string for parameter reference (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**\_Maximale Anzahl von \_ \_ Einfügungen des \_ Fehlers**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1025">15031 (0x3ab7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1025">15031 (0x3AB7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1026">Die maximal zulässige Anzahl von Ersetzungen wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1026">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**Fehler \_ Ereignis- \_ Ereignis \_ Definition \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1028">15032 (0x3ab8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1028">15032 (0x3AB8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1029">Die Ereignis Definition für die Ereignis-ID (%1) wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1029">The event definition could not be found for event id (%1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**Fehler beim \_ EVT-Nachrichten Gebiets Schema \_ \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1031">15033 (0x3ab9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1031">15033 (0x3AB9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1032">Die Gebiets Schema spezifische Ressource für die gewünschte Nachricht ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1032">The locale specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**Fehler- \_ EVT- \_ Version \_ zu \_ alt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1034">15034 (0x3aba)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1034">15034 (0x3ABA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1035">Die Ressource ist zu alt, um kompatibel zu sein.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1035">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**Fehler- \_ EVT- \_ Version \_ zu \_ neu**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1037">15035 (0x3abb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1037">15035 (0x3ABB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1038">Die Ressource ist zu neu, um kompatibel zu sein.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1038">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**Fehler \_ EVT \_ kann \_ den \_ Kanal \_ der \_ Abfrage nicht öffnen.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1040">15036 (0x3abc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1040">15036 (0x3ABC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1041">Der Kanal bei Index %1! d!</span><span class="sxs-lookup"><span data-stu-id="6ed93-1041">The channel at index %1!d!</span></span> <span data-ttu-id="6ed93-1042">der Abfrage kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1042">of the query can't be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**Fehler beim \_ Deaktivieren des \_ Verlegers \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1044">15037 (0x3abd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1044">15037 (0x3ABD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1045">Der Verleger wurde deaktiviert, und die zugehörige Ressource ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1045">The publisher has been disabled and its resource is not available.</span></span> <span data-ttu-id="6ed93-1046">Dies tritt normalerweise auf, wenn der Verleger gerade deinstalliert oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1046">This usually occurs when the publisher is in the process of being uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**Fehler beim \_ \_ Filtern \_ \_ im \_ Bereich.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1048">15038 (0x3abe)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1048">15038 (0x3ABE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1049">Es wurde versucht, einen numerischen Typ zu erstellen, der außerhalb des gültigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1049">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**Fehler beim Aktivieren des \_ EC- \_ Abonnements \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR\_EC\_SUBSCRIPTION\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1051">15080 (0x3ae8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1051">15080 (0x3AE8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1052">Das Abonnement kann nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1052">The subscription fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**Fehler- \_ EC- \_ Protokoll \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR\_EC\_LOG\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1054">15081 (0x3ae9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1054">15081 (0x3AE9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1055">Das Protokoll des Abonnements befindet sich im deaktivierten Zustand und kann nicht zum Weiterleiten von Ereignissen an verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1055">The log of the subscription is in disabled state, and can not be used to forward events to.</span></span> <span data-ttu-id="6ed93-1056">Das Protokoll muss zuerst aktiviert werden, bevor das Abonnement aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1056">The log must first be enabled before the subscription can be activated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**Fehler bei \_ EC- \_ Kreis \_ Weiterleitung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR\_EC\_CIRCULAR\_FORWARDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1058">15082 (0x3aea)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1058">15082 (0x3AEA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1059">Beim Weiterleiten von Ereignissen vom lokalen Computer an sich selbst kann die Abfrage des Abonnements kein Ziel Protokoll des Abonnements enthalten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1059">When forwarding events from local machine to itself, the query of the subscription can't contain target log of the subscription.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**Fehler beim Aufrufen von " \_ EC- \_ Speicher" \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR\_EC\_CREDSTORE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1061">15083 (0x3aeb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1061">15083 (0x3AEB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1062">Der Anmelde Informationsspeicher, der zum Speichern der Anmelde Informationen verwendet wird, ist voll.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1062">The credential store that is used to save credentials is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**Fehler beim Aufrufen der "EC"-Funktion. \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR\_EC\_CRED\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1064">15084 (0x3aec)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1064">15084 (0x3AEC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1065">Die von diesem Abonnement verwendeten Anmelde Informationen können im Anmelde Informationsspeicher nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1065">The credential used by this subscription can't be found in credential store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**Fehler- \_ EC \_ ohne \_ aktiven \_ Kanal**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR\_EC\_NO\_ACTIVE\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1067">15085 (0x3aed)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1067">15085 (0x3AED)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1068">Es wurde kein aktiver Kanal für die Abfrage gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1068">No active channel is found for the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**Fehler- \_ MUI- \_ Datei wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERROR\_MUI\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1070">15100 (0x3afc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1070">15100 (0x3AFC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1071">Der Ressourcen Lader konnte die MUI-Datei nicht finden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1071">The resource loader failed to find MUI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**\_ungültige fehlermui- \_ \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR\_MUI\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1073">15101 (0x3afd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1073">15101 (0x3AFD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1074">Fehler beim Laden der MUI-Datei durch das Ressourcen Lade Modul, weil die Überprüfung der Datei fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1074">The resource loader failed to load MUI file because the file fail to pass validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**Fehler- \_ MUI \_ ungültige \_ RC- \_ Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR\_MUI\_INVALID\_RC\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1076">15102 (0x3afe)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1076">15102 (0x3AFE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1077">Das RC-Manifest ist mit Garbage Data oder nicht unterstützter Version beschädigt, oder das erforderliche Element ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1077">The RC Manifest is corrupted with garbage data or unsupported version or missing required item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**\_ \_ Ungültiger Name für \_ Fehler-MUI \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR\_MUI\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1079">15103 (0x3aff)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1079">15103 (0x3AFF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1080">Das RC-Manifest hat einen ungültigen Kultur Namen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1080">The RC Manifest has invalid culture name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**Fehler \_ MUI \_ ungültiger \_ ultimatefallbackname. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR\_MUI\_INVALID\_ULTIMATEFALLBACK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1082">15104 (0x3b00)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1082">15104 (0x3B00)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1083">Das RC-Manifest weist einen ungültigen ultimatefallback-Namen auf.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1083">The RC Manifest has invalid ultimatefallback name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**die \_ fehlermui- \_ Datei wurde \_ nicht \_ geladen.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR\_MUI\_FILE\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1085">15105 (0x3b01)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1085">15105 (0x3B01)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1086">Der Ressourcen Lade Cache hat keinen geladenen MUI-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1086">The resource loader cache doesn't have loaded MUI entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**Fehler \_ Ressourcen- \_ Enum- \_ Benutzer \_ Beendigung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR\_RESOURCE\_ENUM\_USER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1088">15106 (0x3b02)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1088">15106 (0x3B02)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1089">Die Ressourcen Aufzählung wurde vom Benutzer beendet.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1089">User stopped resource enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**Fehler \_ MUI \_ intlsettings \_ uilang \_ nicht \_ installiert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR\_MUI\_INTLSETTINGS\_UILANG\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1091">15107 (0x3b03)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1091">15107 (0x3B03)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1092">Fehler beim Installieren der Benutzeroberflächen Sprache.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1092">UI language installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**Error \_ MUI \_ intlsettings \_ Ungültiger Gebiets Schema \_ \_ Name**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR\_MUI\_INTLSETTINGS\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1094">15108 (0x3b04)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1094">15108 (0x3B04)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1095">Fehler bei der Gebiets Schema Installation.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1095">Locale installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**Fehler \_ MRM \_ Runtime \_ keine \_ standardmäßige \_ oder \_ neutrale \_ Ressource**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR\_MRM\_RUNTIME\_NO\_DEFAULT\_OR\_NEUTRAL\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1097">15110 (0x3b06)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1097">15110 (0x3B06)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1098">Eine Ressource weist keinen standardmäßigen oder neutralen Wert auf.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1098">A resource does not have default or neutral value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**Fehler \_ MRM \_ ungültige \_ priconfig.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR\_MRM\_INVALID\_PRICONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1100">15111 (0x3b07)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1100">15111 (0x3B07)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1101">Ungültige PRI-Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1101">Invalid PRI config file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**Fehler bei \_ MRM \_ ungültiger \_ \_ Dateityp.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR\_MRM\_INVALID\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1103">15112 (0x3b08)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1103">15112 (0x3B08)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1104">Ungültiger Dateityp.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1104">Invalid file type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**Fehler \_ MRM \_ unbekannter \_ Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR\_MRM\_UNKNOWN\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1106">15113 (0x3b09)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1106">15113 (0x3B09)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1107">Unbekannter Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1107">Unknown qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**Fehler bei \_ MRM \_ ungültiger \_ qualifiziererwert \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1109">15114 (0x3b0a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1109">15114 (0x3B0A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1110">Ungültiger qualifiziererwert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1110">Invalid qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**Fehler \_ MRM \_ Nein \_ Candidate**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR\_MRM\_NO\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1112">15115 (0x3b0b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1112">15115 (0x3B0B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1113">Es wurde kein Kandidat gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1113">No Candidate found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**Fehler \_ MRM \_ keine Entsprechung \_ \_ oder \_ Standard \_ Kandidat**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR\_MRM\_NO\_MATCH\_OR\_DEFAULT\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1115">15116 (0x3b0c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1115">15116 (0x3B0C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1116">ResourceMap oder namedresource verfügt über ein Element, das nicht über eine Standard-oder neutrale Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1116">The ResourceMap or NamedResource has an item that does not have default or neutral resource..</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**Fehler bei der \_ MRM- \_ Ressourcen \_ Typen \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR\_MRM\_RESOURCE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1118">15117 (0x3b0d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1118">15117 (0x3B0D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1119">Ungültiger resourcecandidate-Typ.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1119">Invalid ResourceCandidate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**Fehler \_ MRM \_ doppelter Zuordnungs \_ \_ Name.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR\_MRM\_DUPLICATE\_MAP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1121">15118 (0x3b0e)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1121">15118 (0x3B0E)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1122">Doppelte Ressourcen Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1122">Duplicate Resource Map.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**Fehler beim \_ \_ doppelten \_ Eintrag von MRM.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR\_MRM\_DUPLICATE\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1124">15119 (0x3b0f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1124">15119 (0x3B0F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1125">Doppelter Eintrag.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1125">Duplicate Entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**Fehler bei \_ MRM, \_ ungültiger \_ Ressourcen \_ Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR\_MRM\_INVALID\_RESOURCE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1127">15120 (0x3b10)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1127">15120 (0x3B10)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1128">Ungültiger Ressourcen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1128">Invalid Resource Identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**Fehler beim \_ MRM- \_ Dateipfad \_ zu \_ lang.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR\_MRM\_FILEPATH\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1130">15121 (0x3b11)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1130">15121 (0x3B11)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1131">Der Dateipfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1131">Filepath too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**Fehler \_ MRM \_ nicht unterstützter \_ \_ Verzeichnistyp**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR\_MRM\_UNSUPPORTED\_DIRECTORY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1133">15122 (0x3b12)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1133">15122 (0x3B12)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1134">Nicht unterstützter Verzeichnistyp.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1134">Unsupported directory type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**Fehler bei \_ MRM, \_ ungültige \_ pri- \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR\_MRM\_INVALID\_PRI\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1136">15126 (0x3b16)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1136">15126 (0x3B16)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1137">Ungültige PRI-Datei.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1137">Invalid PRI File.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**Fehler \_ MRM \_ benannte \_ Ressource \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR\_MRM\_NAMED\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1139">15127 (0x3b17)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1139">15127 (0x3B17)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1140">"Namedresource" wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1140">NamedResource Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**Fehler \_ MRM-Zuordnung wurde \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR\_MRM\_MAP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1142">15135 (0x3b1f)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1142">15135 (0x3B1F)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1143">ResourceMap nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1143">ResourceMap Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**Fehler \_ MRM \_ nicht unterstützter \_ \_ Profiltyp**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR\_MRM\_UNSUPPORTED\_PROFILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1145">15136 (0x3b20)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1145">15136 (0x3B20)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1146">Nicht unterstützter MRT-Profiltyp.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1146">Unsupported MRT profile type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**Fehler bei \_ MRM \_ ungültiger \_ qualifiziereroperator \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1148">15137 (0x3b21)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1148">15137 (0x3B21)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1149">Ungültiger qualifiziereroperator.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1149">Invalid qualifier operator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**Fehler beim \_ unbestimmten Wert von MRM- \_ \_ Qualifizierer \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR\_MRM\_INDETERMINATE\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1151">15138 (0x3b22)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1151">15138 (0x3B22)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1152">Der qualifiziererwert oder der qualifiziererwert konnte nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1152">Unable to determine qualifier value or qualifier value has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**Fehler beim \_ Aktivieren von MRM \_ AutoMerge. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR\_MRM\_AUTOMERGE\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1154">15139 (0x3b23)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1154">15139 (0x3B23)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1155">AutoMerge ist in der PRI-Datei aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1155">Automerge is enabled in the PRI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**Fehler \_ MRM \_ zu \_ viele \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR\_MRM\_TOO\_MANY\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1157">15140 (0x3b24)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1157">15140 (0x3B24)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1158">Es wurden zu viele Ressourcen für das Paket definiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1158">Too many resources defined for package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**Fehler bei \_ MCA \_ ungültige Funktions \_ \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR\_MCA\_INVALID\_CAPABILITIES\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1160">15200 (0x3b60)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1160">15200 (0x3B60)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1161">Der Monitor hat eine DDC/CI-Funktions Zeichenfolge zurückgegeben, die nicht der Spezifikation "Access. Bus 3,0", "DDC/CI 1,1" oder "MCCS 2 Revision 1" entsprach.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1161">The monitor returned a DDC/CI capabilities string that did not comply with the ACCESS.bus 3.0, DDC/CI 1.1 or MCCS 2 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**Fehler bei \_ MCA, \_ ungültige \_ VCP- \_ Version.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR\_MCA\_INVALID\_VCP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1163">15201 (0x3b61)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1163">15201 (0x3B61)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1164">Der VCP-Code der VCP-Version (0xDF) des Monitors hat einen ungültigen Versions Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1164">The monitor's VCP Version (0xDF) VCP code returned an invalid version value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**Fehler \_ MCA- \_ Monitor \_ verstößt gegen \_ MCCS- \_ Spezifikation**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR\_MCA\_MONITOR\_VIOLATES\_MCCS\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1166">15202 (0x3b62)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1166">15202 (0x3B62)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1167">Der Monitor entspricht nicht der MCCS-Spezifikation, die er vorgibt, Sie zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1167">The monitor does not comply with the MCCS specification it claims to support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**Fehler bei \_ MCA- \_ MCCS- \_ Versions \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR\_MCA\_MCCS\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1169">15203 (0x3b63)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1169">15203 (0x3B63)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1170">Die MCCS-Version in der MCCS ver-Funktion eines Monitors \_ entspricht nicht der MCCS-Version, die der Monitor meldet, wenn der VCP-Code (0xDF) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1170">The MCCS version in a monitor's mccs\_ver capability does not match the MCCS version the monitor reports when the VCP Version (0xDF) VCP code is used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**Fehler \_ MCA, \_ nicht unterstützte \_ MCCS- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR\_MCA\_UNSUPPORTED\_MCCS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1172">15204 (0x3b64)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1172">15204 (0x3B64)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1173">Die Monitor Konfigurations-API funktioniert nur mit Monitoren, die die MCCs 1,0 Specification, MCCS 2,0 Specification oder die MCCS 2,0 Revision 1-Spezifikation unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1173">The Monitor Configuration API only works with monitors that support the MCCS 1.0 specification, MCCS 2.0 specification or the MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**Fehler bei \_ MCA- \_ interner \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR\_MCA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1175">15205 (0x3b65)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1175">15205 (0x3B65)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1176">Interner Fehler bei der Monitor Konfigurations-API.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1176">An internal Monitor Configuration API error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**Fehler bei \_ MCA- \_ ungültigem \_ \_ technologientyp \_ zurückgegeben**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR\_MCA\_INVALID\_TECHNOLOGY\_TYPE\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1178">15206 (0x3b66)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1178">15206 (0x3B66)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1179">Der Monitor hat einen ungültigen Monitor-Technologietyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1179">The monitor returned an invalid monitor technology type.</span></span> <span data-ttu-id="6ed93-1180">CRT, Plasma und LCD (TFT) sind Beispiele für Überwachungstechnologie Typen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1180">CRT, Plasma and LCD (TFT) are examples of monitor technology types.</span></span> <span data-ttu-id="6ed93-1181">Dieser Fehler impliziert, dass der Monitor die MCCS 2,0-oder MCCS 2,0 Revision 1-Spezifikation verletzt hat.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1181">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**Fehler bei \_ MCA \_ nicht unterstützte \_ Farb \_ Temperatur**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR\_MCA\_UNSUPPORTED\_COLOR\_TEMPERATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1183">15207 (0x3b67)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1183">15207 (0x3B67)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1184">Der Aufrufer von [**setmonitorcolortemperatur**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) hat eine Farbtemperatur angegeben, die vom aktuellen Monitor nicht unterstützt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1184">The caller of [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) specified a color temperature that the current monitor did not support.</span></span> <span data-ttu-id="6ed93-1185">Dieser Fehler impliziert, dass der Monitor die MCCS 2,0-oder MCCS 2,0 Revision 1-Spezifikation verletzt hat.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1185">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**Fehler \_ mehrdeutiges \_ System \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR\_AMBIGUOUS\_SYSTEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1187">15250 (0x3b92)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1187">15250 (0x3B92)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1188">Das angeforderte System Gerät kann nicht identifiziert werden, weil mehrere indizierbare Geräte möglicherweise den Identifikations Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1188">The requested system device cannot be identified due to multiple indistinguishable devices potentially matching the identification criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**Fehler \_ System \_ Gerät \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR\_SYSTEM\_DEVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1190">15299 (0x3bc3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1190">15299 (0x3BC3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1191">Das angeforderte System Gerät wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1191">The requested system device cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**Fehler \_ Hash \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR\_HASH\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1193">15300 (0x3bc4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1193">15300 (0x3BC4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1194">Die Hash Generierung für die angegebene Hash Version und den Hashtyp ist auf dem Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1194">Hash generation for the specified hash version and hash type is not enabled on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**Fehler \_ Hash \_ nicht \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR\_HASH\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1196">15301 (0x3bc5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1196">15301 (0x3BC5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1197">Der vom Server angeforderte Hash ist nicht verfügbar oder nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1197">The hash requested from the server is not available or no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**Fehler \_ beim sekundären \_ IC- \_ Anbieter \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR\_SECONDARY\_IC\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1199">15321 (0x3bd9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1199">15321 (0x3BD9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1200">Die sekundäre interruptcontrollerinstanz, die den angegebenen Interrupt verwaltet, ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1200">The secondary interrupt controller instance that manages the specified interrupt is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**Fehler bei \_ GPIO- \_ Client \_ Informationen \_ ungültig.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR\_GPIO\_CLIENT\_INFORMATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1202">15322 (0x3bda)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1202">15322 (0x3BDA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1203">Die vom GPIO-Client Treiber bereitgestellten Informationen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1203">The information supplied by the GPIO client driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**Fehler- \_ GPIO- \_ Version \_ \_ wird nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR\_GPIO\_VERSION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1205">15323 (0x3bdb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1205">15323 (0x3BDB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1206">Die vom GPIO-Client Treiber angegebene Version wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1206">The version specified by the GPIO client driver is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**Fehler beim \_ GPIO- \_ \_ Registrierungs \_ Paket.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR\_GPIO\_INVALID\_REGISTRATION\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1208">15324 (0x3bdc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1208">15324 (0x3BDC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1209">Das vom GPIO-Client Treiber bereitgestellte Registrierungspaket ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1209">The registration packet supplied by the GPIO client driver is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**Fehler beim \_ GPIO- \_ Vorgang. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR\_GPIO\_OPERATION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1211">15325 (0x3bdd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1211">15325 (0x3BDD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1212">Der angeforderte Vorgang wird für das angegebene Handle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1212">The requested operation is not supported for the specified handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**Fehler beim \_ GPIO- \_ inkompatiblen \_ Verbindungs \_ Modus.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR\_GPIO\_INCOMPATIBLE\_CONNECT\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1214">15326 (0x3bde)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1214">15326 (0x3BDE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1215">Der angeforderte Verbindungs Modus steht in Konflikt mit einem vorhandenen Modus auf einem oder mehreren der angegebenen Pins.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1215">The requested connect mode conflicts with an existing mode on one or more of the specified pins.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**Fehler beim \_ GPIO- \_ Interrupt ist \_ bereits \_ aufgehoben.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR\_GPIO\_INTERRUPT\_ALREADY\_UNMASKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1217">15327 (0x3bdf)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1217">15327 (0x3BDF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1218">Der für die Maskierung angeforderte Interrupt ist nicht maskiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1218">The interrupt requested to be unmasked is not masked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**Fehler \_ beim \_ Umschalten von \_ Runlevel.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR\_CANNOT\_SWITCH\_RUNLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1220">15400 (0x3c28)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1220">15400 (0x3C28)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1221">Der angeforderte Schalter auf Lauf Ebene kann nicht erfolgreich abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1221">The requested run level switch cannot be completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**Fehler \_ ungültige \_ Runlevel- \_ Einstellung.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR\_INVALID\_RUNLEVEL\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1223">15401 (0x3c29)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1223">15401 (0x3C29)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1224">Der Dienst hat eine ungültige Einstellung für die Lauf Ebene.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1224">The service has an invalid run level setting.</span></span> <span data-ttu-id="6ed93-1225">Die Lauf Ebene für einen Dienst darf nicht höher sein als die Lauf Ebene der abhängigen Dienste.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1225">The run level for a service must not be higher than the run level of its dependent services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**Timeout für Fehler bei \_ Runlevel- \_ Switch \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1227">15402 (0x3c2a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1227">15402 (0x3C2A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1228">Der angeforderte Schalter auf Lauf Ebene kann nicht erfolgreich abgeschlossen werden, da ein oder mehrere Dienste innerhalb des angegebenen Timeouts nicht beendet oder neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1228">The requested run level switch cannot be completed successfully since one or more services will not stop or restart within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**\_Timeout für Switch-Agent- \_ \_ \_ Timeout für Fehler**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_AGENT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1230">15403 (0x3c2b)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1230">15403 (0x3C2B)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1231">Ein Switch-Agent auf Lauf Ebene hat innerhalb des angegebenen Timeouts nicht reagiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1231">A run level switch agent did not respond within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**Fehler \_ beim Ausführen \_ \_ des \_ Fehlers "Runlevel"**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR\_RUNLEVEL\_SWITCH\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1233">15404 (0x3c2c)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1233">15404 (0x3C2C)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1234">Zurzeit wird ein Switch auf Lauf Ebene ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1234">A run level switch is currently in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**Fehler \_ Dienste \_ beim \_ Autostart**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR\_SERVICES\_FAILED\_AUTOSTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1236">15405 (0x3c2d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1236">15405 (0x3C2D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1237">Mindestens ein Dienst konnte während der Dienst Startphase eines Schalters auf Lauf Ebene nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1237">One or more services failed to start during the service startup phase of a run level switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**Fehler bei \_ com- \_ Task \_ Beendigung \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR\_COM\_TASK\_STOP\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1239">15501 (0x3c8d)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1239">15501 (0x3C8D)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1240">Die Anforderung zum Beenden der Aufgabe kann nicht sofort abgeschlossen werden, da die Aufgabe mehr Zeit zum Herunterfahren benötigt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1240">The task stop request cannot be completed immediately since task needs more time to shutdown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**Fehler beim \_ Installieren des \_ geöffneten \_ Pakets \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1242">15600 (0x3cf0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1242">15600 (0x3CF0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1243">Das Paket konnte nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1243">Package could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**Fehler beim \_ Installieren des \_ Pakets \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR\_INSTALL\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1245">15601 (0x3cf1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1245">15601 (0x3CF1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1246">Das Paket wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1246">Package was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**Fehler beim \_ Installieren des \_ ungültigen \_ Pakets**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR\_INSTALL\_INVALID\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1248">15602 (0x3cf2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1248">15602 (0x3CF2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1249">Die Paketdaten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1249">Package data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**Fehler beim \_ Installieren der \_ \_ Abhängigkeits Abhängigkeit \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR\_INSTALL\_RESOLVE\_DEPENDENCY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1251">15603 (0x3cf3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1251">15603 (0x3CF3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1252">Paketfehler bei Updates, Abhängigkeits-oder Konflikt Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1252">Package failed updates, dependency or conflict validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**Fehler beim \_ installieren \_ von nicht genügend \_ \_ Speicher \_ Platz.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR\_INSTALL\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1254">15604 (0x3cf4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1254">15604 (0x3CF4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1255">Auf dem Computer ist nicht genügend Speicherplatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1255">There is not enough disk space on your computer.</span></span> <span data-ttu-id="6ed93-1256">Geben Sie Speicherplatz frei, und wiederholen Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1256">Please free up some space and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**Fehler beim \_ Installieren des \_ Netzwerk \_ Fehlers.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR\_INSTALL\_NETWORK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1258">15605 (0x3cf5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1258">15605 (0x3CF5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1259">Beim Herunterladen des Produkts ist ein Problem aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1259">There was a problem downloading your product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**Fehler beim \_ Installieren der \_ Registrierung. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR\_INSTALL\_REGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1261">15606 (0x3cf6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1261">15606 (0x3CF6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1262">Das Paket konnte nicht registriert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1262">Package could not be registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**Fehler beim Installieren der Registrierungs Registrierung. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR\_INSTALL\_DEREGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1264">15607 (0x3cf7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1264">15607 (0x3CF7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1265">Die Registrierung des Pakets konnte nicht aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1265">Package could not be unregistered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**Fehler bei \_ Installation \_ Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR\_INSTALL\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1267">15608 (0x3cf8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1267">15608 (0x3CF8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1268">Der Benutzer hat die Installations Anforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1268">User cancelled the install request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**Fehler bei der \_ Installation. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR\_INSTALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1270">15609 (0x3cf9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1270">15609 (0x3CF9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1271">Fehler bei der Installation.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1271">Install failed.</span></span> <span data-ttu-id="6ed93-1272">Wenden Sie sich an den Softwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1272">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**Fehler beim \_ entfernen. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR\_REMOVE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1274">15610 (0x3cfa)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1274">15610 (0x3CFA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1275">Fehler beim Entfernen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1275">Removal failed.</span></span> <span data-ttu-id="6ed93-1276">Wenden Sie sich an den Softwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1276">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**das Fehler \_ Paket ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**ERROR\_PACKAGE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1278">15611 (0x3cfb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1278">15611 (0x3CFB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1279">Das bereitgestellte Paket ist bereits installiert, und die erneute Installation des Pakets wurde blockiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1279">The provided package is already installed, and reinstallation of the package was blocked.</span></span> <span data-ttu-id="6ed93-1280">Weitere Informationen finden Sie im Ereignisprotokoll AppXDeployment-Server.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1280">Check the AppXDeployment-Server event log for details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**Fehler \_ \_ Behebung erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1282">15612 (0x3cfc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1282">15612 (0x3CFC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1283">Die Anwendung kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1283">The application cannot be started.</span></span> <span data-ttu-id="6ed93-1284">Installieren Sie die Anwendung neu, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1284">Try reinstalling the application to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**Fehler beim \_ Installieren der \_ erforderlichen Komponente. \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR\_INSTALL\_PREREQUISITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1286">15613 (0x3cfd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1286">15613 (0x3CFD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1287">Eine Voraussetzung für eine Installation konnte nicht erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1287">A Prerequisite for an install could not be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**Fehler \_ Paketrepository \_ \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERROR\_PACKAGE\_REPOSITORY\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1289">15614 (0x3cfe)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1289">15614 (0x3CFE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1290">Das Paketrepository ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1290">The package repository is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**Fehler beim \_ Installieren der \_ Richtlinie \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR\_INSTALL\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1292">15615 (0x3cff)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1292">15615 (0x3CFF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1293">Um diese Anwendung zu installieren, benötigen Sie entweder eine Windows-Entwicklerlizenz oder ein System mit Sideloading.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1293">To install this application you need either a Windows developer license or a sideloading-enabled system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**Fehler \_ Paket \_ Aktualisierung**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERROR\_PACKAGE\_UPDATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1295">15616 (0x3d00)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1295">15616 (0x3D00)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1296">Die Anwendung kann nicht gestartet werden, da Sie zurzeit aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1296">The application cannot be started because it is currently updating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**Fehler \_ Bereitstellung \_ blockiert \_ durch \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERROR\_DEPLOYMENT\_BLOCKED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1298">15617 (0x3d01)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1298">15617 (0x3D01)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1299">Der Paket Bereitstellungs Vorgang wird durch die Richtlinie blockiert.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1299">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="6ed93-1300">Wenden Sie sich an Ihren Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1300">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_verwendete Fehler \_ Pakete \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**ERROR\_PACKAGES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1302">15618 (0x3d02)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1302">15618 (0x3D02)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1303">Das Paket konnte nicht installiert werden, da die von ihm modifizierenden Ressourcen zurzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1303">The package could not be installed because resources it modifies are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**Fehler \_ Wiederherstellungs \_ Datei \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERROR\_RECOVERY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1305">15619 (0x3d03)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1305">15619 (0x3D03)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1306">Das Paket konnte nicht wieder hergestellt werden, da die erforderlichen Daten für die Wiederherstellung beschädigt wurden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1306">The package could not be recovered because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**Fehler bei der \_ \_ gestaffelten \_ Signatur.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR\_INVALID\_STAGED\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1308">15620 (0x3d04)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1308">15620 (0x3D04)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1309">Die Signatur ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1309">The signature is invalid.</span></span> <span data-ttu-id="6ed93-1310">Zum Registrieren im Entwicklermodus müssen appxsignature. P7X "und AppxBlockMap.xml gültig sein oder nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1310">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or should not be present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**Fehler beim \_ Löschen des \_ vorhandenen \_ ApplicationData- \_ Speicher \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR\_DELETING\_EXISTING\_APPLICATIONDATA\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1312">15621 (0x3d05)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1312">15621 (0x3D05)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1313">Beim Löschen der bereits vorhandenen Anwendungsdaten des Pakets ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1313">An error occurred while deleting the package's previously existing application data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**Fehler beim \_ Installieren des \_ \_ paketdowngrades**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR\_INSTALL\_PACKAGE\_DOWNGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1315">15622 (0x3d06)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1315">15622 (0x3D06)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1316">Das Paket konnte nicht installiert werden, da bereits eine höhere Version dieses Pakets installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1316">The package could not be installed because a higher version of this package is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**Fehler \_ System \_ muss wieder hergestellt werden \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR\_SYSTEM\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1318">15623 (0x3d07)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1318">15623 (0x3D07)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1319">Ein Fehler in einer System Binärdatei wurde erkannt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1319">An error in a system binary was detected.</span></span> <span data-ttu-id="6ed93-1320">Versuchen Sie, den PC zu aktualisieren, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1320">Try refreshing the PC to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**Fehler beim \_ AppX- \_ Integritäts Fehler \_ \_ CLR \_ ngen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR\_APPX\_INTEGRITY\_FAILURE\_CLR\_NGEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1322">15624 (0x3d08)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1322">15624 (0x3D08)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1323">Auf dem System wurde eine beschädigte CLR ngen-Binärdatei erkannt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1323">A corrupted CLR NGEN binary was detected on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_ \_ fehlerresilienzdatei \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERROR\_RESILIENCY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1325">15625 (0x3d09)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1325">15625 (0x3D09)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1326">Der Vorgang konnte nicht fortgesetzt werden, da die erforderlichen Daten für die Wiederherstellung beschädigt wurden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1326">The operation could not be resumed because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**Fehler beim \_ Installieren des firewalldienstanbieter. \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR\_INSTALL\_FIREWALL\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1328">15626 (0x3d0a)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1328">15626 (0x3D0A)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1329">Das Paket konnte nicht installiert werden, da der Windows-Firewall-Dienst nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1329">The package could not be installed because the Windows Firewall service is not running.</span></span> <span data-ttu-id="6ed93-1330">Aktivieren Sie den Windows-Firewall-Dienst, und versuchen Sie es erneut</span><span class="sxs-lookup"><span data-stu-id="6ed93-1330">Enable the Windows Firewall service and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**appmodel- \_ Fehler " \_ kein \_ Paket"**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL\_ERROR\_NO\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1332">15700 (0x3d54)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1332">15700 (0x3D54)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1333">Der Prozess hat keine Paket Identität.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1333">The process has no package identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_Fehler Paket Laufzeit des appmodel \_ \_ \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_RUNTIME\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1335">15701 (0x3d55)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1335">15701 (0x3D55)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1336">Die Paket Laufzeitinformationen sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1336">The package runtime information is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**Identität des appmodel- \_ Fehler \_ Pakets ist \_ \_ beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_IDENTITY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1338">15702 (0x3d56)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1338">15702 (0x3D56)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1339">Die Paket Identität ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1339">The package identity is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**appmodel- \_ Fehler " \_ keine \_ Anwendung"**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL\_ERROR\_NO\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1341">15703 (0x3d57)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1341">15703 (0x3D57)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1342">Der Prozess hat keine Anwendungs Identität.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1342">The process has no application identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**Fehler beim Laden des Fehler \_ Zustands. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR\_STATE\_LOAD\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1344">15800 (0x3db8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1344">15800 (0x3DB8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1345">Fehler beim Laden des Zustands Speicher.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1345">Loading the state store failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**Fehler \_ Status beim \_ get- \_ Version \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR\_STATE\_GET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1347">15801 (0x3db9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1347">15801 (0x3DB9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1348">Fehler beim Abrufen der Zustands Version für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1348">Retrieving the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**Fehler \_ Zustands \_ Satz- \_ Version \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR\_STATE\_SET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1350">15802 (0x3dba)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1350">15802 (0x3DBA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1351">Fehler beim Festlegen der Zustands Version für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1351">Setting the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**Fehler \_ beim \_ strukturierten \_ Zurücksetzen des Fehler Zustands \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR\_STATE\_STRUCTURED\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1353">15803 (0x3dbb)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1353">15803 (0x3DBB)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1354">Fehler beim Zurücksetzen des strukturierten Zustands der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1354">Resetting the structured state of the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**Fehler \_ Status beim \_ Öffnen des \_ Containers \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR\_STATE\_OPEN\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1356">15804 (0x3dbc)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1356">15804 (0x3DBC)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1357">Der Zustands-Manager konnte den Container nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1357">State Manager failed to open the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**Fehler \_ Status beim \_ Erstellen des \_ Containers \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR\_STATE\_CREATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1359">15805 (0x3dbd)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1359">15805 (0x3DBD)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1360">Fehler beim Erstellen des Containers durch den Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1360">State Manager failed to create the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**Fehler \_ beim \_ Löschen des \_ Containers \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR\_STATE\_DELETE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1362">15806 (0x3dbe)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1362">15806 (0x3DBE)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1363">Der Status-Manager konnte den Container nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1363">State Manager failed to delete the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**Fehler beim Lesen des Fehler \_ Zustands. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR\_STATE\_READ\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1365">15807 (0x3dbf)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1365">15807 (0x3DBF)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1366">Fehler beim Lesen der Einstellung durch den Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1366">State Manager failed to read the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**Fehler beim Schreiben des Fehler \_ Zustands. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR\_STATE\_WRITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1368">15808 (0x3dc0)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1368">15808 (0x3DC0)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1369">Fehler beim Schreiben der Einstellung durch den Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1369">State Manager failed to write the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**Fehler beim Löschen des Fehler \_ Zustands. \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR\_STATE\_DELETE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1371">15809 (0x3dc1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1371">15809 (0x3DC1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1372">Fehler beim Löschen der Einstellung durch den Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1372">State Manager failed to delete the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**Fehler beim Festlegen der Fehler \_ Status \_ Abfrage. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR\_STATE\_QUERY\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1374">15810 (0x3dc2)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1374">15810 (0x3DC2)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1375">Die Einstellung konnte vom Zustands-Manager nicht abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1375">State Manager failed to query the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**Fehler \_ Status beim Lesen der zusammen \_ \_ gesetzten \_ Einstellung \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR\_STATE\_READ\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1377">15811 (0x3dc3)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1377">15811 (0x3DC3)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1378">Fehler beim Lesen der zusammengesetzten Einstellung durch den Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1378">State Manager failed to read the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**Fehler \_ Status beim \_ Schreiben zusammen \_ gesetzter \_ Einstellung \_**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR\_STATE\_WRITE\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1380">15812 (0x3dc4)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1380">15812 (0x3DC4)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1381">Fehler beim Schreiben der zusammengesetzten Einstellung durch den Zustands-Manager.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1381">State Manager failed to write the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**Fehler \_ beim \_ Aufzählen des \_ Containers \_ für den Fehlerstatus**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR\_STATE\_ENUMERATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1383">15813 (0x3dc5)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1383">15813 (0x3DC5)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1384">Der Zustands-Manager konnte die Container nicht aufzählen.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1384">State Manager failed to enumerate the containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**Fehler \_ beim \_ Aufzählen von \_ Einstellungen \_ .**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR\_STATE\_ENUMERATE\_SETTINGS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1386">15814 (0x3dc6)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1386">15814 (0x3DC6)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1387">Der Zustands-Manager konnte die Einstellungen nicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1387">State Manager failed to enumerate the settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**Fehler \_ Status-zusammen \_ gesetzte \_ Einstellung \_ Wert \_ Größen \_ Limit \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_COMPOSITE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1389">15815 (0x3dc7)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1389">15815 (0x3DC7)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1390">Die Größe des zusammengesetzten Einstellungs Werts für den Zustands-Manager hat das Limit überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1390">The size of the state manager composite setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**Fehler \_ Zustands \_ Einstellung \_ Wert für \_ Größen \_ Beschränkung \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1392">15816 (0x3dc8)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1392">15816 (0x3DC8)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1393">Die Größe des Zustands-Manager-Einstellungs Werts hat das Limit überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1393">The size of the state manager setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**Einstellung für die \_ namens Größe des Fehler Zustands wurde \_ \_ \_ \_ \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1395">15817 (0x3dc9)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1395">15817 (0x3DC9)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1396">Die Länge des Zustands-Manager-Einstellungs namens hat das Limit überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1396">The length of the state manager setting name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**Größe des Fehler \_ Zustands für \_ Container \_ Name \_ \_ \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR\_STATE\_CONTAINER\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1398">15818 (0x3dca)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1398">15818 (0x3DCA)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1399">Die Länge des Zustands-Manager-Container namens hat das Limit überschritten.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1399">The length of the state manager container name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6ed93-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**Fehler- \_ API nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="6ed93-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR\_API\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ed93-1401">15841 (0x3de 1)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1401">15841 (0x3DE1)</span></span>
</dt> <dt>



<span data-ttu-id="6ed93-1402">Diese API kann nicht im Kontext des Anwendungs Typs des Aufrufers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed93-1402">This API cannot be used in the context of the caller's application type.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ed93-1403">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ed93-1403">Requirements</span></span>



| <span data-ttu-id="6ed93-1404">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ed93-1404">Requirement</span></span> | <span data-ttu-id="6ed93-1405">Wert</span><span class="sxs-lookup"><span data-stu-id="6ed93-1405">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed93-1406">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1406">Minimum supported client</span></span><br/> | <span data-ttu-id="6ed93-1407">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ed93-1407">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6ed93-1408">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ed93-1408">Minimum supported server</span></span><br/> | <span data-ttu-id="6ed93-1409">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ed93-1409">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ed93-1410">Header</span><span class="sxs-lookup"><span data-stu-id="6ed93-1410">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ed93-1411"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ed93-1411"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed93-1412">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ed93-1412">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed93-1413">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="6ed93-1413">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
