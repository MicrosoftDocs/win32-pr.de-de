---
title: Authentifizierungsmethode-API-Rückruf Sequenz
description: Erfahren Sie mehr über die API-Rückruf Sequenz der Authenticator-Methode. Sehen Sie sich eine Liste an, die die Abfolge von Aufrufen von EAPHost in einer EAP Authenticator-Methode veranschaulicht.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bb5c7d64bfe6e38ebb97550dc76fe8ffcae8176
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391019"
---
# <a name="authenticator-method-api-call-sequence"></a>Authentifizierungsmethode-API-Rückruf Sequenz

In diesem Thema wird die spezifische Rückruf Sequenz für die Authenticator-Methoden-API bereitstellt. Bei einer typischen EAP-Authentifizierungs Sitzung führt EAPHost eine Reihe von Aufrufen für eine EAP-Methode aus, die die EAPHost-Authenticator-Methoden-APIs implementiert.

In der folgenden Liste wird die Abfolge von Aufrufen von EAPHost in einer EAP Authenticator-Methode veranschaulicht.

-   Der EAP-Authentifikator lädt zuerst die EAP-Methoden-dll, die für die jeweilige Authentifizierung auf einem Netzwerk Richtlinien Server (NPS) oder einem anderen Authentifizierungsserver verwendet wird.
-   Ruft [**eapauthenticatorgetinfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) für die Methode mit einer aufgefüllten [**EAP- \_ Typstruktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) auf, um eine Liste von Zeigern auf Funktionen zu erhalten, die für die dll implementiert wurden. Bei nachfolgenden Funktionsaufrufen durch die Authenticator-Methoden (Server) wird davon ausgegangen, dass Sie für die dll implementiert werden.
-   Ruft " [**eapauthenticatorinitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) " auf, um die EAP-Methoden Bibliothek anzuweisen, mindestens eine Authentifizierungs Sitzung mithilfe dieser Authenticator-Methode vorzubereiten.
-   Ruft " [**eapmethodauthenti| orbeginsession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) " auf, um eine eindeutige Authentifizierungs Sitzung einzurichten.
-   Die folgenden Schritte werden wiederholt, bis [**eapmethodauthentianreceivepacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) anzeigt, dass ein Authentifizierungs Ergebnis verfügbar ist.
    -   Ruft [**eapmethodauthentisinorsendpacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) mit einem Zeiger auf ein Anforderungspaket auf, das an den Supplicant übergeben werden soll.
    -   Ruft [**eapmethodauthenticket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) auf, um das vom Supplicant gesendete Antwortpaket abzurufen. Diese Funktion gibt einen **\_ \_ \_ Antwort \_ Aktions Code für den EAP-Methoden Authentifikator** zurück, der die nächste Aktion angibt, die der Authentifikator in der EAP-Authentifizierungs Sitzung ausführen muss.
    -   Wenn der Aktions Code die [EAP- \_ Methoden- \_ AUTHENTICATOR- \_ Antwort \_ antwortet](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action), gibt dies an, dass die EAP-Methode über Attribute verfügt, die der Authentifikator abrufen und an die Peer Methode übergeben kann. Der Authentifikator ruft [**eapmethodauthenticatorgetattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) auf, um die verschiedenen EAP-Authentifizierungs Attribute von der EAP Authenticator-Methode abzurufen. Nachdem der Authentifikator die Attribute verarbeitet hat, ruft er [**eapmethodauthenticatorsetattributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) auf, der aktualisierte EAP-Authentifizierungs Attribute bereitstellt, die für die EAP-Authenticator-Methode festgelegt werden. Diese Funktion gibt einen **\_ \_ \_ Antwort \_ Aktions Code für den EAP-Methoden Authentifikator** zurück, der die nachfolgende Aktion bestimmt.
-   Wenn der Aktions Code das [Antwort Ergebnis des EAP- \_ Methoden \_ Authentifikators \_ \_ ](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)ist, bedeutet dies, dass der Authentifikator die Ergebnisse der Authentifizierungs Sitzung ermittelt hat und dass diese Ergebnisse für EAPHost verfügbar sind. Der Authentifikator ruft [**eapmethodauthenticatorgetresult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) auf und ruft die Ergebnisse der Authentifizierungs Sitzung ab.
-   Danach folgt ein Aufruf von [**eapmethodauthenti| orendsession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) , um die Authentifizierungs Sitzung zu beenden.
-   Zum Schluss wird [**eapmethodauthenticatorshutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) aufgerufen, um die dll der Authenticator-Methode zu entladen.
-   Entlädt die EAP-Methoden Bibliothek.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Antwort Aktion für EAP- \_ Methoden- \_ Authentifikator \_ \_**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Supplicant-API-Rückruf Sequenz](supplicant-api-call-sequence.md)
</dt> <dt>

[Peer Method API-Rückruf Sequenz](peer-method-api-call-sequence.md)
</dt> <dt>

[EAPHost-Aufrufsequenzen](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




