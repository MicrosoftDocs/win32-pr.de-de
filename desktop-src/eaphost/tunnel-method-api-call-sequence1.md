---
title: Tunnel Methode API-Rückruf Sequenz
description: Erfahren Sie mehr über die API-Rückruf Sequenz für Tunnel Methoden. Hier finden Sie eine Übersicht und weitere verfügbare Ressourcen.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316503"
---
# <a name="tunnel-method-api-call-sequence"></a><span data-ttu-id="4dd11-104">Tunnel Methode API-Rückruf Sequenz</span><span class="sxs-lookup"><span data-stu-id="4dd11-104">Tunnel Method API Call Sequence</span></span>

<span data-ttu-id="4dd11-105">In diesem Thema wird die API-Rückruf Sequenz für Tunnel Methoden behandelt.</span><span class="sxs-lookup"><span data-stu-id="4dd11-105">This topic covers the API call sequence for Tunnel Methods</span></span>

## <a name="tunnel-method-call-sequence-overview"></a><span data-ttu-id="4dd11-106">Übersicht über die Tunnel Methoden-Rückruf Sequenz</span><span class="sxs-lookup"><span data-stu-id="4dd11-106">Tunnel Method Call Sequence Overview</span></span>

<span data-ttu-id="4dd11-107">Wenn Supplicant eine Anforderung für Benutzeridentität und Benutzerdaten erhält, tritt in der Regel der folgende API-Aufruffluss auf.</span><span class="sxs-lookup"><span data-stu-id="4dd11-107">When Supplicant gets request for user identity and user data the following API call flow typically occurs.</span></span>

-   <span data-ttu-id="4dd11-108">Der Supplicant ruft eaphostpeer Server processreceivedpacket auf EAPHost auf, um das vom Authentifikator empfangene Paket zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4dd11-108">The Supplicant calls EapHostPeerProcessReceivedPacket on EapHost, to process the packet received from the authenticator.</span></span>
-   <span data-ttu-id="4dd11-109">Bei der Verarbeitung dieses Pakets bestimmt EAPHost es als identityrequest-Paket und ruft [**eappeergetidentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) auf Tunnel Methode auf, um die für die Authentifizierung zu verwendende Benutzeridentität zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4dd11-109">Upon processing this packet, EAPHost determines it as IdentityRequest packet and calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on tunnel method to obtain the user identity to use for authentication.</span></span>
-   <span data-ttu-id="4dd11-110">Wenn die Tunnel Methode eine Benutzeridentität aus der inneren Methode abrufen muss, ruft Sie [**eaphostpeer ergetidentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) auf inner EAPHost auf, der wiederum [**eappeergetidentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) für die innere Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="4dd11-110">If tunnel method needs to obtain user identity from the inner method, it calls [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) on inner EAPHost, which in turn calls [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) on the inner method.</span></span>

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a><span data-ttu-id="4dd11-111">Benutzerinteraktion mit dem Tunnel Methoden-API-Aufruffluss</span><span class="sxs-lookup"><span data-stu-id="4dd11-111">User Interaction with the Tunnel Methods API Call Flow</span></span>

<span data-ttu-id="4dd11-112">In bestimmten Fällen, wenn die Identität nicht verfügbar ist oder wenn der Benutzer zusätzliche Informationen bereitstellen muss, löst die EAP-Methode ein Benutzeroberflächen Dialogfeld für den Supplicant aus.</span><span class="sxs-lookup"><span data-stu-id="4dd11-112">In certain cases, when the identity is not available, or when the user must provide additional information, Eap Method raises an user interface dialog box on the supplicant.</span></span>

<span data-ttu-id="4dd11-113">In solchen Fällen findet die folgende Rückruf Sequenz statt, um Informationen direkt vom Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4dd11-113">In such cases following call sequence typically takes place to get information directly from the user.</span></span>

-   <span data-ttu-id="4dd11-114">Die EAP-Tunnel Methode gibt den Aktions Code zum Aufrufen der Benutzeroberfläche für EAPHost zurück.</span><span class="sxs-lookup"><span data-stu-id="4dd11-114">Tunnel Eap Method returns action code to invoke UI to EapHost.</span></span> <span data-ttu-id="4dd11-115">Supplicant ruft [**eaphostpeer ergetuicontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)auf, um die aktuellen Kontextinformationen für die Benutzeroberfläche für das Dialogfeld Benutzeroberfläche abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4dd11-115">Supplicant calls [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)to obtain the current user interface context information for the user interface dialog box.</span></span>
-   <span data-ttu-id="4dd11-116">Der Supplicant ruft dann [ **eaphosteterinvokeinteractiveui auf.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span><span class="sxs-lookup"><span data-stu-id="4dd11-116">Supplicant then calls [**EapHostPeerInvokeInteractiveUI.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)</span></span> <span data-ttu-id="4dd11-117">Diese Funktion verwendet die UI-Kontextinformationen, um eine interaktive Benutzeroberfläche zu verwenden, die zum erhalten von Anmelde Informationen des Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4dd11-117">This function uses the UI context information to raise an interactive user interface which is used to get credential information from the user.</span></span> <span data-ttu-id="4dd11-118">Der UI-Prozess lädt Eappcfg.dll und ruft die Zeiger auf "eappeerinvokeinteractiveui" und "eappeerfrememory" ab.</span><span class="sxs-lookup"><span data-stu-id="4dd11-118">The UI process loads Eappcfg.dll and obtains the pointers to EapPeerInvokeInteractiveUI and EapPeerFreeMemory.</span></span>
    > [!Note]  
    > <span data-ttu-id="4dd11-119">Der UI-Prozess erfasst in der Regel die Benutzeroberfläche oder verarbeitet interaktive Benutzeroberflächen und ist vom Supplicant-Prozess getrennt.</span><span class="sxs-lookup"><span data-stu-id="4dd11-119">UI process typically collects UI or handles interactive UI and is separate from the supplicant process.</span></span> <span data-ttu-id="4dd11-120">Das Trennen der beiden Prozesse ist keine Voraussetzung für EAPHost, aber dies hat den Vorteil, dass der UI-Prozess mit dem Desktop interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="4dd11-120">Separating the two processes is not a requirement of EAPHost, but doing so has the advantage of allowing the UI process to interact with the desktop.</span></span>

     

-   <span data-ttu-id="4dd11-121">EAPHost ruft [**eappeerinvokeidentityui**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) auf Tunnel Methode auf, um Benutzer Identitätsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4dd11-121">EapHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on tunnel method to obtain user identity information.</span></span>
-   <span data-ttu-id="4dd11-122">Zum Abrufen der Benutzeridentität aus der inneren Methode ruft die Tunnel Methode [**eaphostpeer-invokeidentityui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) auf dem inneren EAPHost auf.</span><span class="sxs-lookup"><span data-stu-id="4dd11-122">In order to obtain user identity from inner method, tunnel method calls [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) on inner EAPHost.</span></span>
-   <span data-ttu-id="4dd11-123">Inner EAPHost ruft [**eappeerinvokeidentityui**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) auf der inneren Methode auf, um die Benutzeroberfläche für Benutzer Identitäten aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4dd11-123">Inner EAPHost calls [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) on inner method to invoke user identity UI.</span></span>
-   <span data-ttu-id="4dd11-124">[**Eaphostpeerot-Kontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) stellt der EAP-Peer Methode, die auf EAPHost geladen wird, nach dem Auslösung der Benutzeroberfläche neue oder aktualisierte Benutzeroberflächen-Kontextinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="4dd11-124">[**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) provides a new or updated UI context information to the EAP peer method loaded on EAPHost after the UI has been raised.</span></span>

<span data-ttu-id="4dd11-125">Im folgenden Diagramm wird die API-Rückruf Sequenz für Tunnel Methoden erläutert.</span><span class="sxs-lookup"><span data-stu-id="4dd11-125">Following diagram explains the API Call Sequence for Tunnel Methods</span></span>

![Tunnel Methoden-API-Rückruf Sequenz](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a><span data-ttu-id="4dd11-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4dd11-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd11-128">EAPHost-Rückruf Sequenz</span><span class="sxs-lookup"><span data-stu-id="4dd11-128">EAPHost Call Sequence</span></span>](about-eaphost-call-sequences.md)
</dt> <dt>

[<span data-ttu-id="4dd11-129">Supplicant-API-Rückruf Sequenz</span><span class="sxs-lookup"><span data-stu-id="4dd11-129">Supplicant API Call Sequence</span></span>](supplicant-api-call-sequence.md)
</dt> <dt>

[<span data-ttu-id="4dd11-130">EAPHost-Supplicant-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="4dd11-130">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




