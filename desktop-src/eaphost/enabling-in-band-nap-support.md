---
title: Implementieren In-Band NAP-Unterstützung für EAP-Methoden
description: Kann für EAPHost-EAP-Methoden aktiviert werden, die die Übertragung von Typ-Length-Value-Objekten (TLVS) unterstützen.
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734616"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>Implementieren In-Band NAP-Unterstützung für EAP-Methoden

Die Unterstützung für den in-Band- [Netzwerk Zugriffsschutz (Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) , NAP) für eine EAP-Methode kann für EAPHost-EAP-Methoden aktiviert werden, die die Übertragung von TLVS (Type-Value Objects) unterstützen. Wenn die in-Band-NAP-Unterstützung aktiviert ist, werden NAP-Pakete in EAP-Methoden Paketen transportiert.

Wenn die Out-of-Band-NAP-Unterstützung aktiviert ist, wird der NAP-Austausch ( [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) , SoH) im Gegensatz zu internen EAP-Methoden Paketen ausgeführt.

Alle TLVS sind Anbieter spezifisch.

## <a name="implementing-nap-support-on-eap-peer-methods"></a>Implementieren der NAP-Unterstützung für EAP-Peer Methoden

Die Implementierung der EAP-Peer Methode erhält ein TLV, das das [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH)-Anforderungs-TLV von einem EAP-Server enthält.

Die Implementierung der EAP-Peer Methode übergibt dann den TLV mit der SoH-Anforderung TLV wie folgt an EAPHost.

-   Die EAP-Peer Methoden Implementierung gibt den Aktions Code [**eappeermethodresponseaction**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) Response bei Rückgabe von [**eappeerprocessrequestpacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)an EAPHost zurück.
-   EAPHost ruft [**eappeergetresponlattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) aus der EAP-Peer Methoden Implementierung auf. Die Attribute werden im Prozess übermittelt.
-   Die Implementierung der EAP-Peer Methode gibt das TLV mit dem SoH-Anforderungs-TLV in [**eappeergetresponmenattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)zurück. Die Attribute werden im Prozess empfangen.

Die Implementierung der EAP-Peer Methode erhält wie folgt ein TLV mit einem SoH-TLV von EAPHost.

-   EAPHost ruft [**eappeersettresponmenattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) aus der Implementierung der EAP-Peer Methode auf. **Eappeerltresponlattribute** enthält ein TLV, das ein SoH-TLV enthält.
-   Die Implementierung der EAP-Peer Methode sendet den SoH-TLV an den EAP-Server.
-   Die Implementierung der EAP-Peer Methode erhält einen TLV, der einen SoH-Antwort-TLV vom EAP-Server enthält.

Die Implementierung der EAP-Peer Methode übergibt das TLV mit der SoH-Antwort TLV wie folgt an EAPHost.

-   Die EAP-Peer Methoden Implementierung gibt den Aktions Code **eappeermethodresponseaction** Response bei Rückgabe von [**eappeerprocessrequestpacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)an EAPHost zurück.
-   EAPHost ruft [**eappeergetresponlattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) aus den Implementierungen der EAP-Peer Methode auf. Die [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) Struktur wird im Prozess übermittelt.
-   Die Implementierung der EAP-Peer Methode gibt das TLV zurück, das den SoH-Antwort-TLV in [**eappeerltresponmenattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)enthält.

> [!Note]  
> Der **eaptype** -Member der [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) Struktur wird immer auf **eateaptlv** festgelegt, und der **pValue** -Member verweist auf das erste Byte des TLV, das die SoH-Antwort TLV enthält.

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>Implementieren der NAP-Unterstützung für EAP-Server Methoden

Die Implementierung der EAP-Server Methode erstellt ein TLV mit einem SoH-Anforderungs-TLV. Die Implementierung der EAP-Server Methode sendet dieses TLV mit der SoH-Anforderungs-TLV an den EAP-Peer. Die Implementierung der EAP-Server Methode empfängt den TLV vom EAP-Peer.

Die Implementierung der EAP-Server Methode übergibt das TLV mit einem SoH-TLV wie folgt an EAPHost.

-   Die EAP-Server Methoden Implementierung gibt den Aktions Code zurück, der die **EAP- \_ Methoden- \_ Authenticator- \_ Antwort \_** auf EAPHost bei Rückgabe von [**eapmethodauthenticatorreceivepacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)antwortet.
-   EAPHost ruft [**eapmethodauthenticatorgetattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) aus der Implementierung der EAP-Server Methode auf.
-   Die Implementierung der EAP-Server Methode gibt das TLV mit dem SoH-TLV in [**eapmethodauthenticatorgetattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)zurück.

Die Implementierung der EAP-Server Methode erhält wie folgt ein TLV mit einem SoH-Antwort-TLV von EAPHost.

-   EAPHost ruft [**eapmethodauthenticatorstattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) aus der Implementierung der EAP-Server Methode auf.
-   Der TLV, der die SoH-Antwort "TLV" enthält, wird in [ **eapmethodauthentionor\tattributes** zurückgegeben.](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   Die Implementierung der EAP-Server Methode sendet den TLV, der die SoH-Antwort TLV enthält.

> [!Note]  
> Der **eaptype** -Member der [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) Struktur wird immer auf **eateaptlv** festgelegt, und der **pValue** -Member verweist auf das erste Byte des TLV, das die SoH-Antwort TLV enthält.

 

### <a name="messages"></a>Meldungen

Der EAP SoH-TLV wird verwendet, um das SoH-Protokoll für die Übertragung über eine EAP-Methode zu kapseln. Alle EAP SoH-TLVS haben dieselbe Struktur und unterscheiden sich nur hinsichtlich der Nachrichten-ID und des Daten Teils der Nachricht.

Weitere Informationen finden Sie unter [Network Access Protection (NAP)-SoH (Statement of Health)-Nachrichten](https://go.microsoft.com/fwlink/p/?linkid=83918).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Benutzeroberfläche der EAP-Methode](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[Aktivieren von Gruppenrichtlinie](enabling-group-policy.md)
</dt> <dt>

[Implementieren der NAP-Unterstützung für EAP-Methoden](implementing-nap-for-eap-methods.md)
</dt> <dt>

[Übertragen von Daten zwischen den Supplicant-und EAP-Methoden](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost-Supplicants](eaphost-supplicants.md)
</dt> </dl>

 

 