---
title: Aktivieren von Gruppenrichtlinie
description: Erfahren Sie, wie Sie den Supplicant durch Aktivieren der Gruppenrichtlinie konfigurieren. Weitere Informationen finden Sie unter Überlegungen zu Supplicants und Anzeigen zusätzlicher verfügbarer Ressourcen.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391035"
---
# <a name="enabling-group-policy"></a><span data-ttu-id="22ce0-104">Aktivieren von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="22ce0-104">Enabling Group Policy</span></span>

<span data-ttu-id="22ce0-105">In diesem Thema wird erläutert, wie Sie den Supplicant durch Aktivieren der Gruppenrichtlinie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="22ce0-105">This topic explains how to configure the supplicant by enabling group policy.</span></span> <span data-ttu-id="22ce0-106">EAPHost-Supplicants können an der Gruppenrichtlinie teilnehmen, damit ein Netzwerkadministrator seine Netzwerk Computer zentral konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="22ce0-106">EAPHost supplicants can participate in group policy to allow a network administrator to centrally configure their network machines.</span></span>

<span data-ttu-id="22ce0-107">Die genaue Methode und der Mechanismus, mit dem sich der Supplicant für die Teilnahme an der Gruppenrichtlinie entscheidet, liegt im Ermessen des Supplicant.</span><span class="sxs-lookup"><span data-stu-id="22ce0-107">The precise method and mechanism by which the supplicant chooses to participate in group policy is at the discretion of the supplicant.</span></span> <span data-ttu-id="22ce0-108">Beispiele für Mechanismen für die Gruppenrichtlinien Beteiligung sind Client-/serverseitige Erweiterungen, administrative Vorlagen usw.</span><span class="sxs-lookup"><span data-stu-id="22ce0-108">Examples of mechanisms for group policy participation include client/server-side extensions, administrative template, and so forth.</span></span>

## <a name="considerations-when-enabling-group-policy"></a><span data-ttu-id="22ce0-109">Überlegungen beim Aktivieren von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="22ce0-109">Considerations When Enabling Group Policy</span></span>

<span data-ttu-id="22ce0-110">Dies sind die Überlegungen für Supplicants in Bezug auf die Gruppenrichtlinie und EAP.</span><span class="sxs-lookup"><span data-stu-id="22ce0-110">These are the considerations for supplicants with respect to group policy and EAP.</span></span>

1.  <span data-ttu-id="22ce0-111">Die EAP-Konfiguration sollte immer als XML-Datei, wann immer möglich, und nicht im Binärformat gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="22ce0-111">EAP configuration should always be stored as XML whenever possible and not in the binary format.</span></span> <span data-ttu-id="22ce0-112">Die Gruppenrichtlinie kann auf jeden Computer in der Domäne angewendet werden, und die EAP-Methoden Konfiguration und die Benutzerdaten sind nicht garantiert zwischen 32-Bit-und 64-Bit-Prozessorarchitekturen portabel.</span><span class="sxs-lookup"><span data-stu-id="22ce0-112">Group policy may be applied to any machine in the domain, and EAP method configuration and user data are not guaranteed to be portable between 32-bit and 64-bit processor architectures.</span></span> <span data-ttu-id="22ce0-113">XML löst die Probleme der Prozessorarchitektur Grenzen auf, da der Supplicant den von der Prozessorarchitektur unabhängigen XML-Code zum Zeitpunkt der Authentifizierung lokal in die binäre Darstellung der Konfiguration konvertiert.</span><span class="sxs-lookup"><span data-stu-id="22ce0-113">XML resolves the processor architecture boundary issues as the supplicant locally converts the processor-architecture independent XML to the binary representation of the configuration at authentication time.</span></span>

    <span data-ttu-id="22ce0-114">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="22ce0-114">For more information, see the following topics.</span></span>

    -   [<span data-ttu-id="22ce0-115">Allgemeine häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="22ce0-115">General Frequently Asked Questions</span></span>](general-frequently-asked-questions.md)
    -   <span data-ttu-id="22ce0-116">[Häufig gestellte Fragen zur EAP-Methode](eap-method-frequently-asked-questions.md).</span><span class="sxs-lookup"><span data-stu-id="22ce0-116">[EAP Method Frequently Asked Questions](eap-method-frequently-asked-questions.md).</span></span>
    -   [<span data-ttu-id="22ce0-117">**EapHostPeerConfigXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="22ce0-117">**EapHostPeerConfigXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [<span data-ttu-id="22ce0-118">**EapHostPeerCredentialsXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="22ce0-118">**EapHostPeerCredentialsXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  <span data-ttu-id="22ce0-119">Wenn eine serverseitige Erweiterung für Gruppenrichtlinien verwendet wird, ruft die Erweiterung [**eaphostpeergetmethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) in der Regel auf, um die verfügbaren Methoden zu ermitteln und eine entsprechende EAP-Konfiguration für diese Richtlinie zu generieren.</span><span class="sxs-lookup"><span data-stu-id="22ce0-119">If a group policy server-side extension is used, the extension will call [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) typically to determine available methods and to generate appropriate EAP configuration for that policy.</span></span> <span data-ttu-id="22ce0-120">Die Richtlinie wird dann an geeignete Netzwerk Clients übertragen, auf denen die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="22ce0-120">The policy is then pushed out to appropriate network clients where the policy is applied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22ce0-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22ce0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22ce0-122">Konfigurieren der Benutzeroberfläche der EAP-Methode</span><span class="sxs-lookup"><span data-stu-id="22ce0-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="22ce0-123">Implementieren In-Band NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="22ce0-123">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="22ce0-124">Implementieren der NAP-Unterstützung für EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="22ce0-124">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="22ce0-125">Übertragen von Daten zwischen den Supplicant-und EAP-Methoden</span><span class="sxs-lookup"><span data-stu-id="22ce0-125">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="22ce0-126">EAPHost-Supplicants</span><span class="sxs-lookup"><span data-stu-id="22ce0-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




