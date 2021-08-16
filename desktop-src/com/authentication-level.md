---
title: Authentifizierungsebene
description: Die Authentifizierungsebene steuert, wie viel Sicherheit ein Client oder Server von seinem SSP möchte.
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c468408a22f1ea0c0fae67d7ce3d5f5b40f8a6342538614c1619acd40574ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311150"
---
# <a name="authentication-level"></a>Authentifizierungsebene

Die Authentifizierungsebene steuert, wie viel Sicherheit ein Client oder Server von seinem SSP möchte. Die Authentifizierungsebene wird festgelegt, indem ein entsprechender RPC C AUTHN LEVEL xxx-Wert über den \_ \_ \_ \_ *dwAuthnLevel-Parameter* an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) übergeben wird. Die Authentifizierungsebenen von Client und Server werden während des Handshakes verglichen, und die höhere Sicherheitsschutzeinstellung wird für die Verbindung verwendet.

Die verschiedenen Authentifizierungsebenen werden wie folgt beschrieben, von der niedrigsten Ebene des Sicherheitsschutzes bis zur höchsten Ebene:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC \_ C \_ AUTHN \_ LEVEL \_ NONE)
</dt> <dd>

Während der Kommunikation zwischen Client und Server wird keine Authentifizierung durchgeführt. Alle Sicherheitseinstellungen werden ignoriert. Diese Authentifizierungsebene kann nur festgelegt werden, wenn die [Authentifizierungsdienstebene](com-authentication-service-constants.md) RPC \_ C \_ AUTHN \_ NONE ist.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Standard (RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT)
</dt> <dd>

COM wählt die Authentifizierungsebene mithilfe der normalen Sicherheitsaushandlung aus. Es wird nie die Authentifizierungsebene None (Keine) verwendet.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Verbinden (RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT)
</dt> <dd>

Der normale Authentifizierungshandshake erfolgt zwischen Client und Server, und ein Sitzungsschlüssel wird eingerichtet, aber dieser Schlüssel wird nie für die Kommunikation zwischen Client und Server verwendet. Die gesamte Kommunikation nach dem Handshake ist unsicher.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Aufruf \_ (RPC-C-AUFRUF \_ AUF \_ \_ AUTHENTIFIZIERUNGSEBENE)
</dt> <dd>

Nur die Header des Anfangs jedes Aufrufs werden signiert. Die restlichen Daten, die zwischen Client und Server ausgetauscht werden, sind weder signiert noch verschlüsselt. Die meisten SSPs unterstützen diese Authentifizierungsebene nicht und werden im Hintergrund zu Packet (Paket) promotet.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paket (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT)
</dt> <dd>

Der Header jedes Pakets ist signiert, aber nicht verschlüsselt. Die Pakete selbst sind nicht signiert oder verschlüsselt.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Paketintegrität (RPC \_ \_ C-AUTHENTIFIZIERUNGSEBENE \_ \_ \_ PKT-INTEGRITÄT)
</dt> <dd>

Jedes Datenpaket wird vollständig signiert, aber nicht verschlüsselt. Da alle Daten vom Absender signiert werden, kann der Empfänger sicher sein, dass keine der Daten während der Übertragung manipuliert wurde.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Paketschutz (RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY)
</dt> <dd>

Jedes Datenpaket wird signiert und verschlüsselt. Dadurch wird die gesamte Kommunikation zwischen Client und Server geschützt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Authenticationlevel](authenticationlevel.md)
</dt> <dt>

[LegacyAuthenticationLevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




