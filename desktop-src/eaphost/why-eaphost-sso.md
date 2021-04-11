---
title: SSO-EAPHost-Szenarioübersicht
description: Enthält zwei Szenarien, in denen die Vorteile eines aktivierten Supplicant (Single Sign-on, einmaliges Anmelden) aufgezeigt werden.
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101126"
---
# <a name="sso-eaphost-scenario-overview"></a><span data-ttu-id="bb216-103">SSO-EAPHost-Szenarioübersicht</span><span class="sxs-lookup"><span data-stu-id="bb216-103">SSO EAPHost Scenario Overview</span></span>

<span data-ttu-id="bb216-104">Das folgende Thema enthält zwei Szenarien, in denen die Vorteile eines aktivierten Supplicant (Single Sign-on, einmaliges Anmelden) veranschaulicht werden.</span><span class="sxs-lookup"><span data-stu-id="bb216-104">The following topic contains two scenarios that demonstrate the advantages of a Single-Sign-On (SSO) enabled supplicant.</span></span>

## <a name="about-the-scenarios"></a><span data-ttu-id="bb216-105">Informationen zu den Szenarien</span><span class="sxs-lookup"><span data-stu-id="bb216-105">About the Scenarios</span></span>

<span data-ttu-id="bb216-106">SSO stellt Funktionen bereit, um zusätzliche Benutzer Anmelde Informationen zu erhalten, als normalerweise im EAP-benutzerblob gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bb216-106">SSO provides functionality to retain additional user credential information than is traditionally stored in the EAP user BLOB.</span></span> <span data-ttu-id="bb216-107">Im Gegensatz zu anderen Anmelde Informationsprozessen können von SSO aktivierte Supplicants Anmelde Situationen wie das AP-Roaming und die Kenn Wort Änderung ohne Benutzereingriff auflösen.</span><span class="sxs-lookup"><span data-stu-id="bb216-107">Unlike other credential processes, SSO-enabled supplicants can resolve login situations like AP roaming, and password change without user intervention.</span></span>

## <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="bb216-108">SSO EAP-TLS Pin Caching-Verhalten</span><span class="sxs-lookup"><span data-stu-id="bb216-108">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="bb216-109">Ein Supplicant kann die Netzwerk Authentifizierung mit einer Smartcard-basierten EAP-Methode wie z. b. EAP-TLS (Extensible Authentication Protocol Transport Layer Security) versuchen.</span><span class="sxs-lookup"><span data-stu-id="bb216-109">A supplicant can attempt network authentication using a smartcard-based EAP method such as Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span></span> <span data-ttu-id="bb216-110">In diesem und ähnlichen Szenario erhält der Supplicant die Smartcard-PIN vom Benutzer und ruft ein Benutzerzertifikat für die Netzwerk Authentifizierung ab, gefolgt von einem Windows-Anmelde Namen auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="bb216-110">In this and similar scenarios, the supplicant obtains the smartcard PIN from the user and retrieves a user certificate for network authentication followed by a call to WinLogin on the local computer.</span></span> <span data-ttu-id="bb216-111">Nach erfolgreicher Authentifizierung speichert der Supplicant den benutzerblob zwischen und speichert keine Benutzer-PIN-Informationen.</span><span class="sxs-lookup"><span data-stu-id="bb216-111">After successful authentication the supplicant caches the user BLOB, and does not store user PIN information.</span></span>

<span data-ttu-id="bb216-112">Wenn der Benutzer zu einem anderen Speicherort wechselt, müssen Wiederaufnahme-und erneute Authentifizierung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="bb216-112">When the user roams to a different location session resumption and re-authentication must occur.</span></span> <span data-ttu-id="bb216-113">Da das Zertifikat nicht vor der Anmeldung gespeichert werden kann, schlägt die Benutzerauthentifizierung fehl, und der Benutzer-BLOB wird vom Supplicant geleert.</span><span class="sxs-lookup"><span data-stu-id="bb216-113">Since the certificate cannot be stored pre-logon, the user authentication will fail and the supplicant flushes the user BLOB.</span></span> <span data-ttu-id="bb216-114">An diesem Punkt ist die Benutzer-PIN erforderlich, um das Benutzerzertifikat für die Netzwerk Authentifizierung von der Smartcard abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bb216-114">At this point the user PIN is required to retrieve the user certificate from the smartcard for network authentication.</span></span> <span data-ttu-id="bb216-115">Da SSO die PIN zwischenspeichert, kann das Zertifikat ohne Benutzereingriff abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bb216-115">Because SSO caches the PIN, the certificate can be retrieved without user intervention.</span></span> <span data-ttu-id="bb216-116">Ohne SSO müsste EAP-TLS erneut eine Benutzeroberfläche für die PIN-Erfassung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bb216-116">Without SSO, EAP-TLS would have to raise a PIN collection UI again.</span></span>

<span data-ttu-id="bb216-117">Eine schrittweise Vorgehensweise finden Sie unter [SSO EAP-TLS Pin Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="bb216-117">For a step-by-step approach, see [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span></span>

## <a name="sso-password-change-behavior"></a><span data-ttu-id="bb216-118">Verhalten von SSO-Kenn Wort Änderungen</span><span class="sxs-lookup"><span data-stu-id="bb216-118">SSO Password Change Behavior</span></span>

<span data-ttu-id="bb216-119">Ein Supplicant kann die Netzwerk Authentifizierung mit einer Kenn Wort basierten EAP-Methode wie Microsoft Challenge Handshake Authentication Protocol, Version 2,0 (MS-CHAPv2), verwenden, die für die Verwendung von winlogin-Anmelde Informationen konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="bb216-119">A supplicant can attempt network authentication using a password-based EAP method such as Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2), configured to use WinLogin credentials.</span></span> <span data-ttu-id="bb216-120">In diesem Szenario sammelt das Supplicant-Benutzer Anmelde Informationen einmal und stellt Sie für die Netzwerk Authentifizierung per EAPHost bereit.</span><span class="sxs-lookup"><span data-stu-id="bb216-120">In this scenario, the supplicant collects user credentials once and provides them to EAPHost for network authentication.</span></span> <span data-ttu-id="bb216-121">Nach erfolgreicher Netzwerk Authentifizierung verwendet der Supplicant denselben Satz von Anmelde Informationen für winlogin.</span><span class="sxs-lookup"><span data-stu-id="bb216-121">After successful network authentication the supplicant uses the same set of credentials for WinLogin.</span></span>

<span data-ttu-id="bb216-122">Wenn Anmelde Informationen, z. b. das Benutzer Kennwort, während der Netzwerk Authentifizierung ohne aktivierten Supplicant geändert wurden, führt der nachfolgende winlogin-Befehl zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="bb216-122">However, if credentials such as the user password were changed during network authentication without an SSO-enabled supplicant, the subsequent WinLogin call will result in failure.</span></span> <span data-ttu-id="bb216-123">SSO behält die neuen Anmelde Informationen bei und ermöglicht einen erfolgreichen winlogin-Vorgang ohne zusätzlichen Benutzereingriff.</span><span class="sxs-lookup"><span data-stu-id="bb216-123">SSO retains the new credentials and allows a successful WinLogin without additional user intervention.</span></span>

<span data-ttu-id="bb216-124">Eine Schritt-für-Schritt-Vorgehensweise finden Sie unter SSO-Kenn [Wort Änderungs Verhalten](sso-password-change-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="bb216-124">For a step-by-step approach, see [SSO Password Change Behavior](sso-password-change-behavior-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb216-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb216-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb216-126">SSO und PLAP</span><span class="sxs-lookup"><span data-stu-id="bb216-126">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




