---
title: IPSec-Konfiguration
description: Windows-Filter Plattform (WFP) ist die zugrunde liegende Plattform für die Windows-Firewall mit erweiterter Sicherheit.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948683"
---
# <a name="ipsec-configuration"></a><span data-ttu-id="6af01-103">IPSec-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="6af01-103">IPsec Configuration</span></span>

<span data-ttu-id="6af01-104">Windows-Filter Plattform (WFP) ist die zugrunde liegende Plattform für die Windows-Firewall mit erweiterter Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="6af01-104">Windows Filtering Platform (WFP) is the underlying platform for Windows Firewall with Advanced Security.</span></span> <span data-ttu-id="6af01-105">WFP wird zum Konfigurieren von Netzwerk Filterungs Regeln verwendet, die Regeln zum Sichern des Netzwerk Datenverkehrs mit IPSec einschließen.</span><span class="sxs-lookup"><span data-stu-id="6af01-105">WFP is used to configure network filtering rules, which include rules that govern securing network traffic with IPsec.</span></span> <span data-ttu-id="6af01-106">Anwendungsentwickler können IPSec direkt mithilfe der WFP-API konfigurieren, um ein präziseeres Modell zum Filtern von Netzwerk Datenverkehr zu nutzen, als das über das MMC-Snap-in (Microsoft Management Console) für die Windows-Firewall mit erweiterter Sicherheit verfügbar gemachte Modell.</span><span class="sxs-lookup"><span data-stu-id="6af01-106">Application developers may configure IPsec directly using the WFP API, in order to take advantage of a more granular network traffic filtering model than the model exposed through the Microsoft Management Console (MMC) snap-in for Windows Firewall with Advanced Security.</span></span>

## <a name="what-is-ipsec"></a><span data-ttu-id="6af01-107">Was ist IPSec?</span><span class="sxs-lookup"><span data-stu-id="6af01-107">What is IPsec</span></span>

<span data-ttu-id="6af01-108">Internet Protokoll Sicherheit (Internet Protocol Security, IPSec) ist ein Satz von Sicherheitsprotokollen, die zum Übertragen von IP-Paketen über das Internet verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-108">Internet Protocol Security (IPsec) is a set of security protocols used to transfer IP packets confidentially across the Internet.</span></span> <span data-ttu-id="6af01-109">IPSec ist für alle IPv6-Implementierungen obligatorisch und optional für IPv4.</span><span class="sxs-lookup"><span data-stu-id="6af01-109">IPsec is mandatory for all IPv6 implementations and optional for IPv4.</span></span>

<span data-ttu-id="6af01-110">Der gesicherte IP-Datenverkehr verfügt über zwei optionale IPSec-Header, die die Typen des kryptografischen Schutzes identifizieren, die auf das IP-Paket angewendet werden, und Informationen zum Decodieren des geschützten Pakets enthalten.</span><span class="sxs-lookup"><span data-stu-id="6af01-110">Secured IP traffic has two optional IPsec headers, which identify the types of cryptographic protection applied to the IP packet and include information for decoding the protected packet.</span></span>

<span data-ttu-id="6af01-111">Der Header "kapselnde Sicherheits Nutzlast (ESP)" wird für Datenschutz und Schutz gegen böswillige Änderungen verwendet, indem Authentifizierung und optionale Verschlüsselung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-111">The Encapsulating Security Payload (ESP) header is used for privacy and protection against malicious modification by performing authentication and optional encryption.</span></span> <span data-ttu-id="6af01-112">Sie kann für Datenverkehr verwendet werden, der NAT-Router (Netzwerk Adressübersetzung) durchläuft.</span><span class="sxs-lookup"><span data-stu-id="6af01-112">It can be used for traffic that traverses Network Address Translation (NAT) routers.</span></span>

<span data-ttu-id="6af01-113">Der Authentifizierungs Header (AH) wird nur zum Schutz gegen böswillige Änderungen verwendet, indem eine Authentifizierung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6af01-113">The Authentication Header (AH) is used only for protection against malicious modification by performing authentication.</span></span> <span data-ttu-id="6af01-114">Sie kann nicht für Datenverkehr verwendet werden, der NAT-Router durchläuft.</span><span class="sxs-lookup"><span data-stu-id="6af01-114">It cannot be used for traffic that traverses NAT routers.</span></span>

<span data-ttu-id="6af01-115">Weitere Informationen zu IPSec finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6af01-115">For more information on IPsec, see also:</span></span>

<dl>

<span data-ttu-id="6af01-116">[Technische Referenz zu IPSec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6af01-116">[IPsec Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))</span></span>  
</dl>

## <a name="what-is-ike"></a><span data-ttu-id="6af01-117">Was ist IKE?</span><span class="sxs-lookup"><span data-stu-id="6af01-117">What is IKE</span></span>

<span data-ttu-id="6af01-118">Internetschlüsselaustausch (IKE) ist ein Schlüsselaustausch Protokoll, das Teil des IPSec-Protokoll Satzes ist.</span><span class="sxs-lookup"><span data-stu-id="6af01-118">Internet Key Exchange (IKE) is a key exchange protocol that is part of the IPsec protocol set.</span></span> <span data-ttu-id="6af01-119">IKE wird beim Einrichten einer sicheren Verbindung verwendet und erfüllt den sicheren Austausch von geheimen Schlüsseln und anderen Schutz bezogenen Parametern, ohne dass der Benutzer eingreifen muss.</span><span class="sxs-lookup"><span data-stu-id="6af01-119">IKE is used while setting up a secure connection and accomplishes the safe exchange of secret keys and other protection-related parameters without the intervention of the user.</span></span>

<span data-ttu-id="6af01-120">Weitere Informationen zu IKE finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6af01-120">For more information on IKE, see also:</span></span>

<dl>

<span data-ttu-id="6af01-121">[Internetschlüsselaustausch](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6af01-121">[Internet Key Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))</span></span>  
</dl>

## <a name="what-is-authip"></a><span data-ttu-id="6af01-122">Was ist AuthIP?</span><span class="sxs-lookup"><span data-stu-id="6af01-122">What is AuthIP</span></span>

<span data-ttu-id="6af01-123">Authentifiziertes Internetprotokoll (AuthIP) ist ein neues Schlüsselaustausch Protokoll, das IKE wie folgt erweitert.</span><span class="sxs-lookup"><span data-stu-id="6af01-123">Authenticated Internet Protocol (AuthIP) is a new key exchange protocol that expands IKE as follows.</span></span>

<dl> <span data-ttu-id="6af01-124">Obwohl IKE nur Anmelde Informationen für die Computer Authentifizierung unterstützt, unterstützt auch AuthIP Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6af01-124">While IKE only supports computer authentication credentials, AuthIP also supports:</span></span>

-   <span data-ttu-id="6af01-125">Benutzer Anmelde Informationen: NTLM, Kerberos, Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="6af01-125">User credentials: NTLM, Kerberos, certificates.</span></span>
-   <span data-ttu-id="6af01-126">NAP-Integritäts Zertifikate (Network Access Protection, Netzwerk Zugriffsschutz)</span><span class="sxs-lookup"><span data-stu-id="6af01-126">Network Access Protection (NAP) health certificates.</span></span>
-   <span data-ttu-id="6af01-127">Anonyme Anmelde Informationen, die für die optionale Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-127">Anonymous credential, used for optional authentication.</span></span>
-   <span data-ttu-id="6af01-128">Kombination von Anmelde Informationen; beispielsweise eine Kombination aus Computer-und Benutzer-Kerberos-Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="6af01-128">Combination of credentials; for example, a combination of machine and user Kerberos credentials.</span></span>

  
<span data-ttu-id="6af01-129">AuthIP verfügt über einen Authentifizierungs-Wiederholungs Mechanismus, mit dem alle konfigurierten Authentifizierungsmethoden überprüft werden, bevor die Verbindung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6af01-129">AuthIP has an authentication-retry mechanism that verifies all configured authentication methods before failing the connection.</span></span>  
<span data-ttu-id="6af01-130">AuthIP kann mit Secure Sockets verwendet werden, um Anwendungs basierten IPSec-geschützten Datenverkehr zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="6af01-130">AuthIP can be used with secure sockets to implement application-based IPsec secured traffic.</span></span> <span data-ttu-id="6af01-131">Sie bietet:</span><span class="sxs-lookup"><span data-stu-id="6af01-131">It provides:</span></span>

-   <span data-ttu-id="6af01-132">Pro-Socket-Authentifizierung und-Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="6af01-132">Per-socket authentication and encryption.</span></span> <span data-ttu-id="6af01-133">Weitere Informationen finden Sie unter [**wsasetsocketsecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) .</span><span class="sxs-lookup"><span data-stu-id="6af01-133">See [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) for more information.</span></span>
-   <span data-ttu-id="6af01-134">Client Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="6af01-134">Client impersonation.</span></span> <span data-ttu-id="6af01-135">(IPSec nimmt die Identität des Sicherheits Kontexts an, unter dem der Socket erstellt wird.)</span><span class="sxs-lookup"><span data-stu-id="6af01-135">(IPsec impersonates the security context under which the socket is created.)</span></span>
-   <span data-ttu-id="6af01-136">Überprüfung des eingehenden und ausgehenden Peer namens.</span><span class="sxs-lookup"><span data-stu-id="6af01-136">Inbound and outbound peer name validation.</span></span> <span data-ttu-id="6af01-137">Weitere Informationen finden Sie unter [**wsasetsocketetertargetname**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) .</span><span class="sxs-lookup"><span data-stu-id="6af01-137">See [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) for more information.</span></span>

  
</dl>

<span data-ttu-id="6af01-138">Weitere Informationen zu AuthIP finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6af01-138">For more information on AuthIP, see also:</span></span>

<dl>

[<span data-ttu-id="6af01-139">AuthIP in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6af01-139">AuthIP in Windows Vista</span></span>](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a><span data-ttu-id="6af01-140">Was ist eine IPSec-Richtlinie?</span><span class="sxs-lookup"><span data-stu-id="6af01-140">What is an IPsec Policy</span></span>

<span data-ttu-id="6af01-141">Eine IPSec-Richtlinie ist ein Satz von Regeln, die bestimmen, welcher Typ von IP-Datenverkehr mit IPSec gesichert werden muss und wie dieser Datenverkehr gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6af01-141">An IPsec policy is a set of rules that determine which type of IP traffic needs to be secured using IPsec and how to secure that traffic.</span></span> <span data-ttu-id="6af01-142">Auf einem Computer ist jeweils nur eine IPSec-Richtlinie aktiv.</span><span class="sxs-lookup"><span data-stu-id="6af01-142">Only one IPsec policy is active on a computer at one time.</span></span>

<span data-ttu-id="6af01-143">Wenn Sie mehr über die Implementierung von IPSec-Richtlinien erfahren möchten, öffnen Sie das MMC-Snap-in "lokale Sicherheitsrichtlinie" (secpol. msc), drücken Sie F1, um die Hilfe anzuzeigen, und wählen Sie dann erstellen und Verwenden von IPSec-Richtlinien im Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="6af01-143">To learn more about implementing IPsec policies, open the Local Security Policy MMC snap-in (secpol.msc), press F1 to display the Help, and then select Creating and Using IPsec Policies from the table of contents.</span></span>

<span data-ttu-id="6af01-144">Weitere Informationen zu IPSec-Richtlinien finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6af01-144">For more information on IPsec policies, see also:</span></span>

<dl>

<span data-ttu-id="6af01-145">[Übersicht über IPSec-Richtlinien Konzepte](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6af01-145">[Overview of IPsec Policy Concepts](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>  
<span data-ttu-id="6af01-146">[Beschreibung einer IPSec-Richtlinie](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6af01-146">[Description of an IPsec Policy](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))</span></span>  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a><span data-ttu-id="6af01-147">Verwenden von WFP zum Konfigurieren von IPSec-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="6af01-147">How to Use WFP to Configure IPsec Policies</span></span>

<span data-ttu-id="6af01-148">Die Microsoft-Implementierung von IPSec verwendet die Windows-Filter Plattform zum Einrichten von IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="6af01-148">The Microsoft implementation of IPsec uses Windows Filtering Platform to setup IPsec policies.</span></span> <span data-ttu-id="6af01-149">IPSec-Richtlinien werden implementiert, indem auf verschiedenen WFP-Ebenen Filter wie folgt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-149">IPsec policies are implemented by adding filters at various WFP layers as follows.</span></span>

-   <span data-ttu-id="6af01-150">Fügen Sie auf der swpm \_ \_ -Schicht IKEEXT \_ V {4 \| 6}-Schichten Filter hinzu, mit denen die von den Schlüssel für die Schlüssel Erstellung (IKE/AuthIP) während des Hauptmodus (mm) verwendeten Aushandlungs Richtlinien angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-150">At the FWPM\_LAYER\_IKEEXT\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules (IKE/AuthIP) during Main Mode (MM) exchanges.</span></span> <span data-ttu-id="6af01-151">Authentifizierungsmethoden und Kryptografiealgorithmen werden auf diesen Ebenen angegeben.</span><span class="sxs-lookup"><span data-stu-id="6af01-151">Authentication methods and cryptographic algorithms are specified at these layers.</span></span>
-   <span data-ttu-id="6af01-152">Auf der \_ Ebene der \_ IPSec \_ V {4 6} auf der swpm-Ebene \| fügen Sie Filter hinzu, mit denen die von den Schlüssel für die Schlüssel Erstellung verwendeten Aushandlungs Richtlinien während des Schnellmodus (qm) und des Modus für erweiterte Modi (EM) angegeben</span><span class="sxs-lookup"><span data-stu-id="6af01-152">At the FWPM\_LAYER\_IPSEC\_V{4\|6} layers add filters that specify the negotiation policies used by the keying modules during Quick Mode (QM) and Extended Mode (EM) exchanges.</span></span> <span data-ttu-id="6af01-153">IPSec-Header (AH/ESP) und kryptografische Algorithmen werden auf diesen Ebenen angegeben.</span><span class="sxs-lookup"><span data-stu-id="6af01-153">IPsec headers (AH/ESP) and cryptographic algorithms are specified at these layers.</span></span>

    <span data-ttu-id="6af01-154">Eine Aushandlungs Richtlinie wird als Richtlinien Anbieter Kontext angegeben, der dem Filter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6af01-154">A negotiation policy is specified as a policy provider context associated with the filter.</span></span> <span data-ttu-id="6af01-155">Das Schlüssel Bindungs Modul listet die Richtlinien Anbieter Kontexte basierend auf den Datenverkehrs Merkmalen auf und ruft die Richtlinie ab, die für die Sicherheitsaus Handlung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6af01-155">The keying module enumerates the policy provider contexts based on the traffic characteristics and obtains the policy to use for the security negotiation.</span></span>

    > [!Note]  
    > <span data-ttu-id="6af01-156">Die WFP-API kann verwendet werden, um die Sicherheits Zuordnungen (SAS) direkt anzugeben und damit die Aushandlungs Richtlinie des Schlüssel Bindungs Moduls zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="6af01-156">The WFP API can be used to specify the Security Associations (SAs) directly and therefore to ignore the keying module negotiation policy.</span></span>

     

-   <span data-ttu-id="6af01-157">Auf der fwpm \_ -Schicht für \_ eingehende \_ Transport \_ v {4 \| 6} und fwpm- \_ Schicht \_ ausgehende \_ Transport \_ v {4 \| 6} werden Filter hinzugefügt, die Legenden aufrufen und bestimmen, welcher Daten Verkehrsfluss gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6af01-157">At the FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers add filters that invoke callouts and determine which traffic flow should be secured.</span></span>
-   <span data-ttu-id="6af01-158">Fügen Sie auf der Ebene des swpm \_ -Schicht-e \_ \_ \_ \_ -v \_ {4 \| 6} Filter hinzu, mit denen die Identitäts Filterung und die Richtlinie pro Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-158">At the FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers add filters that implement identity filtering and per-application policy.</span></span>

<span data-ttu-id="6af01-159">Das folgende Diagramm veranschaulicht die Interaktion der verschiedenen WFP-Komponenten in Bezug auf den IPSec-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6af01-159">The following diagram illustrates the interaction of the various WFP components, with respect to IPsec operation.</span></span>![IPSec-Konfiguration mit Windows-Filter Plattform](images/ipsec-configuration.jpg)

<span data-ttu-id="6af01-161">Nachdem IPsec konfiguriert wurde, wird es in WFP integriert und erweitert die WFP-Filterfunktionen, indem Informationen bereitgestellt werden, die als Filterbedingungen auf der Ebene der Autorisierungs Ebenen der Anwendungsschicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-161">Once IPsec is configured, it integrates with WFP and extends the WFP filtering capabilities by providing information to be used as filtering conditions at the Application Layer Enforcement (ALE) authorization layers.</span></span> <span data-ttu-id="6af01-162">IPSec stellt z. b. die Identität des Remote Benutzers und des Remote Computers bereit, die WFP auf den Ebenen "ALE Connect" und "Accept Authorization" verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="6af01-162">For example, IPsec provides the remote user and remote machine identity, which WFP exposes at the ALE connect and accept authorization layers.</span></span> <span data-ttu-id="6af01-163">Diese Informationen können für eine differenzierte Remote Identitäts Autorisierung durch eine WFP-basierte Firewall-Implementierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6af01-163">This information can be used for fine-grained remote identity authorization by a WFP-based firewall implementation.</span></span>

<span data-ttu-id="6af01-164">Im folgenden finden Sie eine Beispiel-Isolations Richtlinie, die mithilfe von IPSec implementiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="6af01-164">Below is a sample isolation policy that may be implemented using IPsec:</span></span>

-   <span data-ttu-id="6af01-165">Die Ebene " \_ \_ IKEEXT V {4 6}" der Ebene "f" \_ \| – Kerberos-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="6af01-165">FWPM\_LAYER\_IKEEXT\_V{4\|6} layers – Kerberos authentication.</span></span>
-   <span data-ttu-id="6af01-166">\_Ebene der \_ IPSec \_ V {4 \| 6} Ebenen der WPM-Ebene – AH/SHA-1.</span><span class="sxs-lookup"><span data-stu-id="6af01-166">FWPM\_LAYER\_IPSEC\_V{4\|6} layers – AH/SHA-1.</span></span>
-   <span data-ttu-id="6af01-167">WPM \_ -Schicht \_ eingehender \_ Transport \_ v {4 \| 6} und ausgehender Transport der WPM- \_ Ebene \_ \_ \_ v {4 \| 6} Ebenen-Aushandlungs Ermittlung für den gesamten Netzwerk Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="6af01-167">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6} and FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6} layers - negotiation discovery for all network traffic.</span></span>
-   <span data-ttu-id="6af01-168">Voll \_ \_ \_ \_ \_ \_ ständig authentifizierender v {4 \| 6}-Ebenen-IPSec für den gesamten Netzwerk Datenverkehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6af01-168">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6} layers - IPsec required for all network traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6af01-169">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6af01-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6af01-170">**WFP-Ebenen**</span><span class="sxs-lookup"><span data-stu-id="6af01-170">**WFP Layers**</span></span>
</dt> <dt>

[<span data-ttu-id="6af01-171">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="6af01-171">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> <dt>

[<span data-ttu-id="6af01-172">ALE Ebenen</span><span class="sxs-lookup"><span data-stu-id="6af01-172">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

<span data-ttu-id="6af01-173">**Mit der WFP-API implementierte IPSec-Richtlinien Szenarien:**</span><span class="sxs-lookup"><span data-stu-id="6af01-173">**IPsec Policy Scenarios Implemented using WFP API:**</span></span>
</dt> <dt>

[<span data-ttu-id="6af01-174">Transportmodus</span><span class="sxs-lookup"><span data-stu-id="6af01-174">Transport Mode</span></span>](regular-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="6af01-175">Transport Modus für Aushandlungs Ermittlung</span><span class="sxs-lookup"><span data-stu-id="6af01-175">Negotiation Discovery Transport Mode</span></span>](negotiation-discovery-transport-mode.md)
</dt> <dt>

[<span data-ttu-id="6af01-176">Transport Modus für die Aushandlung von Aushandlungen im Begrenzungs Modus</span><span class="sxs-lookup"><span data-stu-id="6af01-176">Negotiation Discovery Transport Mode in Boundary Mode</span></span>](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[<span data-ttu-id="6af01-177">Tunnel Modus</span><span class="sxs-lookup"><span data-stu-id="6af01-177">Tunnel Mode</span></span>](tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="6af01-178">Garantierte Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6af01-178">Guaranteed Encryption</span></span>](guaranteed-encryption.md)
</dt> <dt>

[<span data-ttu-id="6af01-179">Remote Identitäts Autorisierung</span><span class="sxs-lookup"><span data-stu-id="6af01-179">Remote Identity Authorization</span></span>](remote-identity-authorization.md)
</dt> <dt>

[<span data-ttu-id="6af01-180">Manuelle IPSec-SAS</span><span class="sxs-lookup"><span data-stu-id="6af01-180">Manual IPsec SAs</span></span>](manual-ipsec-sas.md)
</dt> <dt>

[<span data-ttu-id="6af01-181">IKE-/AuthIP-Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="6af01-181">IKE/AuthIP Exemptions</span></span>](ike-exemptions.md)
</dt> <dt>

<span data-ttu-id="6af01-182">**IPSec-Lösungen:**</span><span class="sxs-lookup"><span data-stu-id="6af01-182">**IPsec Solutions:**</span></span>
</dt> <dt>

<span data-ttu-id="6af01-183">[Server-und Domänen Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6af01-183">[Server and Domain Isolation](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))</span></span>
</dt> </dl>

 

 