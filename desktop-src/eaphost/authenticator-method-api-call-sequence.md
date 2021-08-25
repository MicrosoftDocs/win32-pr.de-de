---
title: Authenticator Methoden-API-Aufrufsequenz
description: Erfahren Sie mehr über die API-Aufrufsequenz der Authentatormethode. Sehen Sie sich eine Liste an, die die Abfolge von Aufrufen veranschaulicht, die von einem EAPHost für eine EAP-Authentatormethode ausgeführt werden.
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3864d7b08c3c5c154ef3be86d0ac14716cd8b46adb1485fc5c55e598f870a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852290"
---
# <a name="authenticator-method-api-call-sequence"></a>Authenticator Methoden-API-Aufrufsequenz

Dieses Thema enthält die spezifische Aufrufsequenz für die Authentatormethode-API. Während einer typischen EAP-Authentifizierungssitzung führt EAPHost eine Reihe von Aufrufen für eine EAP-Methode aus, die die EAPHost-Authentisierungsmethoden-APIs implementiert.

Die folgende Liste veranschaulicht die Abfolge der Aufrufe, die von EAPHost für eine EAP-Authentatormethode ausgeführt werden.

-   Der EAP-Authentator lädt zuerst die EAP-Methoden-DLL, die für die spezifische Authentifizierung verwendet wird, auf einem Netzwerkrichtlinienserver (NPS) oder einem anderen Authentifizierungsserver.
-   Ruft [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) für die Methode mit einer aufgefüllten [**EAP \_ TYPE-Struktur**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type) auf, um eine Liste von Zeigern auf Funktionen zu erhalten, die in der DLL implementiert sind. Bei nachfolgenden Funktionsaufrufen durch die Authentatormethoden (Server) wird davon ausgegangen, dass sie in der DLL implementiert werden.
-   Ruft [**EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) auf, um die EAP-Methodenbibliothek anweisen, sich mit dieser Authentisierungsmethode auf mindestens eine Authentifizierungssitzung vorzubereiten.
-   Ruft [**EapMethodAuthenticatorBeginSession auf,**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) um eine eindeutige Authentifizierungssitzung zu erstellen.
-   Wiederholt die folgenden Schritte, bis [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) angibt, dass ein Authentifizierungsergebnis verfügbar ist.
    -   Ruft [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) mit einem Zeiger auf ein Anforderungspaket auf, das an den Supplicant übergeben werden soll.
    -   Ruft [**EapMethodAuthenticatorReceivePacket auf,**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) um das vom Supplicant gesendete Antwortpaket abzurufen. Diese Funktion gibt einen **EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ ACTION-Code** zurück, der die nächste Aktion angibt, die der Authentisierungsator in der EAP-Authentifizierungssitzung ausführen muss.
    -   Wenn der Aktionscode [EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ RESPOND](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)ist, gibt dies an, dass die EAP-Methode über Attribute verfügt, die der Authentator abrufen und an die Peermethode übergeben kann. Authenticator ruft [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) auf, um die verschiedenen EAP-Authentifizierungsattribute aus der EAP-Authentisierungsmethode zu erhalten. Nachdem der Authenticator die Attribute verarbeitet hat, ruft er [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) auf, wodurch aktualisierte EAP-Authentifizierungsattribute bereitgestellt werden, die für die EAP-Authentisierungsmethode festgelegt werden. Diese Funktion gibt einen **EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ ACTION-Code** zurück, der die nachfolgende Aktion bestimmt.
-   Wenn der Aktionscode [EAP \_ METHOD \_ AUTHENTICATOR \_ RESPONSE \_ RESULT](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)ist, gibt dies an, dass der Authentator die Ergebnisse der Authentifizierungssitzung bestimmt hat und diese Ergebnisse für EAPHost verfügbar sind. Authenticator ruft [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) auf und ruft die Ergebnisse der Authentifizierungssitzung ab.
-   Darauf folgt ein Aufruf von [**EapMethodAuthenticatorEndSession,**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) um die Authentifizierungssitzung zu beenden.
-   Schließlich erfolgt ein Aufruf von [**EapMethodAuthenticatorShutdown,**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) um die Authentisierungsmethode-DLL zu entladen.
-   Entlädt die EAP-Methodenbibliothek.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_ \_ EAP-METHODENAUTHENTATOR-ANTWORTAKTION \_ \_**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[Supplicant-API-Aufrufsequenz](supplicant-api-call-sequence.md)
</dt> <dt>

[Peermethode- API-Aufrufsequenz](peer-method-api-call-sequence.md)
</dt> <dt>

[EAPHost-Aufrufsequenzen](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




