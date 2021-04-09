---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 1700-3999 und ist für Entwickler bestimmt.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: System Fehler Codes (1700-3999) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860672"
---
# <a name="system-error-codes-1700-3999"></a><span data-ttu-id="c7755-103">System Fehler Codes (1700-3999)</span><span class="sxs-lookup"><span data-stu-id="c7755-103">System Error Codes (1700-3999)</span></span>

> [!NOTE]
> <span data-ttu-id="c7755-104">Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen.</span><span class="sxs-lookup"><span data-stu-id="c7755-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="c7755-105">Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c7755-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="c7755-106">In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) für die Fehler 1700 bis 3999 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c7755-106">The following list describes [system error codes](system-error-codes.md) for errors 1700 to 3999.</span></span> <span data-ttu-id="c7755-107">Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7755-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="c7755-108">Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".</span><span class="sxs-lookup"><span data-stu-id="c7755-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="c7755-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_ \_ ungültige \_ Zeichen folgen \_ Bindung für RPC S**</span><span class="sxs-lookup"><span data-stu-id="c7755-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC\_S\_INVALID\_STRING\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-110">1700 (0x6a4)</span><span class="sxs-lookup"><span data-stu-id="c7755-110">1700 (0x6A4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-111">Die Zeichen folgen Bindung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-111">The string binding is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**\_falsche RPC \_ - \_ Art \_ der \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="c7755-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC\_S\_WRONG\_KIND\_OF\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-113">1701 (0x6a5)</span><span class="sxs-lookup"><span data-stu-id="c7755-113">1701 (0x6A5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-114">Das Bindungs Handle ist nicht der richtige Typ.</span><span class="sxs-lookup"><span data-stu-id="c7755-114">The binding handle is not the correct type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_ungültige RPC S- \_ \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="c7755-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-116">1702 (0x6a6)</span><span class="sxs-lookup"><span data-stu-id="c7755-116">1702 (0x6A6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-117">Das Bindungs Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-117">The binding handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**"RPC \_ S \_ Prot* \_ " \_ wird nicht unterstützt.*\*</span><span class="sxs-lookup"><span data-stu-id="c7755-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC\_S\_PROTSEQ\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-119">1703 (0x6a7)</span><span class="sxs-lookup"><span data-stu-id="c7755-119">1703 (0x6A7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-120">Die RPC-Protokoll Sequenz wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-120">The RPC protocol sequence is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC- \_ S- \_ ungültige \_ RPC- \_ protsek.**</span><span class="sxs-lookup"><span data-stu-id="c7755-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC\_S\_INVALID\_RPC\_PROTSEQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-122">1704 (0x6a8)</span><span class="sxs-lookup"><span data-stu-id="c7755-122">1704 (0x6A8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-123">Die RPC-Protokoll Sequenz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-123">The RPC protocol sequence is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_ \_ ungültige RPC- \_ Zeichenfolge ( \_ UUID)**</span><span class="sxs-lookup"><span data-stu-id="c7755-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC\_S\_INVALID\_STRING\_UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-125">1705 (0x6a9)</span><span class="sxs-lookup"><span data-stu-id="c7755-125">1705 (0x6A9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-126">Der Zeichen folgen-Universal Unique Identifier (UUID) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-126">The string universal unique identifier (UUID) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_ \_ ungültiges \_ Endpunkt \_ Format für RPC-S**</span><span class="sxs-lookup"><span data-stu-id="c7755-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC\_S\_INVALID\_ENDPOINT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-128">1706 (0x6aa)</span><span class="sxs-lookup"><span data-stu-id="c7755-128">1706 (0x6AA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-129">Das Endpunkt Format ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-129">The endpoint format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_Netzwerk- \_ \_ \_ addr ist ungültig.**</span><span class="sxs-lookup"><span data-stu-id="c7755-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC\_S\_INVALID\_NET\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-131">1707 (0x6ab)</span><span class="sxs-lookup"><span data-stu-id="c7755-131">1707 (0x6AB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-132">Die Netzwerkadresse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-132">The network address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S \_ kein \_ Endpunkt \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC\_S\_NO\_ENDPOINT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-134">1708 (0x6ac)</span><span class="sxs-lookup"><span data-stu-id="c7755-134">1708 (0x6AC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-135">Es wurde kein Endpunkt gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-135">No endpoint was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**\_Ungültiges RPC S- \_ \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="c7755-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC\_S\_INVALID\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-137">1709 (0x6ad)</span><span class="sxs-lookup"><span data-stu-id="c7755-137">1709 (0x6AD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-138">Der Timeout Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-138">The timeout value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC \_ S- \_ Objekt \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="c7755-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC\_S\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-140">1710 (0x6ae)</span><span class="sxs-lookup"><span data-stu-id="c7755-140">1710 (0x6AE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-141">Der Universal Unique Identifier (UUID) des Objekts wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-141">The object universal unique identifier (UUID) was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ bereits \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="c7755-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC\_S\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-143">1711 (0x6af)</span><span class="sxs-lookup"><span data-stu-id="c7755-143">1711 (0x6AF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-144">Der Universal Unique Identifier (UUID) für das Objekt wurde bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="c7755-144">The object universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**der RPC- \_ \_ Typ ist \_ bereits \_ registriert.**</span><span class="sxs-lookup"><span data-stu-id="c7755-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**RPC\_S\_TYPE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-146">1712 (0x6b0)</span><span class="sxs-lookup"><span data-stu-id="c7755-146">1712 (0x6B0)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-147">Der typuniversal Unique Identifier (UUID) wurde bereits registriert.</span><span class="sxs-lookup"><span data-stu-id="c7755-147">The type universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC-S, die \_ \_ bereits \_ lauschen**</span><span class="sxs-lookup"><span data-stu-id="c7755-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC\_S\_ALREADY\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-149">1713 (0x6b1)</span><span class="sxs-lookup"><span data-stu-id="c7755-149">1713 (0x6B1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-150">Der RPC-Server lauscht bereits.</span><span class="sxs-lookup"><span data-stu-id="c7755-150">The RPC server is already listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S ist \_ kein " \_ protabqs" \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="c7755-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC\_S\_NO\_PROTSEQS\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-152">1714 (0x6b2)</span><span class="sxs-lookup"><span data-stu-id="c7755-152">1714 (0x6B2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-153">Es wurden keine Protokoll Sequenzen registriert.</span><span class="sxs-lookup"><span data-stu-id="c7755-153">No protocol sequences have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ nicht \_ lauscht**</span><span class="sxs-lookup"><span data-stu-id="c7755-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC\_S\_NOT\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-155">1715 (0x6b3)</span><span class="sxs-lookup"><span data-stu-id="c7755-155">1715 (0x6B3)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-156">Der RPC-Server lauscht nicht.</span><span class="sxs-lookup"><span data-stu-id="c7755-156">The RPC server is not listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_ \_ unbekannter Mgr- \_ \_ Typ "RPC S"**</span><span class="sxs-lookup"><span data-stu-id="c7755-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC\_S\_UNKNOWN\_MGR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-158">1716 (0x6b4)</span><span class="sxs-lookup"><span data-stu-id="c7755-158">1716 (0x6B4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-159">Der Manager-Typ ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-159">The manager type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ unbekannt, \_ Wenn**</span><span class="sxs-lookup"><span data-stu-id="c7755-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC\_S\_UNKNOWN\_IF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-161">1717 (0x6b5)</span><span class="sxs-lookup"><span data-stu-id="c7755-161">1717 (0x6B5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-162">Die Schnittstelle ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-162">The interface is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ keine \_ Bindungen**</span><span class="sxs-lookup"><span data-stu-id="c7755-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC\_S\_NO\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-164">1718 (0x6b6)</span><span class="sxs-lookup"><span data-stu-id="c7755-164">1718 (0x6B6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-165">Es sind keine Bindungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-165">There are no bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S ist \_ nicht \_ Prot/QS**</span><span class="sxs-lookup"><span data-stu-id="c7755-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC\_S\_NO\_PROTSEQS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-167">1719 (0x6b7)</span><span class="sxs-lookup"><span data-stu-id="c7755-167">1719 (0x6B7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-168">Es sind keine Protokoll Sequenzen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-168">There are no protocol sequences.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S \_ - \_ \_ Endpunkt erstellen**</span><span class="sxs-lookup"><span data-stu-id="c7755-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC\_S\_CANT\_CREATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-170">1720 (0x6b8)</span><span class="sxs-lookup"><span data-stu-id="c7755-170">1720 (0x6B8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-171">Der Endpunkt kann nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-171">The endpoint cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**ausgehenden RPC- \_ \_ \_ \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c7755-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC\_S\_OUT\_OF\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-173">1721 (0x6b9)</span><span class="sxs-lookup"><span data-stu-id="c7755-173">1721 (0x6B9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-174">Zum Ausführen dieses Vorgangs sind nicht genügend Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7755-174">Not enough resources are available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC \_ S- \_ Server nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="c7755-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC\_S\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-176">1722 (0x6ba)</span><span class="sxs-lookup"><span data-stu-id="c7755-176">1722 (0x6BA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-177">Der RPC-Server ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7755-177">The RPC server is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC- \_ S- \_ Server ist \_ \_ ausgelastet.**</span><span class="sxs-lookup"><span data-stu-id="c7755-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC\_S\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-179">1723 (0x6BB)</span><span class="sxs-lookup"><span data-stu-id="c7755-179">1723 (0x6BB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-180">Der RPC-Server ist zu stark ausgelastet, um diesen Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c7755-180">The RPC server is too busy to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_ \_ ungültige \_ Netzwerk \_ Optionen für RPC S**</span><span class="sxs-lookup"><span data-stu-id="c7755-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC\_S\_INVALID\_NETWORK\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-182">1724 (0x6bc)</span><span class="sxs-lookup"><span data-stu-id="c7755-182">1724 (0x6BC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-183">Die Netzwerkoptionen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-183">The network options are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ kein \_ Aufruf \_ aktiv**</span><span class="sxs-lookup"><span data-stu-id="c7755-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC\_S\_NO\_CALL\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-185">1725 (0x6bd)</span><span class="sxs-lookup"><span data-stu-id="c7755-185">1725 (0x6BD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-186">Für diesen Thread sind keine Remote Prozedur Aufrufe aktiv.</span><span class="sxs-lookup"><span data-stu-id="c7755-186">There are no remote procedure calls active on this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**Fehler beim RPC \_ S- \_ Aufruf. \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC\_S\_CALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-188">1726 (0x6be)</span><span class="sxs-lookup"><span data-stu-id="c7755-188">1726 (0x6BE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-189">Fehler beim Remote Prozedur Rückruf.</span><span class="sxs-lookup"><span data-stu-id="c7755-189">The remote procedure call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**dne-Fehler bei RPC \_ S- \_ Aufruf. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC\_S\_CALL\_FAILED\_DNE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-191">1727 (0x6bf)</span><span class="sxs-lookup"><span data-stu-id="c7755-191">1727 (0x6BF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-192">Der Remote Prozedur Rückruf ist fehlgeschlagen und wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7755-192">The remote procedure call failed and did not execute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC \_ - \_ Protokoll \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC\_S\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-194">1728 (0x6c0)</span><span class="sxs-lookup"><span data-stu-id="c7755-194">1728 (0x6C0)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-195">RPC-Protokollfehler (Remote Procedure Aufruf).</span><span class="sxs-lookup"><span data-stu-id="c7755-195">A remote procedure call (RPC) protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC- \_ e- \_ Proxy \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="c7755-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC\_S\_PROXY\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-197">1729 (0x6c1)</span><span class="sxs-lookup"><span data-stu-id="c7755-197">1729 (0x6C1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-198">Der Zugriff auf den HTTP-Proxy wird verweigert.</span><span class="sxs-lookup"><span data-stu-id="c7755-198">Access to the HTTP proxy is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**transaktionale \_ \_ nicht unterstützte \_ transaktionssyn \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC\_S\_UNSUPPORTED\_TRANS\_SYN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-200">1730 (0x6c2)</span><span class="sxs-lookup"><span data-stu-id="c7755-200">1730 (0x6C2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-201">Die Übertragungs Syntax wird vom RPC-Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-201">The transfer syntax is not supported by the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_ \_ nicht unterstützter RPC S- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="c7755-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC\_S\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-203">1732 (0x6c4)</span><span class="sxs-lookup"><span data-stu-id="c7755-203">1732 (0x6C4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-204">Der Universal Unique Identifier (UUID)-Typ wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-204">The universal unique identifier (UUID) type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**\_Ungültiges RPC S- \_ \_ Tag**</span><span class="sxs-lookup"><span data-stu-id="c7755-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC\_S\_INVALID\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-206">1733 (0x6c5)</span><span class="sxs-lookup"><span data-stu-id="c7755-206">1733 (0x6C5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-207">Das Tag ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-207">The tag is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_ungültige RPC S- \_ \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="c7755-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC\_S\_INVALID\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-209">1734 (0x6c6)</span><span class="sxs-lookup"><span data-stu-id="c7755-209">1734 (0x6C6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-210">Die Array Begrenzungen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-210">The array bounds are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S \_ No \_ Entry \_ Name**</span><span class="sxs-lookup"><span data-stu-id="c7755-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC\_S\_NO\_ENTRY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-212">1735 (0x6c7)</span><span class="sxs-lookup"><span data-stu-id="c7755-212">1735 (0x6C7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-213">Die Bindung enthält keinen Eintrags Namen.</span><span class="sxs-lookup"><span data-stu-id="c7755-213">The binding does not contain an entry name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**\_Syntax für \_ ungültigen RPC S- \_ Namen \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC\_S\_INVALID\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-215">1736 (0x6c8)</span><span class="sxs-lookup"><span data-stu-id="c7755-215">1736 (0x6C8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-216">Die namens Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-216">The name syntax is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**\_ \_ nicht unterstützte \_ Name- \_ Syntax für RPC S**</span><span class="sxs-lookup"><span data-stu-id="c7755-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC\_S\_UNSUPPORTED\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-218">1737 (0x6c9)</span><span class="sxs-lookup"><span data-stu-id="c7755-218">1737 (0x6C9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-219">Die namens Syntax wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-219">The name syntax is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC \_ S \_ UUID \_ keine \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="c7755-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC\_S\_UUID\_NO\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-221">1739 (0x6cb)</span><span class="sxs-lookup"><span data-stu-id="c7755-221">1739 (0x6CB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-222">Es ist keine Netzwerkadresse zum Erstellen eines Universal Unique Identifier (UUID) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7755-222">No network address is available to use to construct a universal unique identifier (UUID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_doppelter RPC \_ - \_ Endpunkt**</span><span class="sxs-lookup"><span data-stu-id="c7755-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC\_S\_DUPLICATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-224">1740 (0x6cc)</span><span class="sxs-lookup"><span data-stu-id="c7755-224">1740 (0x6CC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-225">Der Endpunkt ist ein Duplikat.</span><span class="sxs-lookup"><span data-stu-id="c7755-225">The endpoint is a duplicate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_ \_ unbekannter \_ authentifiztyp "RPC S" \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC\_S\_UNKNOWN\_AUTHN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-227">1741 (0x6cd)</span><span class="sxs-lookup"><span data-stu-id="c7755-227">1741 (0x6CD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-228">Der Authentifizierungstyp ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-228">The authentication type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**maximale Anzahl von RPC- \_ \_ \_ aufrufen \_ zu \_ klein**</span><span class="sxs-lookup"><span data-stu-id="c7755-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC\_S\_MAX\_CALLS\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-230">1742 (0x6ce)</span><span class="sxs-lookup"><span data-stu-id="c7755-230">1742 (0x6CE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-231">Die maximale Anzahl von Aufrufen ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="c7755-231">The maximum number of calls is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC- \_ S- \_ Zeichenfolge \_ zu \_ lang**</span><span class="sxs-lookup"><span data-stu-id="c7755-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC\_S\_STRING\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-233">1743 (0x6cf)</span><span class="sxs-lookup"><span data-stu-id="c7755-233">1743 (0x6CF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-234">Die Zeichenfolge ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="c7755-234">The string is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**"RPC \_ S \_ Prot\*" wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC\_S\_PROTSEQ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-236">1744 (0x6d0)</span><span class="sxs-lookup"><span data-stu-id="c7755-236">1744 (0x6D0)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-237">Die RPC-Protokoll Sequenz wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-237">The RPC protocol sequence was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ procnum liegt \_ außerhalb \_ des zulässigen \_ Bereichs.**</span><span class="sxs-lookup"><span data-stu-id="c7755-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC\_S\_PROCNUM\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-239">1745 (0x6d1)</span><span class="sxs-lookup"><span data-stu-id="c7755-239">1745 (0x6D1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-240">Die Prozedur Nummer liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c7755-240">The procedure number is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**die RPC \_ S- \_ Bindung \_ hat keine Authentifizierung \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="c7755-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC\_S\_BINDING\_HAS\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-242">1746 (0x6d2)</span><span class="sxs-lookup"><span data-stu-id="c7755-242">1746 (0x6D2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-243">Die Bindung enthält keine Authentifizierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="c7755-243">The binding does not contain any authentication information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_unbekannter RPC S- \_ \_ authn- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="c7755-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC\_S\_UNKNOWN\_AUTHN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-245">1747 (0x6d3)</span><span class="sxs-lookup"><span data-stu-id="c7755-245">1747 (0x6D3)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-246">Der Authentifizierungsdienst ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-246">The authentication service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**nicht auf RPC- \_ \_ \_ Ebene unbekannte authn- \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="c7755-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC\_S\_UNKNOWN\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-248">1748 (0x6d4)</span><span class="sxs-lookup"><span data-stu-id="c7755-248">1748 (0x6D4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-249">Die Authentifizierungs Ebene ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-249">The authentication level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_ \_ ungültige Authentifizierungs \_ \_ Identität für RPC-S**</span><span class="sxs-lookup"><span data-stu-id="c7755-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC\_S\_INVALID\_AUTH\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-251">1749 (0x6d5)</span><span class="sxs-lookup"><span data-stu-id="c7755-251">1749 (0x6D5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-252">Der Sicherheitskontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-252">The security context is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_unbekannter RPC S- \_ \_ Authz- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="c7755-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC\_S\_UNKNOWN\_AUTHZ\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-254">1750 (0x6d6)</span><span class="sxs-lookup"><span data-stu-id="c7755-254">1750 (0x6D6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-255">Der Autorisierungs Dienst ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-255">The authorization service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**\_ \_ Ungültiger Eintrag für EPT S \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT\_S\_INVALID\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-257">1751 (0x6d7)</span><span class="sxs-lookup"><span data-stu-id="c7755-257">1751 (0x6D7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-258">Der Eintrag ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-258">The entry is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S \_ nicht \_ Ausführen \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT\_S\_CANT\_PERFORM\_OP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-260">1752 (0x6d8)</span><span class="sxs-lookup"><span data-stu-id="c7755-260">1752 (0x6D8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-261">Der Server Endpunkt kann den Vorgang nicht durchführen.</span><span class="sxs-lookup"><span data-stu-id="c7755-261">The server endpoint cannot perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="c7755-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT\_S\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-263">1753 (0x6d9)</span><span class="sxs-lookup"><span data-stu-id="c7755-263">1753 (0x6D9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-264">Es sind keine Endpunkte mehr von der Endpunktzuordnung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7755-264">There are no more endpoints available from the endpoint mapper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC \_ S \_ Nothing \_ zum \_ exportieren**</span><span class="sxs-lookup"><span data-stu-id="c7755-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC\_S\_NOTHING\_TO\_EXPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-266">1754 (0x6da)</span><span class="sxs-lookup"><span data-stu-id="c7755-266">1754 (0x6DA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-267">Es wurden keine Schnittstellen exportiert.</span><span class="sxs-lookup"><span data-stu-id="c7755-267">No interfaces have been exported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_ \_ unvollständiger RPC- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="c7755-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC\_S\_INCOMPLETE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-269">1755 (0x6db)</span><span class="sxs-lookup"><span data-stu-id="c7755-269">1755 (0x6DB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-270">Der Eintrags Name ist unvollständig.</span><span class="sxs-lookup"><span data-stu-id="c7755-270">The entry name is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**\_Option " \_ ungültige RPC S" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC\_S\_INVALID\_VERS\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-272">1756 (0x6dc)</span><span class="sxs-lookup"><span data-stu-id="c7755-272">1756 (0x6DC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-273">Die Versions Option ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-273">The version option is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S \_ nicht \_ mehr \_ Mitglieder**</span><span class="sxs-lookup"><span data-stu-id="c7755-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC\_S\_NO\_MORE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-275">1757 (0x6dd)</span><span class="sxs-lookup"><span data-stu-id="c7755-275">1757 (0x6DD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-276">Es sind keine weiteren Mitglieder vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-276">There are no more members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ nicht \_ alle " \_ OBJS" nicht \_ exportiert**</span><span class="sxs-lookup"><span data-stu-id="c7755-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_UNEXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-278">1758 (0x6de)</span><span class="sxs-lookup"><span data-stu-id="c7755-278">1758 (0x6DE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-279">Der Export ist nicht durchgängig.</span><span class="sxs-lookup"><span data-stu-id="c7755-279">There is nothing to unexport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC \_ S- \_ Schnittstelle \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="c7755-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC\_S\_INTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-281">1759 (0x6df)</span><span class="sxs-lookup"><span data-stu-id="c7755-281">1759 (0x6DF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-282">Die Schnittstelle wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-282">The interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC \_ S- \_ Eintrag ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC\_S\_ENTRY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-284">1760 (0x6e0)</span><span class="sxs-lookup"><span data-stu-id="c7755-284">1760 (0x6E0)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-285">Der Eintrag ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-285">The entry already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC \_ S- \_ Eintrag \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="c7755-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC\_S\_ENTRY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-287">1761 (0x6e1)</span><span class="sxs-lookup"><span data-stu-id="c7755-287">1761 (0x6E1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-288">Der Eintrag wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-288">The entry is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC- \_ S- \_ Namensdienst nicht \_ \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="c7755-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC\_S\_NAME\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-290">1762 (0x6e2)</span><span class="sxs-lookup"><span data-stu-id="c7755-290">1762 (0x6E2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-291">Der Namensdienst ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7755-291">The name service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ ungültige \_ NAF- \_ ID für RPC-S**</span><span class="sxs-lookup"><span data-stu-id="c7755-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC\_S\_INVALID\_NAF\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-293">1763 (0x6e3)</span><span class="sxs-lookup"><span data-stu-id="c7755-293">1763 (0x6E3)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-294">Die Netzwerk Adressfamilie ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-294">The network address family is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ \_ unterstützt nicht**</span><span class="sxs-lookup"><span data-stu-id="c7755-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC\_S\_CANNOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-296">1764 (0x6e4)</span><span class="sxs-lookup"><span data-stu-id="c7755-296">1764 (0x6E4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-297">Der angeforderte Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-297">The requested operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S ist \_ kein \_ Kontext \_ verfügbar.**</span><span class="sxs-lookup"><span data-stu-id="c7755-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC\_S\_NO\_CONTEXT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-299">1765 (0x6e5)</span><span class="sxs-lookup"><span data-stu-id="c7755-299">1765 (0x6E5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-300">Es ist kein Sicherheitskontext verfügbar, um den Identitätswechsel zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="c7755-300">No security context is available to allow impersonation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_interner RPC \_ - \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC\_S\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-302">1766 (0x6e6)</span><span class="sxs-lookup"><span data-stu-id="c7755-302">1766 (0x6E6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-303">Interner Fehler bei einem Remote Prozedur Aufruf (RPC).</span><span class="sxs-lookup"><span data-stu-id="c7755-303">An internal error occurred in a remote procedure call (RPC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ S \_ NULL- \_ Teilung**</span><span class="sxs-lookup"><span data-stu-id="c7755-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC\_S\_ZERO\_DIVIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-305">1767 (0x6e7)</span><span class="sxs-lookup"><span data-stu-id="c7755-305">1767 (0x6E7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-306">Der RPC-Server hat eine ganzzahlige Division durch Null versucht.</span><span class="sxs-lookup"><span data-stu-id="c7755-306">The RPC server attempted an integer division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC- \_ S- \_ Adress \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC\_S\_ADDRESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-308">1768 (0x6e8)</span><span class="sxs-lookup"><span data-stu-id="c7755-308">1768 (0x6E8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-309">Beim RPC-Server ist ein Adressierungs Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c7755-309">An addressing error occurred in the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC-S (FP), \_ \_ \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="c7755-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC\_S\_FP\_DIV\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-311">1769 (0x6e9)</span><span class="sxs-lookup"><span data-stu-id="c7755-311">1769 (0x6E9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-312">Ein Gleit Komma Vorgang auf dem RPC-Server verursachte eine Division durch 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c7755-312">A floating-point operation at the RPC server caused a division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**\_LFP \_ - \_ Unterlauf in RPC**</span><span class="sxs-lookup"><span data-stu-id="c7755-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC\_S\_FP\_UNDERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-314">1770 (0x6ea)</span><span class="sxs-lookup"><span data-stu-id="c7755-314">1770 (0x6EA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-315">Auf dem RPC-Server ist ein Gleit Komma Unterlauf aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c7755-315">A floating-point underflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC- \_ S- \_ FP- \_ Überlauf**</span><span class="sxs-lookup"><span data-stu-id="c7755-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC\_S\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-317">1771 (0x6eb)</span><span class="sxs-lookup"><span data-stu-id="c7755-317">1771 (0x6EB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-318">Auf dem RPC-Server ist ein Gleit Komma Überlauf aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c7755-318">A floating-point overflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ keine \_ \_ Einträge mehr**</span><span class="sxs-lookup"><span data-stu-id="c7755-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC\_X\_NO\_MORE\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-320">1772 (0x6ec)</span><span class="sxs-lookup"><span data-stu-id="c7755-320">1772 (0x6EC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-321">Die Liste der RPC-Server, die für die Bindung von automatischen Handles verfügbar sind, ist erschöpft.</span><span class="sxs-lookup"><span data-stu-id="c7755-321">The list of RPC servers available for the binding of auto handles has been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC \_ X \_ SS \_ Char \_ Trans \_ Open \_ Fail**</span><span class="sxs-lookup"><span data-stu-id="c7755-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC\_X\_SS\_CHAR\_TRANS\_OPEN\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-323">1773 (0x6ed)</span><span class="sxs-lookup"><span data-stu-id="c7755-323">1773 (0x6ED)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-324">Die Zeichen Übersetzungs-Tabellen Datei kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-324">Unable to open the character translation table file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC \_ X \_ SS \_ Char \_ Trans \_ - \_ kurzdatei**</span><span class="sxs-lookup"><span data-stu-id="c7755-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC\_X\_SS\_CHAR\_TRANS\_SHORT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-326">1774 (0x6ee)</span><span class="sxs-lookup"><span data-stu-id="c7755-326">1774 (0x6EE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-327">Die Datei, die die Zeichen Übersetzungstabelle enthält, weist weniger als 512 Bytes auf.</span><span class="sxs-lookup"><span data-stu-id="c7755-327">The file containing the character translation table has fewer than 512 bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ in \_ NULL- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="c7755-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC\_X\_SS\_IN\_NULL\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-329">1775 (0x6ef)</span><span class="sxs-lookup"><span data-stu-id="c7755-329">1775 (0x6EF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-330">Während eines Remote Prozedur Aufrufes wurde ein NULL-Kontext Handle vom Client an den Host übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c7755-330">A null context handle was passed from the client to the host during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC \_ X \_ SS- \_ Kontext \_ beschädigt**</span><span class="sxs-lookup"><span data-stu-id="c7755-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC\_X\_SS\_CONTEXT\_DAMAGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-332">1777 (0x6F 1)</span><span class="sxs-lookup"><span data-stu-id="c7755-332">1777 (0x6F1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-333">Das Kontext Handle wurde während eines Remote Prozedur Aufrufes geändert.</span><span class="sxs-lookup"><span data-stu-id="c7755-333">The context handle changed during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC \_ X \_ SS- \_ Handles \_ stimmen nicht überein.**</span><span class="sxs-lookup"><span data-stu-id="c7755-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC\_X\_SS\_HANDLES\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-335">1778 (0x6F 2)</span><span class="sxs-lookup"><span data-stu-id="c7755-335">1778 (0x6F2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-336">Die an einen Remote Prozedur Befehl übergebenen Bindungs Handles stimmen nicht ab.</span><span class="sxs-lookup"><span data-stu-id="c7755-336">The binding handles passed to a remote procedure call do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ kann \_ kein \_ Aufruf \_ handle abrufen**</span><span class="sxs-lookup"><span data-stu-id="c7755-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC\_X\_SS\_CANNOT\_GET\_CALL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-338">1779 (0x6F 3)</span><span class="sxs-lookup"><span data-stu-id="c7755-338">1779 (0x6F3)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-339">Der Stub kann das Remote Prozedur-Rückruf Handle nicht abrufen.</span><span class="sxs-lookup"><span data-stu-id="c7755-339">The stub is unable to get the remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC \_ X \_ NULL \_ ref- \_ Zeiger**</span><span class="sxs-lookup"><span data-stu-id="c7755-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC\_X\_NULL\_REF\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-341">1780 (0x6F 4)</span><span class="sxs-lookup"><span data-stu-id="c7755-341">1780 (0x6F4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-342">Ein NULL-Verweis Zeiger wurde an den Stub übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c7755-342">A null reference pointer was passed to the stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC- \_ X- \_ \_ \_ Enumerationswert außerhalb \_ des zulässigen \_ Bereichs**</span><span class="sxs-lookup"><span data-stu-id="c7755-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-344">1781 (0x6F 5)</span><span class="sxs-lookup"><span data-stu-id="c7755-344">1781 (0x6F5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-345">Der Enumerationswert liegt außerhalb des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="c7755-345">The enumeration value is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC- \_ X- \_ Byte- \_ Anzahl \_ zu \_ klein**</span><span class="sxs-lookup"><span data-stu-id="c7755-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC\_X\_BYTE\_COUNT\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-347">1782 (0x6F 6)</span><span class="sxs-lookup"><span data-stu-id="c7755-347">1782 (0x6F6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-348">Die Byte Anzahl ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="c7755-348">The byte count is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC-X-fehlerhafte \_ \_ \_ Stub- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="c7755-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC\_X\_BAD\_STUB\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-350">1783 (0x6F 7)</span><span class="sxs-lookup"><span data-stu-id="c7755-350">1783 (0x6F7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-351">Der Stub hat ungültige Daten empfangen.</span><span class="sxs-lookup"><span data-stu-id="c7755-351">The stub received bad data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**Fehler bei \_ ungültigem \_ Benutzer \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="c7755-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR\_INVALID\_USER\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-353">1784 (0x6F 8)</span><span class="sxs-lookup"><span data-stu-id="c7755-353">1784 (0x6F8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-354">Der angegebene Benutzer Puffer ist für den angeforderten Vorgang nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-354">The supplied user buffer is not valid for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**Unbekannter Fehler. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR\_UNRECOGNIZED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-356">1785 (0x6F 9)</span><span class="sxs-lookup"><span data-stu-id="c7755-356">1785 (0x6F9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-357">Das Datenträger Medium wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-357">The disk media is not recognized.</span></span> <span data-ttu-id="c7755-358">Sie ist möglicherweise nicht formatiert.</span><span class="sxs-lookup"><span data-stu-id="c7755-358">It may not be formatted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**Fehler " \_ kein \_ vertrauenswürdiges \_ LSA- \_ Geheimnis"**</span><span class="sxs-lookup"><span data-stu-id="c7755-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR\_NO\_TRUST\_LSA\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-360">1786 (0x6fa)</span><span class="sxs-lookup"><span data-stu-id="c7755-360">1786 (0x6FA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-361">Die Arbeitsstation hat keinen geheimen Vertrauens Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c7755-361">The workstation does not have a trust secret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**Fehler " \_ kein \_ vertrauenswürdiges Sam- \_ \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="c7755-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR\_NO\_TRUST\_SAM\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-363">1787 (0x6fb)</span><span class="sxs-lookup"><span data-stu-id="c7755-363">1787 (0x6FB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-364">Die Sicherheitsdatenbank auf dem Server hat kein Computer Konto für diese Arbeitsstations-Vertrauensstellung.</span><span class="sxs-lookup"><span data-stu-id="c7755-364">The security database on the server does not have a computer account for this workstation trust relationship.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**Fehler \_ vertrauenswürdiger \_ Domäne \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR\_TRUSTED\_DOMAIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-366">1788 (0x6fc)</span><span class="sxs-lookup"><span data-stu-id="c7755-366">1788 (0x6FC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-367">Die Vertrauensstellung zwischen der primären Domäne und der vertrauenswürdigen Domäne ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7755-367">The trust relationship between the primary domain and the trusted domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**Fehler bei \_ vertrauenswürdiger \_ Beziehung \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR\_TRUSTED\_RELATIONSHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-369">1789 (0x6fd)</span><span class="sxs-lookup"><span data-stu-id="c7755-369">1789 (0x6FD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-370">Bei der Vertrauensstellung zwischen der Arbeitsstation und der primären Domäne ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c7755-370">The trust relationship between this workstation and the primary domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**Fehler bei \_ Vertrauensstellung \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-372">1790 (0x6fe)</span><span class="sxs-lookup"><span data-stu-id="c7755-372">1790 (0x6FE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-373">Die Netzwerk Anmeldung ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7755-373">The network logon failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC \_ S- \_ Aufruf wird \_ ausgeführt. \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC\_S\_CALL\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-375">1791 (0x6ff)</span><span class="sxs-lookup"><span data-stu-id="c7755-375">1791 (0x6FF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-376">Für diesen Thread wird bereits ein Remote Prozedur Aufrufvorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7755-376">A remote procedure call is already in progress for this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**Fehler \_ Netlogon wurde \_ nicht \_ gestartet.**</span><span class="sxs-lookup"><span data-stu-id="c7755-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR\_NETLOGON\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-378">1792 (0x700)</span><span class="sxs-lookup"><span data-stu-id="c7755-378">1792 (0x700)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-379">Es wurde versucht, sich anzumelden, aber der Netzwerk Anmeldedienst wurde nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="c7755-379">An attempt was made to logon, but the network logon service was not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**Fehler \_ Konto ist \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="c7755-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**ERROR\_ACCOUNT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-381">1793 (0x701)</span><span class="sxs-lookup"><span data-stu-id="c7755-381">1793 (0x701)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-382">Das Konto des Benutzers ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="c7755-382">The user's account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**Fehler \_ Redirector \_ hat \_ geöffnete \_ Handles**</span><span class="sxs-lookup"><span data-stu-id="c7755-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**ERROR\_REDIRECTOR\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-384">1794 (0x702)</span><span class="sxs-lookup"><span data-stu-id="c7755-384">1794 (0x702)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-385">Der Redirector wird verwendet und kann nicht entladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-385">The redirector is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**der Fehler \_ Drucker \_ Treiber ist \_ bereits \_ installiert.**</span><span class="sxs-lookup"><span data-stu-id="c7755-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR\_PRINTER\_DRIVER\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-387">1795 (0x703)</span><span class="sxs-lookup"><span data-stu-id="c7755-387">1795 (0x703)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-388">Der angegebene Druckertreiber ist bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="c7755-388">The specified printer driver is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**\_unbekannter \_ Port für Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR\_UNKNOWN\_PORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-390">1796 (0x704)</span><span class="sxs-lookup"><span data-stu-id="c7755-390">1796 (0x704)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-391">Der angegebene Port ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-391">The specified port is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**Fehler \_ unbekannter \_ Drucker \_ Treiber**</span><span class="sxs-lookup"><span data-stu-id="c7755-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR\_UNKNOWN\_PRINTER\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-393">1797 (0x705)</span><span class="sxs-lookup"><span data-stu-id="c7755-393">1797 (0x705)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-394">Der Druckertreiber ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-394">The printer driver is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**Unbekannter Fehler in \_ \_ PrintProcessor.**</span><span class="sxs-lookup"><span data-stu-id="c7755-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR\_UNKNOWN\_PRINTPROCESSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-396">1798 (0x706)</span><span class="sxs-lookup"><span data-stu-id="c7755-396">1798 (0x706)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-397">Der Druck Prozessor ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-397">The print processor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**Fehler bei \_ ungültiger \_ Trenn \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="c7755-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR\_INVALID\_SEPARATOR\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-399">1799 (0x707)</span><span class="sxs-lookup"><span data-stu-id="c7755-399">1799 (0x707)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-400">Die angegebene Trenn Datei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-400">The specified separator file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**Fehler \_ ungültige \_ Priorität.**</span><span class="sxs-lookup"><span data-stu-id="c7755-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR\_INVALID\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-402">1800 (0x708)</span><span class="sxs-lookup"><span data-stu-id="c7755-402">1800 (0x708)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-403">Die angegebene Priorität ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-403">The specified priority is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**Fehler \_ ungültiger \_ Drucker \_ Name**</span><span class="sxs-lookup"><span data-stu-id="c7755-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR\_INVALID\_PRINTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-405">1801 (0x709)</span><span class="sxs-lookup"><span data-stu-id="c7755-405">1801 (0x709)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-406">Der Druckername ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-406">The printer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**der Fehler \_ Drucker ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**ERROR\_PRINTER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-408">1802 (0x70a)</span><span class="sxs-lookup"><span data-stu-id="c7755-408">1802 (0x70A)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-409">Der Drucker ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-409">The printer already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**Fehler bei \_ ungültigem \_ Drucker \_ Befehl.**</span><span class="sxs-lookup"><span data-stu-id="c7755-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR\_INVALID\_PRINTER\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-411">1803 (0x70b)</span><span class="sxs-lookup"><span data-stu-id="c7755-411">1803 (0x70B)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-412">Der Drucker Befehl ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-412">The printer command is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**\_ungültiger \_ Datentyp.**</span><span class="sxs-lookup"><span data-stu-id="c7755-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR\_INVALID\_DATATYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-414">1804 (0x70c)</span><span class="sxs-lookup"><span data-stu-id="c7755-414">1804 (0x70C)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-415">Der angegebene Datentyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-415">The specified datatype is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**\_ungültige \_ Umgebung**</span><span class="sxs-lookup"><span data-stu-id="c7755-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR\_INVALID\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-417">1805 (0x70d)</span><span class="sxs-lookup"><span data-stu-id="c7755-417">1805 (0x70D)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-418">Die angegebene Umgebung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-418">The environment specified is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S \_ keine \_ \_ Bindungen**</span><span class="sxs-lookup"><span data-stu-id="c7755-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC\_S\_NO\_MORE\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-420">1806 (0x70e)</span><span class="sxs-lookup"><span data-stu-id="c7755-420">1806 (0x70E)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-421">Es sind keine weiteren Bindungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-421">There are no more bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**Fehler \_ nologon- \_ Domänen \_ Vertrauensstellungs \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="c7755-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR\_NOLOGON\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-423">1807 (0x70f)</span><span class="sxs-lookup"><span data-stu-id="c7755-423">1807 (0x70F)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-424">Das verwendete Konto ist ein Domänen Vertrauensstellungs Konto.</span><span class="sxs-lookup"><span data-stu-id="c7755-424">The account used is an interdomain trust account.</span></span> <span data-ttu-id="c7755-425">Verwenden Sie Ihr globales Benutzerkonto oder lokales Benutzerkonto, um auf diesen Server zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c7755-425">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**Fehler \_ nologon \_ - \_ Vertrauensstellungs \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="c7755-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR\_NOLOGON\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-427">1808 (0x710)</span><span class="sxs-lookup"><span data-stu-id="c7755-427">1808 (0x710)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-428">Das verwendete Konto ist ein Computer Konto.</span><span class="sxs-lookup"><span data-stu-id="c7755-428">The account used is a computer account.</span></span> <span data-ttu-id="c7755-429">Verwenden Sie Ihr globales Benutzerkonto oder lokales Benutzerkonto, um auf diesen Server zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c7755-429">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**Fehler \_ nologon \_ Server \_ Vertrauensstellungs \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="c7755-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR\_NOLOGON\_SERVER\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-431">1809 (0x711)</span><span class="sxs-lookup"><span data-stu-id="c7755-431">1809 (0x711)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-432">Das verwendete Konto ist ein Server Vertrauensstellungs Konto.</span><span class="sxs-lookup"><span data-stu-id="c7755-432">The account used is a server trust account.</span></span> <span data-ttu-id="c7755-433">Verwenden Sie Ihr globales Benutzerkonto oder lokales Benutzerkonto, um auf diesen Server zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c7755-433">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**Fehler \_ Domänen \_ Vertrauensstellung \_ inkonsistent**</span><span class="sxs-lookup"><span data-stu-id="c7755-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR\_DOMAIN\_TRUST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-435">1810 (0x712)</span><span class="sxs-lookup"><span data-stu-id="c7755-435">1810 (0x712)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-436">Der Name oder die Sicherheits-ID (SID) der angegebenen Domäne ist mit den Vertrauensstellungs Informationen für diese Domäne nicht konsistent.</span><span class="sxs-lookup"><span data-stu-id="c7755-436">The name or security ID (SID) of the domain specified is inconsistent with the trust information for that domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**Fehler \_ Server \_ hat \_ geöffnete \_ Handles**</span><span class="sxs-lookup"><span data-stu-id="c7755-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERROR\_SERVER\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-438">1811 (0x713)</span><span class="sxs-lookup"><span data-stu-id="c7755-438">1811 (0x713)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-439">Der Server wird verwendet und kann nicht entladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-439">The server is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**Fehler \_ Ressourcen \_ Daten \_ \_ wurden nicht gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**ERROR\_RESOURCE\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-441">1812 (0x714)</span><span class="sxs-lookup"><span data-stu-id="c7755-441">1812 (0x714)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-442">Die angegebene Bilddatei enthielt keinen Ressourcenabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c7755-442">The specified image file did not contain a resource section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**Fehler \_ beim \_ Ressourcentyp \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**ERROR\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-444">1813 (0x715)</span><span class="sxs-lookup"><span data-stu-id="c7755-444">1813 (0x715)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-445">Der angegebene Ressourcentyp wurde in der Bilddatei nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-445">The specified resource type cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**der Fehler \_ Ressourcen \_ Name wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR\_RESOURCE\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-447">1814 (0x716)</span><span class="sxs-lookup"><span data-stu-id="c7755-447">1814 (0x716)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-448">Der angegebene Ressourcen Name wurde in der Bilddatei nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-448">The specified resource name cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**Fehler \_ Ressource \_ lang \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="c7755-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR\_RESOURCE\_LANG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-450">1815 (0x717)</span><span class="sxs-lookup"><span data-stu-id="c7755-450">1815 (0x717)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-451">Die angegebene Ressourcen Sprachen-ID wurde in der Bilddatei nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-451">The specified resource language ID cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**Fehler bei \_ nicht \_ ausreichendem \_ Kontingent.**</span><span class="sxs-lookup"><span data-stu-id="c7755-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR\_NOT\_ENOUGH\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-453">1816 (0x718)</span><span class="sxs-lookup"><span data-stu-id="c7755-453">1816 (0x718)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-454">Das Kontingent reicht für die Verarbeitung dieses Befehls nicht aus.</span><span class="sxs-lookup"><span data-stu-id="c7755-454">Not enough quota is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ keine \_ Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="c7755-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC\_S\_NO\_INTERFACES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-456">1817 (0x719)</span><span class="sxs-lookup"><span data-stu-id="c7755-456">1817 (0x719)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-457">Es wurden keine Schnittstellen registriert.</span><span class="sxs-lookup"><span data-stu-id="c7755-457">No interfaces have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC \_ S- \_ Aufruf \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="c7755-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC\_S\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-459">1818 (0x71a)</span><span class="sxs-lookup"><span data-stu-id="c7755-459">1818 (0x71A)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-460">Der Remote Prozedur Aufrufvorgang wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c7755-460">The remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC \_ S- \_ Bindung \_ unvollständig**</span><span class="sxs-lookup"><span data-stu-id="c7755-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC\_S\_BINDING\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-462">1819 (0x71b)</span><span class="sxs-lookup"><span data-stu-id="c7755-462">1819 (0x71B)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-463">Das Bindungs Handle enthält nicht alle erforderlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="c7755-463">The binding handle does not contain all required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC- \_ S- \_ comm- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC\_S\_COMM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-465">1820 (0x71c)</span><span class="sxs-lookup"><span data-stu-id="c7755-465">1820 (0x71C)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-466">Während eines Remote Prozedur Aufrufes ist ein Kommunikationsfehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c7755-466">A communications failure occurred during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**\_ \_ nicht unterstützte \_ authn- \_ Ebene für RPC S**</span><span class="sxs-lookup"><span data-stu-id="c7755-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC\_S\_UNSUPPORTED\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-468">1821 (0x71d)</span><span class="sxs-lookup"><span data-stu-id="c7755-468">1821 (0x71D)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-469">Die angeforderte Authentifizierungs Ebene wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-469">The requested authentication level is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S \_ kein \_ princ- \_ Name**</span><span class="sxs-lookup"><span data-stu-id="c7755-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC\_S\_NO\_PRINC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-471">1822 (0x71e)</span><span class="sxs-lookup"><span data-stu-id="c7755-471">1822 (0x71E)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-472">Es ist kein Prinzipal Name registriert.</span><span class="sxs-lookup"><span data-stu-id="c7755-472">No principal name registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ - \_ \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC\_S\_NOT\_RPC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-474">1823 (0x71f)</span><span class="sxs-lookup"><span data-stu-id="c7755-474">1823 (0x71F)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-475">Der angegebene Fehler ist kein gültiger Windows-RPC-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c7755-475">The error specified is not a valid Windows RPC error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC \_ S \_ UUID \_ lokal \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC\_S\_UUID\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-477">1824 (0x720)</span><span class="sxs-lookup"><span data-stu-id="c7755-477">1824 (0x720)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-478">Eine UUID, die nur auf diesem Computer gültig ist, wurde zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c7755-478">A UUID that is valid only on this computer has been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC \_ S S- \_ \_ pkg- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC\_S\_SEC\_PKG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-480">1825 (0x721)</span><span class="sxs-lookup"><span data-stu-id="c7755-480">1825 (0x721)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-481">Ein Sicherheitspaket spezifischer Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c7755-481">A security package specific error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC- \_ S \_ nicht \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="c7755-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC\_S\_NOT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-483">1826 (0x722)</span><span class="sxs-lookup"><span data-stu-id="c7755-483">1826 (0x722)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-484">Der Thread wird nicht abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c7755-484">Thread is not canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ungültige RPC X- \_ \_ \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="c7755-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC\_X\_INVALID\_ES\_ACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-486">1827 (0x723)</span><span class="sxs-lookup"><span data-stu-id="c7755-486">1827 (0x723)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-487">Ungültiger Vorgang für das Codierungs-/decodierungshandle.</span><span class="sxs-lookup"><span data-stu-id="c7755-487">Invalid operation on the encoding/decoding handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ falsche \_ es- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="c7755-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC\_X\_WRONG\_ES\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-489">1828 (0x724)</span><span class="sxs-lookup"><span data-stu-id="c7755-489">1828 (0x724)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-490">Nicht kompatible Version des serialisierungspakets.</span><span class="sxs-lookup"><span data-stu-id="c7755-490">Incompatible version of the serializing package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_falsche RPC X- \_ \_ Stub- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="c7755-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC\_X\_WRONG\_STUB\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-492">1829 (0x725)</span><span class="sxs-lookup"><span data-stu-id="c7755-492">1829 (0x725)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-493">Inkompatible Version des RPC-Stubs.</span><span class="sxs-lookup"><span data-stu-id="c7755-493">Incompatible version of the RPC stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**\_Ungültiges RPC X- \_ Pipe- \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="c7755-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC\_X\_INVALID\_PIPE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-495">1830 (0x726)</span><span class="sxs-lookup"><span data-stu-id="c7755-495">1830 (0x726)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-496">Das RPC-Pipe-Objekt ist ungültig oder beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c7755-496">The RPC pipe object is invalid or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC \_ X \_ falsche \_ Pipe- \_ Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="c7755-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC\_X\_WRONG\_PIPE\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-498">1831 (0x727)</span><span class="sxs-lookup"><span data-stu-id="c7755-498">1831 (0x727)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-499">Es wurde versucht, für ein RPC-Pipeobjekt einen ungültigen Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c7755-499">An invalid operation was attempted on an RPC pipe object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC \_ X \_ falsche \_ Pipe- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="c7755-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC\_X\_WRONG\_PIPE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-501">1832 (0x728)</span><span class="sxs-lookup"><span data-stu-id="c7755-501">1832 (0x728)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-502">Nicht unterstützte RPC-Pipe-Version.</span><span class="sxs-lookup"><span data-stu-id="c7755-502">Unsupported RPC pipe version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**Fehler bei RPC-e-Cookie-Authentifizierung \_ \_ \_ . \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC\_S\_COOKIE\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-504">1833 (0x729)</span><span class="sxs-lookup"><span data-stu-id="c7755-504">1833 (0x729)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-505">Der HTTP-Proxy Server hat die Verbindung abgelehnt, weil die Cookie-Authentifizierung fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="c7755-505">HTTP proxy server rejected the connection because the cookie authentication failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**das RPC \_ S- \_ Gruppenmitglied wurde \_ \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**RPC\_S\_GROUP\_MEMBER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-507">1898 (0x76a)</span><span class="sxs-lookup"><span data-stu-id="c7755-507">1898 (0x76A)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-508">Das Gruppenmitglied wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-508">The group member was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ nicht \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="c7755-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT\_S\_CANT\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-510">1899 (0x76b)</span><span class="sxs-lookup"><span data-stu-id="c7755-510">1899 (0x76B)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-511">Der Endpunkt Mapper-Datenbankeintrag konnte nicht erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-511">The endpoint mapper database entry could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_Ungültiges RPC S- \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="c7755-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC\_S\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-513">1900 (0x76c)</span><span class="sxs-lookup"><span data-stu-id="c7755-513">1900 (0x76C)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-514">Der Universal Unique Identifier (UUID) des Objekts ist die Nil-UUID.</span><span class="sxs-lookup"><span data-stu-id="c7755-514">The object universal unique identifier (UUID) is the nil UUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**\_ungültige \_ Zeit**</span><span class="sxs-lookup"><span data-stu-id="c7755-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-516">1901 (0x76d)</span><span class="sxs-lookup"><span data-stu-id="c7755-516">1901 (0x76D)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-517">Die angegebene Zeit ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-517">The specified time is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**\_ungültiger \_ Formular \_ Name.**</span><span class="sxs-lookup"><span data-stu-id="c7755-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR\_INVALID\_FORM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-519">1902 (0x76e)</span><span class="sxs-lookup"><span data-stu-id="c7755-519">1902 (0x76E)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-520">Der angegebene Formular Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-520">The specified form name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**Fehler bei \_ ungültiger \_ Formular \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="c7755-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR\_INVALID\_FORM\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-522">1903 (0x76f)</span><span class="sxs-lookup"><span data-stu-id="c7755-522">1903 (0x76F)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-523">Die angegebene Formular Größe ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-523">The specified form size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**Fehler \_ beim \_ warten bereits**</span><span class="sxs-lookup"><span data-stu-id="c7755-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR\_ALREADY\_WAITING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-525">1904 (0x770)</span><span class="sxs-lookup"><span data-stu-id="c7755-525">1904 (0x770)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-526">Auf das angegebene Drucker Handle wird bereits gewartet.</span><span class="sxs-lookup"><span data-stu-id="c7755-526">The specified printer handle is already being waited on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**Fehler \_ Drucker \_ gelöscht**</span><span class="sxs-lookup"><span data-stu-id="c7755-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR\_PRINTER\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-528">1905 (0x771)</span><span class="sxs-lookup"><span data-stu-id="c7755-528">1905 (0x771)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-529">Der angegebene Drucker wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c7755-529">The specified printer has been deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**Fehler \_ beim \_ Drucker \_ Zustand.**</span><span class="sxs-lookup"><span data-stu-id="c7755-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR\_INVALID\_PRINTER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-531">1906 (0x772)</span><span class="sxs-lookup"><span data-stu-id="c7755-531">1906 (0x772)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-532">Der Drucker Zustand ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-532">The state of the printer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**Fehler \_ Kennwort \_ muss \_ geändert werden**</span><span class="sxs-lookup"><span data-stu-id="c7755-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR\_PASSWORD\_MUST\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-534">1907 (0x773)</span><span class="sxs-lookup"><span data-stu-id="c7755-534">1907 (0x773)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-535">Das Kennwort des Benutzers muss vor der Anmeldung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-535">The user's password must be changed before signing in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**Fehler \_ Domänen \_ Controller \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="c7755-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERROR\_DOMAIN\_CONTROLLER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-537">1908 (0x774)</span><span class="sxs-lookup"><span data-stu-id="c7755-537">1908 (0x774)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-538">Der Domänen Controller für diese Domäne konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-538">Could not find the domain controller for this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**Fehler \_ Konto \_ gesperrt \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**ERROR\_ACCOUNT\_LOCKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-540">1909 (0x775)</span><span class="sxs-lookup"><span data-stu-id="c7755-540">1909 (0x775)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-541">Das Konto, auf das verwiesen wird, ist zurzeit gesperrt und darf nicht bei angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="c7755-541">The referenced account is currently locked out and may not be logged on to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**oder \_ ungültiges \_ oxid**</span><span class="sxs-lookup"><span data-stu-id="c7755-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OR\_INVALID\_OXID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-543">1910 (0x776)</span><span class="sxs-lookup"><span data-stu-id="c7755-543">1910 (0x776)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-544">Das angegebene Objekt Exportprogramm wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-544">The object exporter specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**oder \_ ungültige \_ OID.**</span><span class="sxs-lookup"><span data-stu-id="c7755-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OR\_INVALID\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-546">1911 (0x777)</span><span class="sxs-lookup"><span data-stu-id="c7755-546">1911 (0x777)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-547">Das angegebene Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-547">The object specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**oder \_ ungültiger \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="c7755-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OR\_INVALID\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-549">1912 (0x778)</span><span class="sxs-lookup"><span data-stu-id="c7755-549">1912 (0x778)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-550">Der angegebene objektresolersatz wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-550">The object resolver set specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC- \_ e- \_ Sendevorgang \_ unvollständig**</span><span class="sxs-lookup"><span data-stu-id="c7755-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC\_S\_SEND\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-552">1913 (0x779)</span><span class="sxs-lookup"><span data-stu-id="c7755-552">1913 (0x779)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-553">Einige Daten werden weiterhin im Anforderungs Puffer gesendet.</span><span class="sxs-lookup"><span data-stu-id="c7755-553">Some data remains to be sent in the request buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**Ungültiges asynchrones Handle für RPC \_ S \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC\_S\_INVALID\_ASYNC\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-555">1914 (0x77a)</span><span class="sxs-lookup"><span data-stu-id="c7755-555">1914 (0x77A)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-556">Ungültiges asynchrones Remote Prozedur-Rückruf handle.</span><span class="sxs-lookup"><span data-stu-id="c7755-556">Invalid asynchronous remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_Ungültiger asynchroner \_ \_ \_ Aufruf von RPC S**</span><span class="sxs-lookup"><span data-stu-id="c7755-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC\_S\_INVALID\_ASYNC\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-558">1915 (0x77b)</span><span class="sxs-lookup"><span data-stu-id="c7755-558">1915 (0x77B)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-559">Ungültiges asynchrones RPC-Aufruf Handle für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c7755-559">Invalid asynchronous RPC call handle for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC- \_ X- \_ Pipe \_ geschlossen**</span><span class="sxs-lookup"><span data-stu-id="c7755-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC\_X\_PIPE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-561">1916 (0x77c)</span><span class="sxs-lookup"><span data-stu-id="c7755-561">1916 (0x77C)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-562">Das RPC-Pipe-Objekt wurde bereits geschlossen.</span><span class="sxs-lookup"><span data-stu-id="c7755-562">The RPC pipe object has already been closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC \_ X \_ Pipe- \_ Disziplin- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC\_X\_PIPE\_DISCIPLINE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-564">1917 (0x77d)</span><span class="sxs-lookup"><span data-stu-id="c7755-564">1917 (0x77D)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-565">Der RPC-Aufruf wurde abgeschlossen, bevor alle Pipes verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="c7755-565">The RPC call completed before all pipes were processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC- \_ X- \_ Pipe \_ leer**</span><span class="sxs-lookup"><span data-stu-id="c7755-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC\_X\_PIPE\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-567">1918 (0x77e)</span><span class="sxs-lookup"><span data-stu-id="c7755-567">1918 (0x77E)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-568">Von der RPC-Pipe sind keine weiteren Daten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7755-568">No more data is available from the RPC pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**Fehler " \_ kein \_ Sitename"**</span><span class="sxs-lookup"><span data-stu-id="c7755-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR\_NO\_SITENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-570">1919 (0x77f)</span><span class="sxs-lookup"><span data-stu-id="c7755-570">1919 (0x77F)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-571">Für diesen Computer ist kein Website Name verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7755-571">No site name is available for this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**Fehler beim Zugriff auf die \_ \_ \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="c7755-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR\_CANT\_ACCESS\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-573">1920 (0x780)</span><span class="sxs-lookup"><span data-stu-id="c7755-573">1920 (0x780)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-574">Auf die Datei kann nicht vom System zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-574">The file cannot be accessed by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**Fehler \_ beim \_ Auflösen des \_ Datei namens.**</span><span class="sxs-lookup"><span data-stu-id="c7755-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR\_CANT\_RESOLVE\_FILENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-576">1921 (0x781)</span><span class="sxs-lookup"><span data-stu-id="c7755-576">1921 (0x781)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-577">Der Name der Datei kann nicht vom System aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-577">The name of the file cannot be resolved by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**nicht übereinstimmender RPC \_ S- \_ \_ Eintragstyp \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC\_S\_ENTRY\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-579">1922 (0x782)</span><span class="sxs-lookup"><span data-stu-id="c7755-579">1922 (0x782)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-580">Der Eintrag weist nicht den erwarteten Typ auf.</span><span class="sxs-lookup"><span data-stu-id="c7755-580">The entry is not of the expected type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ nicht \_ alle \_ OBJS- \_ exportierten**</span><span class="sxs-lookup"><span data-stu-id="c7755-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-582">1923 (0x783)</span><span class="sxs-lookup"><span data-stu-id="c7755-582">1923 (0x783)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-583">Nicht alle Objekt-UUIDs konnten in den angegebenen Eintrag exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-583">Not all object UUIDs could be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC \_ S- \_ Schnittstelle \_ nicht \_ exportiert**</span><span class="sxs-lookup"><span data-stu-id="c7755-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC\_S\_INTERFACE\_NOT\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-585">1924 (0x784)</span><span class="sxs-lookup"><span data-stu-id="c7755-585">1924 (0x784)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-586">Die Schnittstelle konnte nicht in den angegebenen Eintrag exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-586">Interface could not be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC- \_ S- \_ Profil \_ nicht \_ hinzugefügt**</span><span class="sxs-lookup"><span data-stu-id="c7755-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC\_S\_PROFILE\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-588">1925 (0x785)</span><span class="sxs-lookup"><span data-stu-id="c7755-588">1925 (0x785)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-589">Der angegebene Profil Eintrag konnte nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-589">The specified profile entry could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ PRF \_ ELT wurde \_ nicht \_ hinzugefügt.**</span><span class="sxs-lookup"><span data-stu-id="c7755-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC\_S\_PRF\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-591">1926 (0x786)</span><span class="sxs-lookup"><span data-stu-id="c7755-591">1926 (0x786)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-592">Das angegebene Profil Element konnte nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-592">The specified profile element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ PRF \_ ELT \_ nicht \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="c7755-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC\_S\_PRF\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-594">1927 (0x787)</span><span class="sxs-lookup"><span data-stu-id="c7755-594">1927 (0x787)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-595">Das angegebene Profil Element konnte nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-595">The specified profile element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC- \_ e- \_ GRP wird \_ \_ nicht \_ hinzugefügt.**</span><span class="sxs-lookup"><span data-stu-id="c7755-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC\_S\_GRP\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-597">1928 (0x788)</span><span class="sxs-lookup"><span data-stu-id="c7755-597">1928 (0x788)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-598">Das Gruppenelement konnte nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-598">The group element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC- \_ S \_ GRP \_ ELT \_ nicht \_ entfernt**</span><span class="sxs-lookup"><span data-stu-id="c7755-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC\_S\_GRP\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-600">1929 (0x789)</span><span class="sxs-lookup"><span data-stu-id="c7755-600">1929 (0x789)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-601">Das Gruppenelement konnte nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-601">The group element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**Fehler- \_ km- \_ Treiber \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="c7755-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR\_KM\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-603">1930 (0x78a)</span><span class="sxs-lookup"><span data-stu-id="c7755-603">1930 (0x78A)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-604">Der Druckertreiber ist nicht kompatibel mit einer Richtlinie, die auf Ihrem Computer aktiviert ist und NT 4,0-Treiber blockiert.</span><span class="sxs-lookup"><span data-stu-id="c7755-604">The printer driver is not compatible with a policy enabled on your computer that blocks NT 4.0 drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**Fehler \_ Kontext ist \_ abgelaufen.**</span><span class="sxs-lookup"><span data-stu-id="c7755-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**ERROR\_CONTEXT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-606">1931 (0x78b)</span><span class="sxs-lookup"><span data-stu-id="c7755-606">1931 (0x78B)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-607">Der Kontext ist abgelaufen und kann nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-607">The context has expired and can no longer be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**Fehler \_ pro \_ Benutzer \_ Vertrauensstellungs \_ Kontingent \_ überschritten**</span><span class="sxs-lookup"><span data-stu-id="c7755-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR\_PER\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-609">1932 (0x78c)</span><span class="sxs-lookup"><span data-stu-id="c7755-609">1932 (0x78C)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-610">Das Kontingent für die Delegierte Vertrauensstellung des aktuellen Benutzers wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="c7755-610">The current user's delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**Fehler \_ alle \_ Benutzer \_ Vertrauensstellungs \_ Kontingente \_ überschritten.**</span><span class="sxs-lookup"><span data-stu-id="c7755-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR\_ALL\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-612">1933 (0x78d)</span><span class="sxs-lookup"><span data-stu-id="c7755-612">1933 (0x78D)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-613">Das Kontingent für die Gesamt Erstellung Delegierter Vertrauens Stellungen wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="c7755-613">The total delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**Fehler \_ beim \_ Löschen der \_ Vertrauens \_ Quote \_ für den Benutzer.**</span><span class="sxs-lookup"><span data-stu-id="c7755-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR\_USER\_DELETE\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-615">1934 (0x78e)</span><span class="sxs-lookup"><span data-stu-id="c7755-615">1934 (0x78E)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-616">Das Kontingent für den Delegierten Vertrauens Löschvorgang des aktuellen Benutzers wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="c7755-616">The current user's delegated trust deletion quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**Fehler bei der \_ \_ firewallfirewall. \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR\_AUTHENTICATION\_FIREWALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-618">1935 (0x78f)</span><span class="sxs-lookup"><span data-stu-id="c7755-618">1935 (0x78F)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-619">Der Computer, bei dem Sie sich anmelden, wird durch eine Authentifizierungs Firewall geschützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-619">The computer you are signing into is protected by an authentication firewall.</span></span> <span data-ttu-id="c7755-620">Das angegebene Konto darf sich nicht bei dem Computer authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="c7755-620">The specified account is not allowed to authenticate to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**Fehler beim \_ Blockieren von Remote \_ Druck \_ Verbindungen \_ .**</span><span class="sxs-lookup"><span data-stu-id="c7755-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR\_REMOTE\_PRINT\_CONNECTIONS\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-622">1936 (0x790)</span><span class="sxs-lookup"><span data-stu-id="c7755-622">1936 (0x790)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-623">Remote Verbindungen mit dem Druck Spooler werden durch eine auf Ihrem Computer festgelegte Richtlinie blockiert.</span><span class="sxs-lookup"><span data-stu-id="c7755-623">Remote connections to the Print Spooler are blocked by a policy set on your machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**Fehler \_ NTLM \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="c7755-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR\_NTLM\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-625">1937 (0x791)</span><span class="sxs-lookup"><span data-stu-id="c7755-625">1937 (0x791)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-626">Die Authentifizierung ist fehlgeschlagen, weil die NTLM-Authentifizierung deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="c7755-626">Authentication failed because NTLM authentication has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**Fehler \_ Kennwort- \_ Änderung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c7755-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR\_PASSWORD\_CHANGE\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-628">1938 (0x792)</span><span class="sxs-lookup"><span data-stu-id="c7755-628">1938 (0x792)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-629">Anmeldefehler: Die EAS-Richtlinie erfordert, dass der Benutzer sein Kennwort ändert, bevor dieser Vorgang ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7755-629">Logon Failure: EAS policy requires that the user change their password before this operation can be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**Fehler \_ ungültiges \_ Pixel \_ Format.**</span><span class="sxs-lookup"><span data-stu-id="c7755-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR\_INVALID\_PIXEL\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-631">2000 (0x7d0)</span><span class="sxs-lookup"><span data-stu-id="c7755-631">2000 (0x7D0)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-632">Das Pixel Format ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-632">The pixel format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**fehlerhafter \_ \_ Treiber Fehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR\_BAD\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-634">2001 (0x7d1)</span><span class="sxs-lookup"><span data-stu-id="c7755-634">2001 (0x7D1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-635">Der angegebene Treiber ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-635">The specified driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**Fehler bei \_ ungültigem \_ Fenster \_ Stil.**</span><span class="sxs-lookup"><span data-stu-id="c7755-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR\_INVALID\_WINDOW\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-637">2002 (0x7d2)</span><span class="sxs-lookup"><span data-stu-id="c7755-637">2002 (0x7D2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-638">Der Fenster Stil oder das Klassen Attribut ist für diesen Vorgang ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-638">The window style or class attribute is invalid for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**\_fehlermetadatendatei \_ \_ wird nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="c7755-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR\_METAFILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-640">2003 (0x7d3)</span><span class="sxs-lookup"><span data-stu-id="c7755-640">2003 (0x7D3)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-641">Der angeforderte Metadatei-Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-641">The requested metafile operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**Fehler \_ Transformation \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="c7755-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**ERROR\_TRANSFORM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-643">2004 (0x7d4)</span><span class="sxs-lookup"><span data-stu-id="c7755-643">2004 (0x7D4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-644">Der angeforderte Transformations Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-644">The requested transformation operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**Fehler \_ Clipping \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="c7755-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**ERROR\_CLIPPING\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-646">2005 (0x7d5)</span><span class="sxs-lookup"><span data-stu-id="c7755-646">2005 (0x7D5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-647">Der angeforderte Clippingvorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7755-647">The requested clipping operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**\_ungültiger \_ CMM-Fehler.**</span><span class="sxs-lookup"><span data-stu-id="c7755-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR\_INVALID\_CMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-649">2010 (0x7da)</span><span class="sxs-lookup"><span data-stu-id="c7755-649">2010 (0x7DA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-650">Das angegebene Farb Verwaltungsmodul ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-650">The specified color management module is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**Fehler \_ ungültiges \_ Profil.**</span><span class="sxs-lookup"><span data-stu-id="c7755-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR\_INVALID\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-652">2011 (0x7db)</span><span class="sxs-lookup"><span data-stu-id="c7755-652">2011 (0x7DB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-653">Das angegebene Farbprofil ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-653">The specified color profile is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_Fehlertag \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**ERROR\_TAG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-655">2012 (0x7dc)</span><span class="sxs-lookup"><span data-stu-id="c7755-655">2012 (0x7DC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-656">Das angegebene Tag wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-656">The specified tag was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**\_Fehlertag \_ nicht \_ vorhanden**</span><span class="sxs-lookup"><span data-stu-id="c7755-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ERROR\_TAG\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-658">2013 (0x7dd)</span><span class="sxs-lookup"><span data-stu-id="c7755-658">2013 (0x7DD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-659">Ein erforderliches Tag ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-659">A required tag is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**Fehler \_ doppeltes \_ Tag**</span><span class="sxs-lookup"><span data-stu-id="c7755-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR\_DUPLICATE\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-661">2014 (0x7de)</span><span class="sxs-lookup"><span data-stu-id="c7755-661">2014 (0x7DE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-662">Das angegebene Tag ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-662">The specified tag is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**das Fehler \_ Profil ist \_ nicht \_ \_ mit dem \_ Gerät verknüpft.**</span><span class="sxs-lookup"><span data-stu-id="c7755-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-664">2015 (0x7df)</span><span class="sxs-lookup"><span data-stu-id="c7755-664">2015 (0x7DF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-665">Das angegebene Farbprofil ist dem angegebenen Gerät nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c7755-665">The specified color profile is not associated with the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**Fehler \_ Profil wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**ERROR\_PROFILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-667">2016 (0x7e0)</span><span class="sxs-lookup"><span data-stu-id="c7755-667">2016 (0x7E0)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-668">Das angegebene Farbprofil wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-668">The specified color profile was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**\_ungültiger \_ colorspace-Fehler.**</span><span class="sxs-lookup"><span data-stu-id="c7755-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR\_INVALID\_COLORSPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-670">2017 (0x7e1)</span><span class="sxs-lookup"><span data-stu-id="c7755-670">2017 (0x7E1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-671">Der angegebene Farbraum ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-671">The specified color space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ICM-Fehler ist \_ \_ nicht \_ aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="c7755-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR\_ICM\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-673">2018 (0x7e2)</span><span class="sxs-lookup"><span data-stu-id="c7755-673">2018 (0x7E2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-674">Die Bild Farbverwaltung ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c7755-674">Image Color Management is not enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**Fehler beim \_ Löschen von \_ ICM \_ XForm.**</span><span class="sxs-lookup"><span data-stu-id="c7755-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR\_DELETING\_ICM\_XFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-676">2019 (0x7e3)</span><span class="sxs-lookup"><span data-stu-id="c7755-676">2019 (0x7E3)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-677">Beim Löschen der Farb Transformation ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c7755-677">There was an error while deleting the color transform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**Fehler \_ ungültige \_ Transformation**</span><span class="sxs-lookup"><span data-stu-id="c7755-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR\_INVALID\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-679">2020 (0x7e4)</span><span class="sxs-lookup"><span data-stu-id="c7755-679">2020 (0x7E4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-680">Die angegebene Farb Transformation ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-680">The specified color transform is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**Fehler bei colorspace-Konflikt. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR\_COLORSPACE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-682">2021 (0x7e5)</span><span class="sxs-lookup"><span data-stu-id="c7755-682">2021 (0x7E5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-683">Die angegebene Transformation entspricht nicht dem Farbraum der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="c7755-683">The specified transform does not match the bitmap's color space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**Fehler \_ ungültiger \_ ColorIndex.**</span><span class="sxs-lookup"><span data-stu-id="c7755-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR\_INVALID\_COLORINDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-685">2022 (0x7e6)</span><span class="sxs-lookup"><span data-stu-id="c7755-685">2022 (0x7E6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-686">Der angegebene benannte Farb Index ist nicht im Profil vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-686">The specified named color index is not present in the profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**Fehler \_ Profil \_ entspricht \_ \_ Gerät nicht \_**</span><span class="sxs-lookup"><span data-stu-id="c7755-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**ERROR\_PROFILE\_DOES\_NOT\_MATCH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-688">2023 (0x7e7)</span><span class="sxs-lookup"><span data-stu-id="c7755-688">2023 (0x7E7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-689">Das angegebene Profil ist für ein Gerät mit einem anderen Typ als dem angegebenen Gerät vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c7755-689">The specified profile is intended for a device of a different type than the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**Fehler beim \_ verbundenen \_ anderen \_ Kennwort**</span><span class="sxs-lookup"><span data-stu-id="c7755-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-691">2108 (0x83c)</span><span class="sxs-lookup"><span data-stu-id="c7755-691">2108 (0x83C)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-692">Die Netzwerkverbindung wurde erfolgreich hergestellt, aber der Benutzer musste aufgefordert werden, ein anderes Kennwort als das ursprünglich angegebene Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="c7755-692">The network connection was made successfully, but the user had to be prompted for a password other than the one originally specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**Fehler beim \_ verbundenen \_ anderen \_ Kennwort- \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="c7755-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-694">2109 (0x83d)</span><span class="sxs-lookup"><span data-stu-id="c7755-694">2109 (0x83D)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-695">Die Netzwerkverbindung wurde mithilfe der Standard Anmelde Informationen erfolgreich hergestellt.</span><span class="sxs-lookup"><span data-stu-id="c7755-695">The network connection was made successfully using default credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**Ungültiger \_ \_ Benutzername**</span><span class="sxs-lookup"><span data-stu-id="c7755-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR\_BAD\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-697">2202 (0x89a)</span><span class="sxs-lookup"><span data-stu-id="c7755-697">2202 (0x89A)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-698">Der angegebene Benutzername ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c7755-698">The specified username is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**Fehler \_ nicht \_ verbunden**</span><span class="sxs-lookup"><span data-stu-id="c7755-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-700">2250 (0x8ca)</span><span class="sxs-lookup"><span data-stu-id="c7755-700">2250 (0x8CA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-701">Diese Netzwerkverbindung ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-701">This network connection does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**Fehler beim \_ Öffnen von \_ Dateien**</span><span class="sxs-lookup"><span data-stu-id="c7755-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-703">2401 (0x961)</span><span class="sxs-lookup"><span data-stu-id="c7755-703">2401 (0x961)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-704">Für diese Netzwerkverbindung sind Dateien geöffnet oder ausstehende Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="c7755-704">This network connection has files open or requests pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**\_aktive \_ Verbindungsfehler**</span><span class="sxs-lookup"><span data-stu-id="c7755-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR\_ACTIVE\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-706">2402 (0x962)</span><span class="sxs-lookup"><span data-stu-id="c7755-706">2402 (0x962)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-707">Aktive Verbindungen sind immer noch vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7755-707">Active connections still exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_fehlergerät \_ wird \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="c7755-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR\_DEVICE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-709">2404 (0x964)</span><span class="sxs-lookup"><span data-stu-id="c7755-709">2404 (0x964)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-710">Das Gerät wird von einem aktiven Prozess verwendet und kann nicht getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-710">The device is in use by an active process and cannot be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**\_unbekannter Fehler \_ \_ Monitor.**</span><span class="sxs-lookup"><span data-stu-id="c7755-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR\_UNKNOWN\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-712">3000 (0xBB8)</span><span class="sxs-lookup"><span data-stu-id="c7755-712">3000 (0xBB8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-713">Der angegebene Druckmonitor ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c7755-713">The specified print monitor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**Fehler \_ Drucker \_ Treiber \_ wird \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="c7755-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR\_PRINTER\_DRIVER\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-715">3001 (0xbb9)</span><span class="sxs-lookup"><span data-stu-id="c7755-715">3001 (0xBB9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-716">Der angegebene Druckertreiber wird zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7755-716">The specified printer driver is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**Fehler \_ \_ Spooldatei \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR\_SPOOL\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-718">3002 (0xBBA)</span><span class="sxs-lookup"><span data-stu-id="c7755-718">3002 (0xBBA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-719">Die Spooldatei wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-719">The spool file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**Fehler \_ SPL \_ Nein \_ StartDoc**</span><span class="sxs-lookup"><span data-stu-id="c7755-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR\_SPL\_NO\_STARTDOC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-721">3003 (0xbbb)</span><span class="sxs-lookup"><span data-stu-id="c7755-721">3003 (0xBBB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-722">Es wurde kein StartDocPrinter-Befehl ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7755-722">A StartDocPrinter call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**Fehler- \_ SPL \_ Nein, \_ AddJob**</span><span class="sxs-lookup"><span data-stu-id="c7755-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR\_SPL\_NO\_ADDJOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-724">3004 (0xbbc)</span><span class="sxs-lookup"><span data-stu-id="c7755-724">3004 (0xBBC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-725">Es wurde kein AddJob-Befehl ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="c7755-725">An AddJob call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**der Fehler \_ Druck \_ Prozessor ist \_ bereits \_ installiert.**</span><span class="sxs-lookup"><span data-stu-id="c7755-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR\_PRINT\_PROCESSOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-727">3005 (0xbbd)</span><span class="sxs-lookup"><span data-stu-id="c7755-727">3005 (0xBBD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-728">Der angegebene Druck Prozessor wurde bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="c7755-728">The specified print processor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**der Fehler \_ Druck \_ Monitor ist \_ bereits \_ installiert.**</span><span class="sxs-lookup"><span data-stu-id="c7755-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR\_PRINT\_MONITOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-730">3006 (0xbbe)</span><span class="sxs-lookup"><span data-stu-id="c7755-730">3006 (0xBBE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-731">Der angegebene Druckmonitor wurde bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="c7755-731">The specified print monitor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**Fehler \_ beim \_ Druck \_ Monitor.**</span><span class="sxs-lookup"><span data-stu-id="c7755-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR\_INVALID\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-733">3007 (0xbbf)</span><span class="sxs-lookup"><span data-stu-id="c7755-733">3007 (0xBBF)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-734">Der angegebene Druckmonitor verfügt nicht über die erforderlichen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c7755-734">The specified print monitor does not have the required functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**Fehler \_ Druck \_ Monitor \_ wird \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="c7755-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR\_PRINT\_MONITOR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-736">3008 (0xbc0)</span><span class="sxs-lookup"><span data-stu-id="c7755-736">3008 (0xBC0)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-737">Der angegebene Druckmonitor wird zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7755-737">The specified print monitor is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**Fehler \_ Drucker \_ hat \_ Aufträge in \_ Warteschlange eingereiht**</span><span class="sxs-lookup"><span data-stu-id="c7755-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR\_PRINTER\_HAS\_JOBS\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-739">3009 (0xbc1)</span><span class="sxs-lookup"><span data-stu-id="c7755-739">3009 (0xBC1)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-740">Der angeforderte Vorgang ist nicht zulässig, wenn Aufträge in die Warteschlange eingereiht wurden.</span><span class="sxs-lookup"><span data-stu-id="c7755-740">The requested operation is not allowed when there are jobs queued to the printer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**Fehler \_ beim \_ Neustart \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="c7755-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR\_SUCCESS\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-742">3010 (0xbc2)</span><span class="sxs-lookup"><span data-stu-id="c7755-742">3010 (0xBC2)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-743">Der angeforderte Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c7755-743">The requested operation is successful.</span></span> <span data-ttu-id="c7755-744">Änderungen werden erst wirksam, wenn das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c7755-744">Changes will not be effective until the system is rebooted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**Fehler \_ beim \_ Neustart \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="c7755-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR\_SUCCESS\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-746">3011 (0xbc3)</span><span class="sxs-lookup"><span data-stu-id="c7755-746">3011 (0xBC3)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-747">Der angeforderte Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c7755-747">The requested operation is successful.</span></span> <span data-ttu-id="c7755-748">Änderungen werden erst wirksam, wenn der Dienst neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c7755-748">Changes will not be effective until the service is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**Fehler \_ Drucker wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERROR\_PRINTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-750">3012 (0xbc4)</span><span class="sxs-lookup"><span data-stu-id="c7755-750">3012 (0xBC4)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-751">Es wurden keine Drucker gefunden.</span><span class="sxs-lookup"><span data-stu-id="c7755-751">No printers were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**Fehler \_ Drucker \_ Treiber \_ gewarnt**</span><span class="sxs-lookup"><span data-stu-id="c7755-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR\_PRINTER\_DRIVER\_WARNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-753">3013 (0xbc5)</span><span class="sxs-lookup"><span data-stu-id="c7755-753">3013 (0xBC5)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-754">Der Druckertreiber ist bekanntermaßen unzuverlässig.</span><span class="sxs-lookup"><span data-stu-id="c7755-754">The printer driver is known to be unreliable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**Fehler \_ Drucker \_ Treiber \_ blockiert**</span><span class="sxs-lookup"><span data-stu-id="c7755-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR\_PRINTER\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-756">3014 (0xbc6)</span><span class="sxs-lookup"><span data-stu-id="c7755-756">3014 (0xBC6)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-757">Der Druckertreiber ist bekannt, dass er das System beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="c7755-757">The printer driver is known to harm the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**Fehler \_ Drucker- \_ Treiber \_ Paket wird \_ \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="c7755-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR\_PRINTER\_DRIVER\_PACKAGE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-759">3015 (0xbc7)</span><span class="sxs-lookup"><span data-stu-id="c7755-759">3015 (0xBC7)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-760">Das angegebene Druckertreiber Paket wird zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7755-760">The specified printer driver package is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**Fehler beim \_ Core- \_ Treiber \_ Paket \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="c7755-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR\_CORE\_DRIVER\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-762">3016 (0xbc8)</span><span class="sxs-lookup"><span data-stu-id="c7755-762">3016 (0xBC8)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-763">Es wurde kein Core-Treiber Paket gefunden, das für das Druckertreiber Paket erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c7755-763">Unable to find a core driver package that is required by the printer driver package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**Fehler \_ beim \_ Neustart \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="c7755-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR\_FAIL\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-765">3017 (0xbc9)</span><span class="sxs-lookup"><span data-stu-id="c7755-765">3017 (0xBC9)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-766">Der angeforderte Vorgang ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7755-766">The requested operation failed.</span></span> <span data-ttu-id="c7755-767">Ein Systemneustart ist erforderlich, um ein Rollback der vorgenommenen Änderungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c7755-767">A system reboot is required to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**Fehler \_ beim \_ Neustart \_ wurde initiiert.**</span><span class="sxs-lookup"><span data-stu-id="c7755-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR\_FAIL\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-769">3018 (0xbca)</span><span class="sxs-lookup"><span data-stu-id="c7755-769">3018 (0xBCA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-770">Der angeforderte Vorgang ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7755-770">The requested operation failed.</span></span> <span data-ttu-id="c7755-771">Ein Systemneustart wurde initiiert, um ein Rollback der vorgenommenen Änderungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c7755-771">A system reboot has been initiated to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**Fehler \_ Drucker- \_ Treiber \_ Download \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="c7755-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR\_PRINTER\_DRIVER\_DOWNLOAD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-773">3019 (0xbcb)</span><span class="sxs-lookup"><span data-stu-id="c7755-773">3019 (0xBCB)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-774">Der angegebene Druckertreiber wurde im System nicht gefunden und muss heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-774">The specified printer driver was not found on the system and needs to be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**Fehler \_ beim \_ Neustart des Auftrags \_ \_ erforderlich.**</span><span class="sxs-lookup"><span data-stu-id="c7755-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR\_PRINT\_JOB\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-776">3020 (0xbcc)</span><span class="sxs-lookup"><span data-stu-id="c7755-776">3020 (0xBCC)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-777">Fehler beim Drucken des angeforderten Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="c7755-777">The requested print job has failed to print.</span></span> <span data-ttu-id="c7755-778">Ein Drucksystem Update erfordert, dass der Auftrag erneut übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c7755-778">A print system update requires the job to be resubmitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**Fehler \_ beim \_ Drucker \_ Treiber \_ Manifest.**</span><span class="sxs-lookup"><span data-stu-id="c7755-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR\_INVALID\_PRINTER\_DRIVER\_MANIFEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-780">3021 (0xbcd)</span><span class="sxs-lookup"><span data-stu-id="c7755-780">3021 (0xBCD)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-781">Der Druckertreiber enthält kein gültiges Manifest oder enthält zu viele Manifeste.</span><span class="sxs-lookup"><span data-stu-id="c7755-781">The printer driver does not contain a valid manifest, or contains too many manifests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**Fehler \_ Drucker \_ nicht \_ share fähig**</span><span class="sxs-lookup"><span data-stu-id="c7755-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR\_PRINTER\_NOT\_SHAREABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-783">3022 (0xbce)</span><span class="sxs-lookup"><span data-stu-id="c7755-783">3022 (0xBCE)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-784">Der angegebene Drucker kann nicht freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7755-784">The specified printer cannot be shared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**Fehler \_ Anforderung \_ angehalten**</span><span class="sxs-lookup"><span data-stu-id="c7755-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**ERROR\_REQUEST\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-786">3050 (0xbea)</span><span class="sxs-lookup"><span data-stu-id="c7755-786">3050 (0xBEA)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-787">Der Vorgang wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="c7755-787">The operation was paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c7755-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**Fehler \_ - \_ e/a neu ausgestellt \_ als \_ zwischengespeichert**</span><span class="sxs-lookup"><span data-stu-id="c7755-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR\_IO\_REISSUE\_AS\_CACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7755-789">3950 (0xF 6E)</span><span class="sxs-lookup"><span data-stu-id="c7755-789">3950 (0xF6E)</span></span>
</dt> <dt>



<span data-ttu-id="c7755-790">Wiederholen Sie den angegebenen Vorgang als zwischengespeicherten e/a-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c7755-790">Reissue the given operation as a cached IO operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="c7755-791">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7755-791">Requirements</span></span>



| <span data-ttu-id="c7755-792">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7755-792">Requirement</span></span> | <span data-ttu-id="c7755-793">Wert</span><span class="sxs-lookup"><span data-stu-id="c7755-793">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7755-794">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7755-794">Minimum supported client</span></span><br/> | <span data-ttu-id="c7755-795">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7755-795">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c7755-796">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7755-796">Minimum supported server</span></span><br/> | <span data-ttu-id="c7755-797">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7755-797">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7755-798">Header</span><span class="sxs-lookup"><span data-stu-id="c7755-798">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7755-799"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7755-799"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7755-800">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7755-800">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7755-801">System Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="c7755-801">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




