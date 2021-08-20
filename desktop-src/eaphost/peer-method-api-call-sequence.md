---
title: Peermethode- API-Aufrufsequenz
description: Erfahren Sie mehr über die API-Aufrufsequenz der Peermethode. Sehen Sie sich eine Liste an, die die Abfolge von Aufrufen veranschaulicht, die von einem EAPHost für eine EAP-Peermethode ausgeführt werden.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647a6a558d282ff4ae3691c23600b696b79764ee68a1007ccabb445c5a1fe65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042788"
---
# <a name="peer-method-api-call-sequence"></a>Peermethode- API-Aufrufsequenz

Dieses Thema enthält die spezifische Aufrufsequenz für die Peermethode-API. Während einer typischen EAP-Authentifizierungssitzung führt EAPHost eine Reihe von Aufrufen von EAP-Methoden durch, um die EAPHost-Peermethoden-API zu implementieren.

Die folgende Liste veranschaulicht die Abfolge der Aufrufe, die von EAPHost für eine EAP-Peermethode ausgeführt werden.

-   Lädt die für die Authentifizierung verwendete EAP-Peermethode-DLL.
-   Ruft [**EapPeerGetInfo für die**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) -Methode auf, um eine Liste von Zeigern auf Funktionen zu erhalten, die in der DLL implementiert sind. Nachfolgende Funktionsaufrufe durch den EAPHost-Peer (Client) werden als in der DLL implementiert angenommen.
-   Ruft [**EapPeerInitialize auf,**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) um die EAP-Methodenbibliothek anweisen, sich mit dieser Peermethode auf mindestens eine Authentifizierungssitzung vorzubereiten.
-   Ruft [**EapPeerBeginSession auf,**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) um eine eindeutige Authentifizierungssitzung zu erstellen.
-   Ruft [**EapPeerGetIdentity auf,**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) um die Identität für die Authentifizierung zu erhalten. Wenn die Identität nicht verfügbar ist oder der Benutzer zusätzliche Informationen bereitstellen muss, ruft EAPHost [ **EapPeerGetUIContext auf.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Diese Funktion erhält die Kontextinformationen für das Dialogfeld der Benutzeroberfläche, das auf dem Supplicant ausgelöst wird. Nachdem der Benutzer die Identitätsinformationen übermittelt hat, wird die Benutzeridentität mit einem Aufruf von [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)festgelegt und durch einen Aufruf von **EapPeerGetIdentity erhalten.**
-   Wiederholt die folgenden Schritte, bis [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) angibt, dass ein Authentifizierungsergebnis verfügbar ist.
    -   Ruft [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) mit dem Zeiger eines Anforderungspakets auf, das an den Supplicant übergeben werden soll.
    -   Ruft **EapPeerGetResponsePacket auf,** um das Antwortpaket abzurufen, das an den Authentator gesendet werden soll.
    -   Wenn EAP-Attribute während der Authentifizierungssitzung abgerufen oder gesendet werden müssen, ruft EAPHost optional [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) bzw. [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) auf.
-   Wenn der Authentator einen Aktionscode sendet, der angibt, dass die Authentifizierung abgeschlossen ist, ruft EAPHost [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) auf und ruft die Ergebnisse der Authentifizierung ab.
-   Ruft [**EapPeerEndSession auf,**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) um die Authentifizierungssitzung zu beenden.
-   Ruft [**EapPeerShutdown auf,**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) um die Peermethode-DLL zu entladen.
-   Entlädt die EAP-Methodenbibliothek.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Supplicant-API-Aufrufsequenz](supplicant-api-call-sequence.md)
</dt> <dt>

[Authenticator Methoden-API-Aufrufsequenz](authenticator-method-api-call-sequence.md)
</dt> <dt>

[EAPHost-Aufrufsequenzen](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




