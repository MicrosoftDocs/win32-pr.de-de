---
title: Implementieren der NAP-Unterstützung für EAP-Methoden
description: Erfahren Sie, wie Sie die NAP-Unterstützung für einen EAPHost-Supplicant implementieren. Weitere Informationen finden Sie unter EAPHost-bezogene NAP-Themen und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: c25e4f03-759a-47a7-8b35-bbe669501c5c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e5f0bc8900ee3d9cb01edb79b64b8ef5a68df4c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104039879"
---
# <a name="implementing-nap-support-for-eap-methods"></a><span data-ttu-id="76d93-104">Implementieren der NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="76d93-104">Implementing NAP Support for EAP Methods</span></span>

<span data-ttu-id="76d93-105">In diesem Thema wird erläutert, wie NAP für einen EAPHost-Supplicant implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="76d93-105">This topic explains how to implement NAP for an EAPHost supplicant.</span></span> <span data-ttu-id="76d93-106">In Windows Vista und Windows Server 2008 ist ein NAP-Erzwingungs Client (NAP EC) für authentifizierte [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Verbindungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76d93-106">In Windows Vista and Windows Server 2008 a NAP Enforcement Client (NAP EC) is available for [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authenticated connections.</span></span>

## <a name="implementing-network-access-protection-nap"></a><span data-ttu-id="76d93-107">Implementieren von Netzwerk Zugriffsschutz (Network Access Protection, NAP)</span><span class="sxs-lookup"><span data-stu-id="76d93-107">Implementing Network Access Protection (NAP)</span></span>

<span data-ttu-id="76d93-108">Zur Unterstützung von NAP implementiert ein EAPHost-Supplicant eine Rückruffunktion, die mit dem [**notificationhandler**](/previous-versions/windows/desktop/api) -Rückruf Prototyp übereinstimmt und einen Zeiger auf diese Rückruffunktion bereitstellen muss, wenn [**eaphostpeer erbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="76d93-108">To support NAP, an EAPHost supplicant implements a callback function matching the [**NotificationHandler**](/previous-versions/windows/desktop/api) callback prototype and must provide a pointer to this callback function when calling [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>

<span data-ttu-id="76d93-109">Die Rückruffunktion nimmt zwei Parameter an.</span><span class="sxs-lookup"><span data-stu-id="76d93-109">The callback function takes two parameters.</span></span>

-   <span data-ttu-id="76d93-110">Eine GUID, die die der Authentifizierung zugeordnete-Schnittstelle eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="76d93-110">A GUID that uniquely identifies the interface associated with the authentication.</span></span>
-   <span data-ttu-id="76d93-111">Ein void-Zeiger auf eine nicht transparente Datenstruktur, die vom Supplicant bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="76d93-111">A VOID pointer to an opaque data structure that is supplied by the supplicant.</span></span>

<span data-ttu-id="76d93-112">EAPHost Ruft die vom Supplicant bereitgestellte Rückruffunktion mit der eindeutigen Schnittstellen-GUID und dem void-Zeiger auf, wenn sich der Quarantäne Zustand des Computers ändert.</span><span class="sxs-lookup"><span data-stu-id="76d93-112">EAPHost will call the supplicant-provided callback function with the unique interface GUID and the VOID pointer when the quarantine state of the machine changes.</span></span> <span data-ttu-id="76d93-113">Wenn EAPHost die von Supplicant bereitgestellte Rückruffunktion aufruft, antwortet der Supplicant, indem er die vom Schnittstellen-GUID/void-Zeiger identifizierte logische Netzwerkverbindung abbricht und die Authentifizierung mit **eaphostpeer erbeginsession** erneut startet.</span><span class="sxs-lookup"><span data-stu-id="76d93-113">When EAPHost calls the supplicant-provided callback function, the supplicant responds by tearing down the logical network connection identified by the interface GUID/VOID pointer and begins authentication again using **EapHostPeerBeginSession**.</span></span>

<span data-ttu-id="76d93-114">EAPHost kann die vom Supplicant bereitgestellte Rückruffunktion jederzeit aufrufen: vor, während einer aktiven Authentifizierung oder nach Abschluss der Authentifizierung (nachdem [**eaphostpeer-EndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) aufgerufen wurde, aber nicht vor dem Aufrufen von [**eaphostpeer-clearconnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) ).</span><span class="sxs-lookup"><span data-stu-id="76d93-114">EAPHost may call the supplicant-supplied callback function at any time: before, during an active authentication, or after the authentication has been completed (after [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) has been called but not before [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) has been called).</span></span> <span data-ttu-id="76d93-115">Der Supplicant sollte immer Antworten, indem er die logische Netzwerkverbindung abbricht und erneut authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="76d93-115">The supplicant should always respond by tearing down the logical network connection and re-authenticating.</span></span>

<span data-ttu-id="76d93-116">Wenn der Supplicant heruntergefahren oder nicht mehr benachrichtigt wird, dass der Isolations Status nicht mehr empfangen werden kann, sollte der Supplicant [**eaphostpeer-clearconnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) aufrufen und die entsprechende Schnittstellen-GUID angeben.</span><span class="sxs-lookup"><span data-stu-id="76d93-116">If the supplicant is shutting down or choosing to no longer receive notification of isolation state changes, the supplicant should call [**EapHostPeerClearConnection**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerclearconnection) and specify the appropriate interface GUID.</span></span> <span data-ttu-id="76d93-117">Wenn der Supplicant die Isolation der Verbindung des logischen Netzwerks ermitteln möchte, kann der Supplicant diese Informationen von **eaphostpeer. isolationstate** abrufen, wenn [**eaphostpeer-methodresult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) von [**eaphostpeer ergetresult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="76d93-117">If the supplicant wishes to determine the isolation of the logical network connection, the supplicant can obtain that information from **EapHostPeerMethodResult.isolationState** when the [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult) is obtained from [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult).</span></span>

## <a name="eaphost-related-nap-information"></a><span data-ttu-id="76d93-118">EAPHost Verwandte NAP-Informationen</span><span class="sxs-lookup"><span data-stu-id="76d93-118">EAPHost Related NAP Information</span></span>

<span data-ttu-id="76d93-119">Informationen zu NAP-Informationen für die EAPHost-API finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="76d93-119">For EAPHost API related NAP information refer to the following topics.</span></span>

-   [<span data-ttu-id="76d93-120">**EAP \_ - \_ Attributtyp**</span><span class="sxs-lookup"><span data-stu-id="76d93-120">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
-   [<span data-ttu-id="76d93-121">**EAP- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="76d93-121">**EAP\_ERROR**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)
-   [<span data-ttu-id="76d93-122">Häufig gestellte Fragen zu EAPHost-Supplicant</span><span class="sxs-lookup"><span data-stu-id="76d93-122">EAPHost Supplicant Frequently Asked Questions</span></span>](eaphost-supplicant-frequently-asked-questions.md)
-   [<span data-ttu-id="76d93-123">**Eigenschaften der EAP-Methode**</span><span class="sxs-lookup"><span data-stu-id="76d93-123">**EAP Method Properties**</span></span>](eap-method-properties.md)
-   [<span data-ttu-id="76d93-124">**Eaphosteterbeginsession**</span><span class="sxs-lookup"><span data-stu-id="76d93-124">**EapHostPeerBeginSession**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession)
-   [<span data-ttu-id="76d93-125">**EAP-bezogene Fehler-und Informations Konstanten**</span><span class="sxs-lookup"><span data-stu-id="76d93-125">**EAP Related Error and Information Constants**</span></span>](eap-related-error-and-information-constants.md)
-   [<span data-ttu-id="76d93-126">**Isolations \_ Status**</span><span class="sxs-lookup"><span data-stu-id="76d93-126">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)
-   [<span data-ttu-id="76d93-127">**Notificationhandler**</span><span class="sxs-lookup"><span data-stu-id="76d93-127">**NotificationHandler**</span></span>](/previous-versions/windows/desktop/api)

## <a name="additional-resources"></a><span data-ttu-id="76d93-128">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="76d93-128">Additional Resources</span></span>


-   <span data-ttu-id="76d93-129">Eine Liste der NAP-Ressourcen finden Sie unter [Netzwerk Zugriffsschutz](https://go.microsoft.com/fwlink/p/?linkid=84107).</span><span class="sxs-lookup"><span data-stu-id="76d93-129">For a list of NAP resources, see [Network Access Protection](https://go.microsoft.com/fwlink/p/?linkid=84107).</span></span>
-   <span data-ttu-id="76d93-130">Informationen zum Statement of Health finden Sie unter [Network Access Protection (NAP)-SoH (Statement of Health)-Nachrichten](https://go.microsoft.com/fwlink/p/?linkid=83918).</span><span class="sxs-lookup"><span data-stu-id="76d93-130">For Statement of Health information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>
-   <span data-ttu-id="76d93-131">Informationen zur Unternehmensnetzwerk-Gruppen Webseite und zum Blog finden Sie unter [Netzwerk Zugriffsschutz (Network Access Protection, NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span><span class="sxs-lookup"><span data-stu-id="76d93-131">For the Enterprise Networking Group webpage and blog, see [Network Access Protection (NAP)](https://go.microsoft.com/fwlink/p/?linkid=83845).</span></span>
-   <span data-ttu-id="76d93-132">Informationen zur NAP-API finden Sie unter [Netzwerk Zugriffsschutz](/windows/desktop/NAP/network-access-protection-start-page).</span><span class="sxs-lookup"><span data-stu-id="76d93-132">For NAP API information, see [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page).</span></span>


## <a name="related-topics"></a><span data-ttu-id="76d93-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76d93-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d93-134">Konfigurieren der Benutzeroberfläche der EAP-Methode</span><span class="sxs-lookup"><span data-stu-id="76d93-134">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="76d93-135">Aktivieren von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="76d93-135">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="76d93-136">Implementieren In-Band NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="76d93-136">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="76d93-137">Übertragen von Daten zwischen den Supplicant-und EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="76d93-137">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="76d93-138">EAPHost-Supplicants</span><span class="sxs-lookup"><span data-stu-id="76d93-138">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 