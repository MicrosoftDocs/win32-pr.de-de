---
title: Peer Method API-Rückruf Sequenz
description: Erfahren Sie mehr über die API-Rückruf Sequenz der Peer Methode. Sehen Sie sich eine Liste an, die die Abfolge von Aufrufen von EAPHost auf einer EAP-Peer Methode veranschaulicht.
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac9be0f6de228fd5b1ebf2d2c28320baf76e914
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102354"
---
# <a name="peer-method-api-call-sequence"></a>Peer Method API-Rückruf Sequenz

Dieses Thema enthält die spezifische Rückruf Sequenz für die API der Peer Methode. Bei einer typischen EAP-Authentifizierungs Sitzung führt EAPHost eine Reihe von Aufrufen an EAP-Methoden aus, um die EAPHost-Peer Methoden-API zu implementieren.

In der folgenden Liste wird die Abfolge von Aufrufen von EAPHost auf einer EAP-Peer Methode veranschaulicht.

-   Lädt die für die Authentifizierung verwendete EAP-Peer Methoden-dll.
-   Ruft [**eappeergetinfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) für die-Methode auf, um eine Liste von Zeigern auf Funktionen zu erhalten, die für die dll implementiert wurden. Bei nachfolgenden Funktionsaufrufen durch den EAPHost-Peer (Client) wird davon ausgegangen, dass Sie für die dll implementiert werden.
-   Ruft " [**eappeerinitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) " auf, um die EAP-Methoden Bibliothek anzuweisen, mit dieser Peer Methode mindestens eine Authentifizierungs Sitzung vorzubereiten.
-   Ruft " [**eappeerbeginsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) " auf, um eine eindeutige Authentifizierungs Sitzung einzurichten.
-   Ruft [**eappeergetidentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) auf, um die Identität zu erhalten, die für die Authentifizierung verwendet werden soll. Wenn die Identität nicht verfügbar ist oder der Benutzer zusätzliche Informationen bereitstellen muss, ruft EAPHost [ **eappeergetuicontext auf.**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) Diese Funktion Ruft die Kontextinformationen für das Benutzeroberflächen Dialogfeld ab, das für den Supplicant ausgelöst wird. Nachdem der Benutzer die Identitätsinformationen übermittelt hat, wird die Benutzeridentität mit einem Aufrufen von [**eappeersetuicontext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)festgelegt und durch einen Aufrufen von **eappeergetidentity** abgerufen.
-   Die folgenden Schritte werden wiederholt, bis [**eappeerprocessrequestpacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) anzeigt, dass ein Authentifizierungs Ergebnis verfügbar ist.
    -   Ruft [**eappeerprocessrequestpacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) mit dem Zeiger eines Anforderungs Pakets auf, das an den Supplicant übergeben werden soll.
    -   Ruft **eappeergetresponsepacket** auf, um das Antwortpaket abzurufen, das an den Authentifikator gesendet werden soll.
    -   Wenn EAP-Attribute während der Authentifizierungs Sitzung abgerufen oder gesendet werden müssen, ruft EAPHost optional [**eappeergetresponlattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) bzw. [**eappeersettresponsitzungsattribute**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) auf.
-   Wenn der Authentifikator einen Aktions Code sendet, der angibt, dass die Authentifizierung fertig ist, ruft EAPHost [**eappeergetresult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) auf und ruft die Ergebnisse der Authentifizierung ab.
-   Ruft " [**eappeerendsession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) " auf, um die Authentifizierungs Sitzung zu beenden.
-   Ruft " [**eappeershutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) " auf, um die Peer Methoden-dll zu entladen.
-   Entlädt die EAP-Methoden Bibliothek.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Supplicant-API-Rückruf Sequenz](supplicant-api-call-sequence.md)
</dt> <dt>

[Authentifizierungsmethode-API-Rückruf Sequenz](authenticator-method-api-call-sequence.md)
</dt> <dt>

[EAPHost-Aufrufsequenzen](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




