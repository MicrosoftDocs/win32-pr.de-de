---
title: Informationen über EAP
description: Extensible Authentication Protocol (EAP), ein Standard, der von vielen Microsoft-Netzwerkkomponenten unterstützt wird.
ms.assetid: a2f41808-4316-431a-ab58-f1e25d3c61f6
keywords:
- Extensible Authentication-Protokoll, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631299c9e57a233794dde8bf205d98b8c91b76c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391133"
---
# <a name="about-eap"></a><span data-ttu-id="b40ac-104">Informationen über EAP</span><span class="sxs-lookup"><span data-stu-id="b40ac-104">About EAP</span></span>

<span data-ttu-id="b40ac-105">In diesem Thema wird das Extensible Authentication Protocol (EAP) beschrieben, ein Standard, der von vielen Microsoft-Netzwerkkomponenten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b40ac-105">This topic describes Extensible Authentication Protocol (EAP), a standard supported by many Microsoft networking components.</span></span>

## <a name="eap-components"></a><span data-ttu-id="b40ac-106">EAP-Komponenten</span><span class="sxs-lookup"><span data-stu-id="b40ac-106">EAP Components</span></span>

<span data-ttu-id="b40ac-107">EAP ist für den Schutz der Sicherheit von drahtlosen LANs (802.1 x), verkabelten LANs und Einwähl-und VPN-Verbindungen (Virtual Private Networks, VPNs) entscheidend.</span><span class="sxs-lookup"><span data-stu-id="b40ac-107">EAP is crucial for protecting the security of wireless (802.1X) LANs, wired LANs, and dial-up and Virtual Private Networks (VPNs).</span></span>

<span data-ttu-id="b40ac-108">Die folgenden Komponenten unterstützen das EAP-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="b40ac-108">The following components support the EAP protocol.</span></span>

-   <span data-ttu-id="b40ac-109">Microsoft-Remote Zugriffs Clients und-Server für DFÜ und VPN (PPTP und L2TP/IPSec) implementieren EAP als Erweiterung für PPP.</span><span class="sxs-lookup"><span data-stu-id="b40ac-109">Microsoft Remote Access Clients and Servers for both dial-up and VPN (PPTP and L2TP/IPSec) implement EAP as an extension to PPP.</span></span> <span data-ttu-id="b40ac-110">Weitere Informationen finden Sie unter [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span><span class="sxs-lookup"><span data-stu-id="b40ac-110">For more information, see [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063).</span></span>
-   <span data-ttu-id="b40ac-111">Microsoft IEEE 802.1 x-kompatible drahtlose und verkabelte LAN-Clients implementieren EAP gemäß der Definition im IEEE 802.1 x-Entwurfs Standard.</span><span class="sxs-lookup"><span data-stu-id="b40ac-111">Microsoft IEEE 802.1X compatible wireless and wired LAN clients implement EAP as defined in the IEEE 802.1X draft standard.</span></span>
-   <span data-ttu-id="b40ac-112">Microsoft RADIUS Server (Internet Authentication Service, IAS) implementiert EAP, wie in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055)definiert.</span><span class="sxs-lookup"><span data-stu-id="b40ac-112">Microsoft RADIUS server, called Internet Authentication Service (IAS) implement EAP as defined in [RFC 2865](https://go.microsoft.com/fwlink/p/?linkid=84055).</span></span>

<span data-ttu-id="b40ac-113">Alle oben genannten Komponenten unterstützen diese erweiterbare Architektur über das Microsoft Windows Software Development Kit (SDK), sodass Sie Authentifizierungs Module von Drittanbietern integrieren können.</span><span class="sxs-lookup"><span data-stu-id="b40ac-113">All of the above components support this extensible architecture through the Microsoft Windows Software Development Kit (SDK), making it possible to integrate third-party authentication modules.</span></span> <span data-ttu-id="b40ac-114">Dieser erweiterbare Mechanismus kann verwendet werden, um Token-Karten, Kerberos-, Public Key-und S/Key-Authentifizierungsprotokolle zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b40ac-114">This extensible mechanism can be used to support token cards, Kerberos, Public Key, and S/Key authentication protocols.</span></span>

## <a name="protected-extensible-authentication-protocol"></a><span data-ttu-id="b40ac-115">Geschütztes erweiterbares Authentifizierungsprotokoll</span><span class="sxs-lookup"><span data-stu-id="b40ac-115">Protected Extensible Authentication Protocol</span></span>

<span data-ttu-id="b40ac-116">Zusätzlich zu EAP unterstützen auch die Wireless-Implementierung (802.1 x) und der RADIUS-Server einen neuen Standard namens Protected EAP (PEAP).</span><span class="sxs-lookup"><span data-stu-id="b40ac-116">In addition to EAP, the wireless (802.1X) implementation and RADIUS server also support an emerging standard called Protected EAP (PEAP).</span></span>

<span data-ttu-id="b40ac-117">PEAP bietet wie folgt verschiedene wichtige Dienste für andere EAP-Authentifizierungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="b40ac-117">PEAP provides several key services to other EAP authentication protocols, as follows.</span></span>

-   <span data-ttu-id="b40ac-118">PEAP verschlüsselt EAP-Pakete anderer EAP-Authentifizierungsprotokolle mithilfe von Transport Layer Security (TLS), einer Secure Socket Layer (SSL)-basierten Technologie.</span><span class="sxs-lookup"><span data-stu-id="b40ac-118">PEAP encrypts EAP packets of other EAP authentication protocols using Transport Layer Security (TLS), a Secure Socket Layer (SSL) based technology.</span></span> <span data-ttu-id="b40ac-119">Weitere Informationen finden Sie unter [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span><span class="sxs-lookup"><span data-stu-id="b40ac-119">For more information, see [RFC 2716](https://go.microsoft.com/fwlink/p/?linkid=84050).</span></span>
-   <span data-ttu-id="b40ac-120">Der Server wird von der Serverseite mithilfe eines Serverzertifikats mit RADIUS-Server authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="b40ac-120">PEAP authenticates the server-side using a Server Certificate, with RADIUS server.</span></span>
-   <span data-ttu-id="b40ac-121">Peer-App bietet eine schnelle erneute Authentifizierung, die effizientes Roaming zwischen drahtlosen Geräten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b40ac-121">PEAP offers fast re-authentication capability that supports efficient roaming between wireless devices.</span></span>
-   <span data-ttu-id="b40ac-122">PEAP verwaltet die Fragmentierung und neuassembly von EAP-Paketen.</span><span class="sxs-lookup"><span data-stu-id="b40ac-122">PEAP manages the fragmentation and re-assembly of EAP packets.</span></span>
-   <span data-ttu-id="b40ac-123">Peer generiert Schlüssel zum Verschlüsseln von drahtlosem Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="b40ac-123">PEAP generates keys used for encrypting wireless traffic.</span></span>

<span data-ttu-id="b40ac-124">PEAP vereinfacht das Schreiben eines EAP-Protokolls erheblich, da der Programmierer diese Probleme nicht mehr beheben muss.</span><span class="sxs-lookup"><span data-stu-id="b40ac-124">PEAP makes it much easier to write an EAP protocol because the programmer no longer has to address these issues.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b40ac-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b40ac-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b40ac-126">Informationen zu EAP und EAPHost</span><span class="sxs-lookup"><span data-stu-id="b40ac-126">About EAP and EAPHost</span></span>](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 




