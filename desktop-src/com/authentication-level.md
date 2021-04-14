---
title: Authentifizierungs Ebene
description: Mit der Authentifizierungs Ebene wird gesteuert, wie viel Sicherheit ein Client oder Server von seinem SSP aus möchte.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311508"
---
# <a name="authentication-level"></a><span data-ttu-id="fb13a-103">Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="fb13a-103">Authentication Level</span></span>

<span data-ttu-id="fb13a-104">Mit der Authentifizierungs Ebene wird gesteuert, wie viel Sicherheit ein Client oder Server von seinem SSP aus möchte.</span><span class="sxs-lookup"><span data-stu-id="fb13a-104">The authentication level controls how much security a client or server wants from its SSP.</span></span> <span data-ttu-id="fb13a-105">Die Authentifizierungs Ebene wird festgelegt, indem ein entsprechender Wert der RPC- \_ C- \_ authn- \_ Ebene \_ xxx an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) über den *dwauthnlevel* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb13a-105">The authentication level is set by passing an appropriate RPC\_C\_AUTHN\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwAuthnLevel* parameter.</span></span> <span data-ttu-id="fb13a-106">Die Authentifizierungs Ebenen von Client und Server werden während des Handshakes verglichen, und für die Verbindung wird die Sicherheitsschutz Einstellung auf höherer Ebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb13a-106">The authentication levels from the client and server are compared during the handshake, and the higher level security protection setting is used for the connection.</span></span>

<span data-ttu-id="fb13a-107">Die verschiedenen Authentifizierungs Ebenen werden wie folgt beschrieben: vom niedrigsten Sicherheitsschutz zum höchsten:</span><span class="sxs-lookup"><span data-stu-id="fb13a-107">The different authentication levels are described as follows, from lowest level security protection to highest:</span></span>

<dl> <dt>

<span data-ttu-id="fb13a-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC- \_ C- \_ authn- \_ Ebene \_ None)</span><span class="sxs-lookup"><span data-stu-id="fb13a-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC\_C\_AUTHN\_LEVEL\_NONE)</span></span>
</dt> <dd>

<span data-ttu-id="fb13a-109">Bei der Kommunikation zwischen Client und Server wird keine Authentifizierung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-109">No authentication is performed during the communication between client and server.</span></span> <span data-ttu-id="fb13a-110">Alle Sicherheitseinstellungen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fb13a-110">All security settings are ignored.</span></span> <span data-ttu-id="fb13a-111">Diese Authentifizierungs Ebene kann nur festgelegt werden, wenn die [Authentifizierungsdienst Ebene](com-authentication-service-constants.md) RPC \_ C \_ authn \_ None ist.</span><span class="sxs-lookup"><span data-stu-id="fb13a-111">This authentication level can be set only if the [authentication service level](com-authentication-service-constants.md) is RPC\_C\_AUTHN\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="fb13a-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Standard (Standardwert für RPC- \_ C- \_ authn- \_ Ebene \_ )</span><span class="sxs-lookup"><span data-stu-id="fb13a-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC\_C\_AUTHN\_LEVEL\_DEFAULT)</span></span>
</dt> <dd>

<span data-ttu-id="fb13a-113">COM wählt die Authentifizierungs Ebene aus, indem er die normale Aushandlung der Sicherheits Pauschale verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb13a-113">COM chooses the authentication level by using its normal security blanket negotiation.</span></span> <span data-ttu-id="fb13a-114">Es wird nie eine Authentifizierungs Ebene von "None" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-114">It will never choose an authentication level of None.</span></span>

</dd> <dt>

<span data-ttu-id="fb13a-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Verbinden (RPC- \_ C- \_ authn- \_ Ebene \_ Connect)</span><span class="sxs-lookup"><span data-stu-id="fb13a-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT)</span></span>
</dt> <dd>

<span data-ttu-id="fb13a-116">Der normale Authentifizierungs Hand Shake erfolgt zwischen Client und Server, und es wird ein Sitzungsschlüssel eingerichtet, aber dieser Schlüssel wird nie für die Kommunikation zwischen dem Client und dem Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb13a-116">The normal authentication handshake occurs between the client and server, and a session key is established but that key is never used for communication between the client and server.</span></span> <span data-ttu-id="fb13a-117">Die gesamte Kommunikation nach dem Hand Shake ist nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="fb13a-117">All communication after the handshake is nonsecure.</span></span>

</dd> <dt>

<span data-ttu-id="fb13a-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Aufruf (RPC- \_ C- \_ authn-Ebene- \_ \_ Aufruf)</span><span class="sxs-lookup"><span data-stu-id="fb13a-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC\_C\_AUTHN\_LEVEL\_CALL)</span></span>
</dt> <dd>

<span data-ttu-id="fb13a-119">Nur die Header des Beginns der einzelnen Aufrufe werden signiert.</span><span class="sxs-lookup"><span data-stu-id="fb13a-119">Only the headers of the beginning of each call are signed.</span></span> <span data-ttu-id="fb13a-120">Der Rest der zwischen Client und Server ausgetauschten Daten ist weder signiert noch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-120">The rest of the data exchanged between the client and server is neither signed nor encrypted.</span></span> <span data-ttu-id="fb13a-121">Die meisten SSPs unterstützen diese Authentifizierungs Ebene nicht und Stufen Sie automatisch auf das Paket herauf.</span><span class="sxs-lookup"><span data-stu-id="fb13a-121">Most SSPs do not support this authentication level and silently promote it to Packet.</span></span>

</dd> <dt>

<span data-ttu-id="fb13a-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paket (RPC- \_ C- \_ authn- \_ Ebene \_ Pkt)</span><span class="sxs-lookup"><span data-stu-id="fb13a-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC\_C\_AUTHN\_LEVEL\_PKT)</span></span>
</dt> <dd>

<span data-ttu-id="fb13a-123">Der Header der einzelnen Pakete ist signiert, aber nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-123">The header of each packet is signed but not encrypted.</span></span> <span data-ttu-id="fb13a-124">Die Pakete selbst sind nicht signiert oder verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-124">The packets themselves are not signed or encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="fb13a-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Paketintegrität (Pkt-Integrität der RPC- \_ C- \_ authn- \_ Ebene \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="fb13a-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Packet Integrity (RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY)</span></span>
</dt> <dd>

<span data-ttu-id="fb13a-126">Jedes Datenpaket ist vollständig signiert, aber nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-126">Each packet of data is signed in its entirety but is not encrypted.</span></span> <span data-ttu-id="fb13a-127">Da alle Daten vom Absender signiert werden, kann der Empfänger sicher sein, dass während der Übertragung keine Daten manipuliert wurden.</span><span class="sxs-lookup"><span data-stu-id="fb13a-127">Because all of the data is signed by the sender, the recipient can be certain that none of the data has been tampered with during transit.</span></span>

</dd> <dt>

<span data-ttu-id="fb13a-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Paket Datenschutz (RPC- \_ C- \_ authn- \_ Ebene \_ Pkt- \_ Datenschutz)</span><span class="sxs-lookup"><span data-stu-id="fb13a-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Packet Privacy (RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY)</span></span>
</dt> <dd>

<span data-ttu-id="fb13a-129">Jedes Datenpaket wird signiert und verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-129">Each data packet is signed and encrypted.</span></span> <span data-ttu-id="fb13a-130">Dadurch wird die gesamte Kommunikation zwischen dem Client und dem Server geschützt.</span><span class="sxs-lookup"><span data-stu-id="fb13a-130">This helps protect the entire communication between the client and server.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="fb13a-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb13a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb13a-132">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="fb13a-132">AuthenticationLevel</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="fb13a-133">Legacyauthenticationlevel</span><span class="sxs-lookup"><span data-stu-id="fb13a-133">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
</dt> </dl>

 

 




