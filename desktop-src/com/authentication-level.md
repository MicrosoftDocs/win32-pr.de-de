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
# <a name="authentication-level"></a>Authentifizierungs Ebene

Mit der Authentifizierungs Ebene wird gesteuert, wie viel Sicherheit ein Client oder Server von seinem SSP aus möchte. Die Authentifizierungs Ebene wird festgelegt, indem ein entsprechender Wert der RPC- \_ C- \_ authn- \_ Ebene \_ xxx an [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) über den *dwauthnlevel* -Parameter übergeben wird. Die Authentifizierungs Ebenen von Client und Server werden während des Handshakes verglichen, und für die Verbindung wird die Sicherheitsschutz Einstellung auf höherer Ebene verwendet.

Die verschiedenen Authentifizierungs Ebenen werden wie folgt beschrieben: vom niedrigsten Sicherheitsschutz zum höchsten:

<dl> <dt>

<span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC- \_ C- \_ authn- \_ Ebene \_ None)
</dt> <dd>

Bei der Kommunikation zwischen Client und Server wird keine Authentifizierung durchgeführt. Alle Sicherheitseinstellungen werden ignoriert. Diese Authentifizierungs Ebene kann nur festgelegt werden, wenn die [Authentifizierungsdienst Ebene](com-authentication-service-constants.md) RPC \_ C \_ authn \_ None ist.

</dd> <dt>

<span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Standard (Standardwert für RPC- \_ C- \_ authn- \_ Ebene \_ )
</dt> <dd>

COM wählt die Authentifizierungs Ebene aus, indem er die normale Aushandlung der Sicherheits Pauschale verwendet. Es wird nie eine Authentifizierungs Ebene von "None" ausgewählt.

</dd> <dt>

<span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Verbinden (RPC- \_ C- \_ authn- \_ Ebene \_ Connect)
</dt> <dd>

Der normale Authentifizierungs Hand Shake erfolgt zwischen Client und Server, und es wird ein Sitzungsschlüssel eingerichtet, aber dieser Schlüssel wird nie für die Kommunikation zwischen dem Client und dem Server verwendet. Die gesamte Kommunikation nach dem Hand Shake ist nicht sicher.

</dd> <dt>

<span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Aufruf (RPC- \_ C- \_ authn-Ebene- \_ \_ Aufruf)
</dt> <dd>

Nur die Header des Beginns der einzelnen Aufrufe werden signiert. Der Rest der zwischen Client und Server ausgetauschten Daten ist weder signiert noch verschlüsselt. Die meisten SSPs unterstützen diese Authentifizierungs Ebene nicht und Stufen Sie automatisch auf das Paket herauf.

</dd> <dt>

<span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Paket (RPC- \_ C- \_ authn- \_ Ebene \_ Pkt)
</dt> <dd>

Der Header der einzelnen Pakete ist signiert, aber nicht verschlüsselt. Die Pakete selbst sind nicht signiert oder verschlüsselt.

</dd> <dt>

<span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Paketintegrität (Pkt-Integrität der RPC- \_ C- \_ authn- \_ Ebene \_ \_ )
</dt> <dd>

Jedes Datenpaket ist vollständig signiert, aber nicht verschlüsselt. Da alle Daten vom Absender signiert werden, kann der Empfänger sicher sein, dass während der Übertragung keine Daten manipuliert wurden.

</dd> <dt>

<span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Paket Datenschutz (RPC- \_ C- \_ authn- \_ Ebene \_ Pkt- \_ Datenschutz)
</dt> <dd>

Jedes Datenpaket wird signiert und verschlüsselt. Dadurch wird die gesamte Kommunikation zwischen dem Client und dem Server geschützt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AuthenticationLevel](authenticationlevel.md)
</dt> <dt>

[Legacyauthenticationlevel](legacyauthenticationlevel.md)
</dt> </dl>

 

 




