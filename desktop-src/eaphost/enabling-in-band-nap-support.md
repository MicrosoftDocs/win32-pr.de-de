---
title: Implementieren In-Band NAP-Unterstützung für EAP-Methoden
description: Kann für EAPHost-EAP-Methoden aktiviert werden, die die Übertragung von Typlängen-Wert-Objekten (Type-Length-Value Objects, TLVs) unterstützen.
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477ad8f2ee033b3f98f9cac0e7ee34d18dc62f00dd5bd7c0e09509ad32bcfa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904276"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementieren In-Band NAP-Unterstützung für EAP-Methoden

In-Band-Nap-Unterstützung [(Network Access Protection,](/windows/desktop/NAP/network-access-protection-start-page) Netzwerkzugriffsschutz) für eine EAP-Methode kann für EAPHost-EAP-Methoden aktiviert werden, die die Übertragung von Typlängenwertobjekten (Type-Length-Value Objects, TLVs) unterstützen. Wenn die In-Band-NAP-Unterstützung aktiviert ist, werden NAP-Pakete innerhalb von EAP-Methodenpaketen transportiert.

Wenn hingegen out-of-band-NAP-Unterstützung aktiviert ist, erfolgt der NAP-SoH-Austausch (Statement [of Health)](https://go.microsoft.com/fwlink/p/?linkid=83917) über andere Mittel als interne EAP-Methodenpakete.

Alle TLVs sind herstellerspezifisch.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementieren von NAP-Unterstützung für EAP-Peermethoden

Die Implementierung der EAP-Peermethode empfängt einen TLV, der die Anforderung der Integritätsanforderung [(Statement of Health,](https://go.microsoft.com/fwlink/p/?linkid=83917) SoH) von einem EAP-Server enthält.

Die Implementierung der EAP-Peermethode übergibt dann den TLV mit dem SoH-Anforderungs-TLV wie folgt an EAPHost.

-   Die Implementierung der EAP-Peermethode gibt bei der Rückgabe von [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)den Aktionscode [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) an EAPHost zurück.
-   EAPHost ruft [**EapPeerGetResponseAttributes aus der**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) Implementierung der EAP-Peermethode auf. Die Attribute werden im Prozess übergeben.
-   Die Implementierung der EAP-Peermethode gibt den TLV zurück, der den TLV der SoH-Anforderung in [**EapPeerGetResponseAttributes enthält.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) Die Attribute werden im Prozess empfangen.

Die Implementierung der EAP-Peermethode empfängt wie folgt einen TLV mit einem SoH-TLV von EAPHost.

-   EAPHost ruft [**EapPeerSetResponseAttributes aus**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) der Implementierung der EAP-Peermethode auf. **EapPeerSetResponseAttributes** enthält einen TLV, der einen SoH-TLV enthält.
-   Die Implementierung der EAP-Peermethode sendet den SoH-TLV an den EAP-Server.
-   Die Implementierung der EAP-Peermethode empfängt einen TLV, der eine SoH-Antwort-TLV vom EAP-Server enthält.

Die Implementierung der EAP-Peermethode übergibt den TLV mit der SoH-Antwort-TLV wie folgt an EAPHost.

-   Die Implementierung der EAP-Peermethode gibt bei der Rückgabe von [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)den Aktionscode **EapPeerMethodResponseActionRespond** an EAPHost zurück.
-   EAPHost ruft [**EapPeerGetResponseAttributes aus**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) den Implementierungen der EAP-Peermethode auf. Die [**EAP \_ ATTRIBUTES-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) wird im Prozess übergeben.
-   Die Implementierung der EAP-Peermethode gibt den TLV zurück, der die SoH-Antwort TLV in [**EapPeerSetResponseAttributes enthält.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)

> [!Note]  
> Das **eapType-Member** der [**EAP \_ ATTRIBUTE-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) wird immer auf **"friEAPTLV"** festgelegt, und das **pValue-Member** wird auf das erste Byte des TLV zeigen, das die TLV-Antwort soH enthält.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementieren von NAP-Unterstützung für EAP-Servermethoden

Die Implementierung der EAP-Servermethode erstellt einen TLV, der eine SoH-Anforderungs-TLV enthält. Die Implementierung der EAP-Servermethode sendet diesen TLV mit dem SoH Request TLV an den EAP-Peer. Die Implementierung der EAP-Servermethode empfängt den TLV vom EAP-Peer.

Die Implementierung der EAP-Servermethode übergibt den TLV mit einem SoH-TLV wie folgt an EAPHost.

-   Die Implementierung der EAP-Servermethode gibt den Aktionscode **EAP \_ METHOD \_ AUTHENTICATOR RESPONSE \_ \_ RESPOND** to EAPHost on return from [**EapMethodAuthenticatorReceivePacket zurück.**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)
-   EAPHost ruft [**EapMethodAuthenticatorGetAttributes aus**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) der Implementierung der EAP-Servermethode auf.
-   Die Implementierung der EAP-Servermethode gibt den TLV mit dem SoH-TLV in [**EapMethodAuthenticatorGetAttributes zurück.**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)

Die Implementierung der EAP-Servermethode empfängt wie folgt einen TLV mit einer SoH-Antwort-TLV von EAPHost.

-   EAPHost ruft [**EapMethodAuthenticatorSetAttributes aus**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) der Implementierung der EAP-Servermethode auf.
-   Das TLV, das die SoH-Antwort TLV enthält, wird in [ **EapMethodAuthenticatorSetAttributes zurückgegeben.**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   Die Implementierung der EAP-Servermethode sendet den TLV mit dem SoH-Antwort-TLV.

> [!Note]  
> Das **eapType-Member** der [**EAP \_ ATTRIBUTE-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) wird immer auf **"friEAPTLV"** festgelegt, und das **pValue-Member** wird auf das erste Byte des TLV zeigen, das die TLV-Antwort soH enthält.

 

### <a name="messages"></a>Nachrichten

Der EAP-SoH-TLV wird verwendet, um das SoH-Protokoll für die Übertragung über eine EAP-Methode zu kapseln. Alle EAP-SoH-TLVs haben dieselbe Struktur und unterscheiden sich nur von der Nachrichten-ID und dem Datenteil der Nachricht.

Weitere Informationen finden Sie unter [Network Access Protection (NAP) Statement of Health (SoH)-Meldungen](https://go.microsoft.com/fwlink/p/?linkid=83918).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der EAP-Benutzeroberfläche](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Aktivieren Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Übertragen von Daten zwischen den Supplicant- und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 