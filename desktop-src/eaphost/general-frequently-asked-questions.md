---
title: Allgemeine häufig gestellte Fragen
description: Lesen Sie Antworten auf häufig gestellte Fragen zu den EAPHost-APIs, z. b. "wie lautet die Lebensdauer einer Authentifizierung?".
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106339105"
---
# <a name="general-frequently-asked-questions"></a><span data-ttu-id="6e23b-103">Allgemeine häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="6e23b-103">General Frequently Asked Questions</span></span>

<span data-ttu-id="6e23b-104">Im folgenden Thema finden Sie Antworten auf häufig gestellte Fragen zu den EAPHost-APIs.</span><span class="sxs-lookup"><span data-stu-id="6e23b-104">The following topic provides answers to commonly-asked questions about the EAPHost APIs.</span></span>

### <a name="general-frequently-asked-questions"></a><span data-ttu-id="6e23b-105">Allgemeine häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="6e23b-105">General Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e23b-106">Frage</span><span class="sxs-lookup"><span data-stu-id="6e23b-106">Question</span></span></th>
<th><span data-ttu-id="6e23b-107">Antwort</span><span class="sxs-lookup"><span data-stu-id="6e23b-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e23b-108">Was ist ein Supplicant?</span><span class="sxs-lookup"><span data-stu-id="6e23b-108">What is a supplicant?</span></span></td>
<td><span data-ttu-id="6e23b-109">Der Supplicant ist die Entität, die mithilfe von EAPHost authentifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e23b-109">The supplicant is the entity to be authenticated using EAPHost.</span></span> <span data-ttu-id="6e23b-110">Typische Supplicants sind [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Clients, 802,3-Clients und RRAS (Routing-und RAS-Dienst), Punkt-zu-Punkt-Clients (PPP).</span><span class="sxs-lookup"><span data-stu-id="6e23b-110">Typical supplicants are [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) clients, 802.3 clients, and Routing and Remote Access Service (RRAS), Point-to-Point (PPP) clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-111">Was ist ein Peer?</span><span class="sxs-lookup"><span data-stu-id="6e23b-111">What is a peer?</span></span></td>
<td><span data-ttu-id="6e23b-112">Der Peer ist die Clientseite einer EAP-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="6e23b-112">The peer is the client side of an EAP authentication.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-113">Wie unterscheidet sich ein Peer von einem Supplicant?</span><span class="sxs-lookup"><span data-stu-id="6e23b-113">How does a peer differ from a supplicant?</span></span></td>
<td><span data-ttu-id="6e23b-114">Der Supplicant transportiert Pakete, während ein Peer dies nicht tut.</span><span class="sxs-lookup"><span data-stu-id="6e23b-114">The supplicant transports packets, whereas a peer does not.</span></span> <span data-ttu-id="6e23b-115">Dennoch sind die Begriffe "Peer", "Supplicant" und "Client" größtenteils Synonym.</span><span class="sxs-lookup"><span data-stu-id="6e23b-115">Nonetheless, the terms peer, supplicant and client are largely synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-116">Was ist ein Authentifikator?</span><span class="sxs-lookup"><span data-stu-id="6e23b-116">What is an authenticator?</span></span></td>
<td><span data-ttu-id="6e23b-117">Der Authentifikator ist der drahtlos Zugriffspunkt, der Netzwerk Zugriffs Server (Network Access Server, NAS) oder das Netzwerk Zugriffsgerät (nad), das den Supplicant authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="6e23b-117">The authenticator is the wireless access point, network access server (NAS), or network access device (NAD) that authenticates the supplicant.</span></span> <span data-ttu-id="6e23b-118">Der Authentifikator wird auch als EAP-Server bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6e23b-118">The authenticator is also known as the EAP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-119">Was ist die Lebensdauer einer Authentifizierung?</span><span class="sxs-lookup"><span data-stu-id="6e23b-119">What is the lifetime of an authentication?</span></span></td>
<td><span data-ttu-id="6e23b-120">Die Lebensdauer einer einzelnen Authentifizierungs Sitzung auf der Clientseite ist alles, was zwischen den aufgerufenen Funktionen [<strong>eaphostpeer erbeginsession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) und [<strong>eaphostpeer erendsession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) auftritt.</span><span class="sxs-lookup"><span data-stu-id="6e23b-120">The lifetime of a single authentication session on the client side is everything that occurs between the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) and [<strong>EapHostPeerEndSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) functions being called.</span></span> <span data-ttu-id="6e23b-121">Die Lebensdauer auf der Authenticator-Seite ist alles, was zwischen den Funktionen [<strong>eappeerbeginsession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) und [<strong>eappeerendsession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession) auftritt.</span><span class="sxs-lookup"><span data-stu-id="6e23b-121">The lifetime on the authenticator side is everything that occurs between the [<strong>EapPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) and [<strong>EapPeerEndSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-122">Was ist ein BLOB?</span><span class="sxs-lookup"><span data-stu-id="6e23b-122">What is a BLOB?</span></span> <span data-ttu-id="6e23b-123">Warum würde ich ein Konfigurations-BLOB (Binary) in XML konvertieren?</span><span class="sxs-lookup"><span data-stu-id="6e23b-123">Why would I convert a configuration (binary) BLOB to XML?</span></span></td>
<td><span data-ttu-id="6e23b-124">Ein BLOB ist eine Binary Large Object.</span><span class="sxs-lookup"><span data-stu-id="6e23b-124">A BLOB is a binary large object.</span></span> <span data-ttu-id="6e23b-125">XML hat mehrere Vorteile gegenüber einem binären konfigurationsblob.</span><span class="sxs-lookup"><span data-stu-id="6e23b-125">XML has several advantages over a binary configuration BLOB.</span></span> <span data-ttu-id="6e23b-126">Konfigurationsdaten, die in XML gespeichert werden, sind lesbarer, Benutzer bearbeitbarer und plattformübergreifender.</span><span class="sxs-lookup"><span data-stu-id="6e23b-126">Configuration data that is stored in XML is human-readable, human-editable, and cross-platform.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-127">Wann kann ich ein gespeichertes XML-BLOB in ein binäres Blob konvertieren?</span><span class="sxs-lookup"><span data-stu-id="6e23b-127">When do I convert a stored XML BLOB back to a binary BLOB?</span></span></td>
<td><span data-ttu-id="6e23b-128">Es ist möglich, ein binäres Blob oder ein XML-BLOB zu speichern, aber Sie müssen das XML-BLOB immer wieder in ein binäres Blob konvertieren, bevor es mit Lauf Zeit-APIs verwendet werden kann. die Lauf Zeit-APIs können ein XML-Verzeichnis nicht akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="6e23b-128">It's possible to store a binary BLOB or XML BLOB, but you must always convert the XML BLOB back to a binary BLOB before use with run-time APIs; the run-time APIs cannot accept an XML directory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-129">Was sind native Methoden?</span><span class="sxs-lookup"><span data-stu-id="6e23b-129">What are native methods?</span></span></td>
<td><span data-ttu-id="6e23b-130">Native EAP-Methoden verwenden die neue EAPHost-API.</span><span class="sxs-lookup"><span data-stu-id="6e23b-130">Native EAP methods use the new EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-131">Was sind Legacy Methoden?</span><span class="sxs-lookup"><span data-stu-id="6e23b-131">What are legacy methods?</span></span></td>
<td><span data-ttu-id="6e23b-132">Ältere EAP-Methoden werden in der [Extensible Authentication-Protokoll Referenz](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference)definiert.</span><span class="sxs-lookup"><span data-stu-id="6e23b-132">Legacy EAP methods are defined in the [Extensible Authentication Protocol Reference](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span></span> <span data-ttu-id="6e23b-133">Die Legacy-EAP-Methoden stehen für die Verwendung in Windows Vista und Windows Server 2008 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6e23b-133">The legacy EAP methods are available for use in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6e23b-134">Diese Methoden sind möglicherweise nicht für die Verwendung in nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6e23b-134">These methods may not be available for use in subsequent versions of the operating system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-135">Worin besteht der Unterschied zwischen Legacy-und systemeigenen Methoden?</span><span class="sxs-lookup"><span data-stu-id="6e23b-135">What's the difference between legacy and native methods?</span></span></td>
<td><span data-ttu-id="6e23b-136">Die nativen APIs sind einfacher und verfügen über weniger Features.</span><span class="sxs-lookup"><span data-stu-id="6e23b-136">The native APIs are simpler and have fewer features.</span></span> <span data-ttu-id="6e23b-137">Alle neuen EAP-Methoden sollten mithilfe der EAPHost-API geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6e23b-137">All new EAP methods should be written using the EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-138">Was ist eine &quot; Gruppenrichtlinie &quot; ?</span><span class="sxs-lookup"><span data-stu-id="6e23b-138">What is &quot;group policy&quot;?</span></span></td>
<td><span data-ttu-id="6e23b-139">Eine Beschreibung der Gruppenrichtlinie finden Sie unter [Gruppenrichtlinie Sammlung](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="6e23b-139">For a description of group policy, see [Group Policy Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-140">Können EAPHost-Funktionen die von der Gruppenrichtlinie angegebene Konfigurationsrichtlinie außer Kraft setzen?</span><span class="sxs-lookup"><span data-stu-id="6e23b-140">Can EAPHost functions override configuration policy specified by group policy?</span></span></td>
<td><span data-ttu-id="6e23b-141">Nein, niemals.</span><span class="sxs-lookup"><span data-stu-id="6e23b-141">No, never.</span></span> <span data-ttu-id="6e23b-142">Wenn die Gruppenrichtlinie verwendet wird, werden die EAPHost-Konfigurationseinstellungen von Gruppenrichtlinien Einstellungen immer überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6e23b-142">If group policy is in use, group policy settings will always override EAPHost configuration settings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-143">Was ist einmaliges Anmelden (Single-Sign-on, SSO)?</span><span class="sxs-lookup"><span data-stu-id="6e23b-143">What is Single-Sign-On (SSO)?</span></span></td>
<td><span data-ttu-id="6e23b-144">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) ist ein Mechanismus für die Layer-2-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="6e23b-144">[802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) is a layer 2 authentication mechanism.</span></span> <span data-ttu-id="6e23b-145">Abhängig von der SSO-Konfiguration ermöglicht SSO Benutzern, sich vor oder unmittelbar nach der Anmeldung bei Windows bei dem Netzwerk mithilfe der [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) -Authentifizierung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="6e23b-145">Depending on the SSO configuration, SSO enables users to authenticate to the network using [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authentication before or immediately after logging on to Windows.</span></span> <span data-ttu-id="6e23b-146">SSO kann so konfiguriert werden, dass Windows-Anmelde Informationen für die Netzwerk Authentifizierung verwendet werden (in diesem Fall geben die Benutzer ihre Anmelde Informationen nur einmal ein) oder verwenden andere Anmelde Informationen für Windows-und Netzwerk Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="6e23b-146">SSO can be configured to use Windows credentials for network authentication (in which case users enter their credentials only once) or use different credentials for Windows and network authentication.</span></span> <span data-ttu-id="6e23b-147">Weitere Informationen finden Sie unter [SSO und PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="6e23b-147">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-148">Was ist der Zugriffs Anbieter für die Vorab Anmeldung (PLAP)</span><span class="sxs-lookup"><span data-stu-id="6e23b-148">What is Pre-Logon Access Provider (PLAP)</span></span></td>
<td><span data-ttu-id="6e23b-149">Weitere Informationen finden Sie unter [SSO und PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="6e23b-149">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-150">Was ist das Protected Extensible Authentication Protocol (Peer)?</span><span class="sxs-lookup"><span data-stu-id="6e23b-150">What is Protected Extensible Authentication Protocol (PEAP)?</span></span></td>
<td><span data-ttu-id="6e23b-151">Weitere Informationen finden Sie unter [Peer-App](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) und Informationen [zum Extensible Authentication-Protokoll](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span><span class="sxs-lookup"><span data-stu-id="6e23b-151">For more information, see [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) and [About Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-152">Wie geht es mit der Sitzungs Wiederaufnahme und der erneuten Authentifizierung durch.</span><span class="sxs-lookup"><span data-stu-id="6e23b-152">How does PEAP deal with session resumption and re-authentication?</span></span></td>
<td><span data-ttu-id="6e23b-153">Die Wiederaufnahme der Sitzung und die erneute Authentifizierung treten in der Regel beim Roaming in einem Drahtlos Netzwerk auf.</span><span class="sxs-lookup"><span data-stu-id="6e23b-153">Session resumption and re-authentication typically occurs while roaming on a wireless network.</span></span> <span data-ttu-id="6e23b-154">Die Windows-Datenschutz-API (DPAPI) bietet eine Möglichkeit, Daten zu schützen und an einen Benutzer und optional an die Anmelde Sitzung zu binden.</span><span class="sxs-lookup"><span data-stu-id="6e23b-154">Windows Data Protection API (DPAPI) provides a way to protect and bind data to a user and optionally the logon session.</span></span> <span data-ttu-id="6e23b-155">Der Aufrufer gibt [<strong>cryptprotectmemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) einen unverschlüsselten Puffer an, und DPAPI verschlüsselt den Speicher an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="6e23b-155">The caller gives [<strong>CryptProtectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) an unencrypted buffer and DPAPI will encrypt the memory in place.</span></span> <span data-ttu-id="6e23b-156">Später kann der Aufrufer den verschlüsselten Puffer an [<strong>cryptunprotectmemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) übergeben, und DPAPI entschlüsselt den Speicher wieder.</span><span class="sxs-lookup"><span data-stu-id="6e23b-156">Later, the caller can pass in the encrypted buffer to [<strong>CryptUnprotectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) and DPAPI will decrypt the memory, once again in place.</span></span> <span data-ttu-id="6e23b-157">Weitere Informationen finden Sie unter [TLS-interne Anwendungs Erweiterung (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) und [Peer-App](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="6e23b-157">For more information, see [TLS Inner Application Extension (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) and [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-158">Was ist EAP-Transport Level Security (EAP-TLS)?</span><span class="sxs-lookup"><span data-stu-id="6e23b-158">What is EAP-Transport Level Security (EAP-TLS)?</span></span></td>
<td><span data-ttu-id="6e23b-159">EAP-TLS ist ein Client/Server-Protokoll, bei dem unterschiedliche Zertifikat Profile in der Regel für den Client und den Server verwendet werden. Weitere Informationen finden Sie unter [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="6e23b-159">EAP-TLS is a client-server protocol in which distinct certificate profiles are typically used for the client and server.For more information, see [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-160">Gewusst wie eine Kenn Wort Änderung mithilfe der API der lokalen Sicherheits Autorität (Local Security Authority, LSA) implementieren?</span><span class="sxs-lookup"><span data-stu-id="6e23b-160">How do I implement a password change using the Local Security Authority (LSA) API?</span></span></td>
<td><span data-ttu-id="6e23b-161">Verwenden Sie die [<strong>lsacallauthenticationpackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage)-Funktion, um eine Kenn Wort Änderung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="6e23b-161">Use the [<strong>LsaCallAuthenticationPackage</strong>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) function to implement a password change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-162">Warum soll die Ablauf Verfolgung in EAPHost aktiviert werden?</span><span class="sxs-lookup"><span data-stu-id="6e23b-162">Why would I want to enable tracing in EAPHost?</span></span></td>
<td><span data-ttu-id="6e23b-163">Die Ablauf Verfolgungs Protokolle enthalten Debuginformationen (nur in englischer Sprache), die Microsoft-Entwicklern und-Partnern dabei helfen können, die Hauptursachen von Problemen zu ermitteln, die mit dem Authentifizierungsprozess auftreten.</span><span class="sxs-lookup"><span data-stu-id="6e23b-163">The trace logs contain debugging information (available in English only) that may assist Microsoft developers and partners in finding the root causes of any issues being experienced with the authentication process.</span></span> <span data-ttu-id="6e23b-164">Weitere Informationen finden Sie unter [aktivieren](enabling-tracing.md)der Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="6e23b-164">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-165">Warum erhalte ich den Fehlercode NTE_BAD_KEY_STATE (0x8009000bl), wenn ich die [Kryptografie](/windows/desktop/SecCrypto/cryptography-portal) -API zum Anmelden beim EAP-TLS-Austausch verwende?</span><span class="sxs-lookup"><span data-stu-id="6e23b-165">Why do I encounter the error code, NTE_BAD_KEY_STATE (0x8009000BL) when I use the [Cryptography](/windows/desktop/SecCrypto/cryptography-portal) API to sign into the EAP-TLS exchange?</span></span></td>
<td><span data-ttu-id="6e23b-166">In WinError. h wird NTE_BAD_KEY_STATE (0x8009000bl) als Schlüssel definiert, &quot; der nicht für die Verwendung im angegebenen Zustand gültig ist &quot; .</span><span class="sxs-lookup"><span data-stu-id="6e23b-166">In Winerror.h NTE_BAD_KEY_STATE (0x8009000BL) is defined as a &quot;key not valid for use in specified state&quot;.</span></span> <span data-ttu-id="6e23b-167">Dieser Fehler wird in der Regel in den folgenden Szenarien zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6e23b-167">This error is typically returned in the following scenarios.</span></span>
<ul>
<li><span data-ttu-id="6e23b-168">Beim Versuch, ein nicht exportier bares privates Schlüssel-BLOB zu exportieren</span><span class="sxs-lookup"><span data-stu-id="6e23b-168">When attempting to export a non-exportable private key BLOB</span></span></li>
<li><span data-ttu-id="6e23b-169">Bei einem erfolglosen Versuch, ein Pseudo zufälliges Funktions-Hash handle (PRF) mithilfe von [<strong>cryptkreatehash</strong>] (/Windows/Desktop/API/wincrypt/NF-wincrypt-cryptcreatehash) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6e23b-169">When unsuccessfully attempting to generate a pseudo-random function (PRF) hash handle using [<strong>CryptCreateHash</strong>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash)</span></span></li>
</ul>
<span data-ttu-id="6e23b-170">Weitere Informationen finden Sie unter [Beenden von Nachrichten im TLS 1,0-Protokoll](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="6e23b-170">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e23b-171">Was ist eine pseudo zufällige Funktion (PRF)?</span><span class="sxs-lookup"><span data-stu-id="6e23b-171">What is a pseudo-random function (PRF)?</span></span></td>
<td><span data-ttu-id="6e23b-172">Eine Funktion, die einen Schlüssel, eine Bezeichnung und einen Ausgangswert als Eingabe annimmt und dann eine Ausgabe beliebiger Länge erzeugt.</span><span class="sxs-lookup"><span data-stu-id="6e23b-172">A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span> <span data-ttu-id="6e23b-173">Weitere Informationen finden Sie unter [Beenden von Nachrichten im TLS 1,0-Protokoll](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="6e23b-173">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e23b-174">Wie wird EAPHost an Netzwerkadapter gebunden?</span><span class="sxs-lookup"><span data-stu-id="6e23b-174">How does EAPHost bind to network adapters?</span></span></td>
<td><span data-ttu-id="6e23b-175">EAPHost ermöglicht das gleichzeitige Betreiben mehrerer Supplicants, und jede Supplicant kann an mehrere Netzwerkadapter gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="6e23b-175">EAPHost allows multiple supplicants to operate simultaneously, and each supplicant can bind to multiple network adapters.</span></span> <span data-ttu-id="6e23b-176">EAPHost-Supplicants stellen eine Bindung an die Netzwerk Ebenen bereit und Steuern den Authentifizierungsprozess.</span><span class="sxs-lookup"><span data-stu-id="6e23b-176">EAPHost supplicants provide binding to the network layers and drive the authentication process.</span></span> <span data-ttu-id="6e23b-177">Supplicants enthalten die Authentifizierungs Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6e23b-177">Supplicants contain authentication configuration.</span></span> <span data-ttu-id="6e23b-178">Supplicants speichert auch den Zustand und stellt nachfolgende Verbindungssicherheit bereit.</span><span class="sxs-lookup"><span data-stu-id="6e23b-178">Supplicants also save the state and provide subsequent connection security.</span></span> <span data-ttu-id="6e23b-179">Da EAPHost nicht direkt an einen Netzwerk Mechanismus gebunden wird, ist die Erweiterbarkeit möglich.</span><span class="sxs-lookup"><span data-stu-id="6e23b-179">Because EAPHost doesn't directly bind to any network mechanism, supplicant extensibility is possible.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="6e23b-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e23b-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e23b-181">FAQ zu EAPHost-Supplicant</span><span class="sxs-lookup"><span data-stu-id="6e23b-181">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="6e23b-182">FAQ zu EAPHost-Methoden</span><span class="sxs-lookup"><span data-stu-id="6e23b-182">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="6e23b-183">EAPHost-Entwicklungs FAQs</span><span class="sxs-lookup"><span data-stu-id="6e23b-183">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

