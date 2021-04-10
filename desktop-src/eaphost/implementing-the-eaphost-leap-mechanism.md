---
title: Implementieren des EAPHost-Schaltmechanismus
description: Beschreibt den EAPHost-Mechanismus, der Drittanbietern das Schreiben von Lightweight Extensible Authentication Protocol (Sprung)-Modulen für Windows ermöglicht.
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc50cda8d32cc26dd81af5733345deebb579c792
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102507"
---
# <a name="implementing-the-eaphost-leap-mechanism"></a>Implementieren des EAPHost-Schaltmechanismus

In diesem Thema wird der EAPHost-Mechanismus beschrieben, der Drittanbietern das Schreiben von Lightweight Extensible Authentication Protocol (Sprung)-Modulen für Windows ermöglicht. "Springen" ist eine ältere, von Cisco erstellte Authentifizierungsmethode gemäß [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016). Weitere Informationen zu Schalt Vorschauen finden Sie unter [Cisco LEAP Q&A](https://go.microsoft.com/fwlink/p/?linkid=84018).

## <a name="eaphost-authentication-process"></a>EAPHost-Authentifizierungsprozess

Der reguläre EAPHost-Authentifizierungs Vorgang erfolgt wie folgt:

-   Der Authentifikator sendet eine Anforderung zum Authentifizieren des Peers. Die Anwendung ruft z. b. [**eaphostpeer erbeginsession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) mit der Konfiguration und den Benutzerdaten von EAPHost auf.
-   Der Peer sendet ein Antwortpaket als Antwort auf eine gültige Anforderung. Ein erfolgreicher-Rückruf gibt z. b. ein Sitzungs Handle des **EAP- \_ Sitzungs \_ Handles** zurück.
-   Der Authentifikator sendet ein zusätzliches Anforderungspaket, und der Peer antwortet mit einer Antwort. Beispielsweise ruft die Anwendung [**eaphostpeergetsendpacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) auf, um von EAPHost während der gesamten Sitzung empfangene EAP-Pakete abzurufen. Jedes Paket wird durch einen [**eaphostpeer-processreceivedpacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket)-Code verarbeitet.
-   [**Eaphostpeer-processreceivedpacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) gibt immer einen Aktions Code zurück. Der Supplicant muss dann die Funktion aufzurufen, die dem Aktions Code entspricht.
-   Die Abfolge von Anforderungen und Antworten wird so lange wie nötig fortgesetzt. Beispielsweise kann die Anwendung [**eaphostpeergetresponseattribute**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) aufrufen, um verfügbare EAP-Attribute anzufordern, und der Peer antwortet mit [**eaphostpeersetresponseattributs**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) , um Sie zurückzugeben.
-   Nach einer ersten Anforderung kann eine neue Anforderung nicht gesendet werden, bis eine gültige Antwort empfangen wird.
-   Die Konversation wird fortgesetzt, bis der Authentifikator den Peer nicht authentifizieren kann. in diesem Fall muss die Authenticator-Implementierung einen EAP-Fehler übertragen. Beispielsweise würde eine nicht zulässige Antwort auf eine oder mehrere Anforderungen bewirken, dass der Authentifikator einen Code 4-EAP-Fehler übermittelt.
-   Alternativ kann die Authentifizierungs Konversation fortgesetzt werden, bis der Authentifikator ermittelt, dass eine erfolgreiche Authentifizierung erfolgt ist. in diesem Fall muss der Authentifikator einen EAP-Erfolg übertragen (Code 3).
-   Unabhängig davon, ob das Ergebnis erfolgreich oder fehlerhaft ist, ruft die Anwendung [**eaphostpeer Server EndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) auf, um die Sitzung zu beenden. Bei einem Fehler kann die erneute Authentifizierung versucht werden, indem eine andere Sitzung mit EAPHost geöffnet und entweder dieselbe oder eine neue Identität bereitgestellt wird.

### <a name="leap-authentication-process"></a>Schalt Authentifizierungsprozess

Der Vorgang für die Sprung Authentifizierung unterscheidet sich vom regulären EAPHost-Authentifizierungsprozess wie folgt:

-   Die EAP-Authentifizierung wird vom Server (Authentifikator) initiiert. Der Sprung wird hingegen vom Client (Peer) initiiert.
    -   Daher müssen Sie beim Schreiben eines Sprung Moduls immer sicherstellen, dass das Challenge Request-Paket von der Peer-Methode und die EAP-Antwort vom EAP-Server immer die gleiche Paket-ID wie das EAP-Erfolgs Paket vom Server aufweisen muss.

    <!-- -->

    -   Im Gegensatz dazu verfügen EAPHost-Anforderungs-und-Antwort-und Erfolgs Pakete in der Regel über unterschiedliche IDs.
        > [!Note]  
        > Jede EAP-Anforderung verfügt über ein typffeld, das angibt, was angefordert wird. Wie bei dem Anforderungspaket enthält jedes EAP-Antwortpaket ein Type-Feld, das dem type-Feld der Anforderung entspricht. Beispiele hierfür sind Identitäts Anforderungs-und Anforderungs Anforderungs Pakete.

         

-   Bei einem Fehler mit EAPHost kann die erneute Authentifizierung versucht werden, indem eine andere Sitzung mit EAPHost geöffnet und entweder dieselbe Identität oder eine neue Identität bereitgestellt wird.

### <a name="leap-authenticator-method-implementation"></a>Implementierung der Sprung Authenticator-Methode

Wenn Sie eine Schalt-Authenticator-Methode entwickeln, stellen Sie Folgendes sicher:

-   Bei der Ausführung der ersten Authentifizierungs Phase (Peer-Authentifizierung) muss der Vorgang zum Senden von Authentifizierungsmethoden für den [**EAP- \_ \_ methodenauthentifikator den \_ Antwort \_ Code der EAP-Methode**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) zurückgeben. Wenn [**eapmethodauthenticatorsendpacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) aufgerufen wird, sollte ein gültiges [**eappacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket) mit einem EAP-Code von [**eapcodesuccess**](/windows/win32/api/eapmethodtypes/ne-eapmethodtypes-eapcode)zurückgegeben werden.
-   Die Schalt-Authenticator-Methoden des EAP-Methoden-Authentifikators sollten den Aktions Code des [**\_ \_ \_ Antwort \_ Ergebnisses der EAP-Methode**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) zurückgeben, wenn die erste Phase der
-   Beim Aufruf von [**eapmethodauthenticatorsendpacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) muss das abschließende Authentifizierungs Antwortpaket mit dem Antwort Ergebnis Aktions Code des [**EAP- \_ Methoden \_ \_ \_ Authentifikators**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) zurückgegeben werden. Anschließend muss in nachfolgenden Aufrufen von [**eapmethodauthenticatorgetresult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) das **EAP- \_ Sitzungs \_ handle** zurückgegeben werden, um die authentifizierte Sitzung zu identifizieren.
-   

### <a name="leap-peer-method-implementation"></a>Implementierung der Sprung Peer Methode

Wenn Sie eine Schalt Peer Methode entwickeln, stellen Sie Folgendes sicher:

-   Schalt Peer Methoden sollten den [**eappeermethodresponseaction Send**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) -Aktions Code zurückgeben, nachdem die erste Phase der Authentifizierung (Peer Authentifizierung) erfolgreich war.
-   Schalt Peer Methoden sollten den [**eappeermethodresponseaction result**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) -Aktions Code zurückgeben, nachdem die 2. Authentifizierungs Phase erfolgreich war.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Rückruf Sequenz](about-eaphost-call-sequences.md)
</dt> <dt>

[Verwenden von EAPHost](using-eap-host.md)
</dt> </dl>

 

 




