---
title: Tunnel Methode API-Rückruf Sequenz
description: Erfahren Sie mehr über die API-Rückruf Sequenz für Tunnel Methoden. Hier finden Sie eine Übersicht und weitere verfügbare Ressourcen.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316503"
---
# <a name="tunnel-method-api-call-sequence"></a>Tunnel Methode API-Rückruf Sequenz

In diesem Thema wird die API-Rückruf Sequenz für Tunnel Methoden behandelt.

## <a name="tunnel-method-call-sequence-overview"></a>Übersicht über die Tunnel Methoden-Rückruf Sequenz

Wenn Supplicant eine Anforderung für Benutzeridentität und Benutzerdaten erhält, tritt in der Regel der folgende API-Aufruffluss auf.

-   Der Supplicant ruft eaphostpeer Server processreceivedpacket auf EAPHost auf, um das vom Authentifikator empfangene Paket zu verarbeiten.
-   Bei der Verarbeitung dieses Pakets bestimmt EAPHost es als identityrequest-Paket und ruft [**eappeergetidentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) auf Tunnel Methode auf, um die für die Authentifizierung zu verwendende Benutzeridentität zu erhalten.
-   Wenn die Tunnel Methode eine Benutzeridentität aus der inneren Methode abrufen muss, ruft Sie [**eaphostpeer ergetidentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) auf inner EAPHost auf, der wiederum [**eappeergetidentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) für die innere Methode aufruft.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Benutzerinteraktion mit dem Tunnel Methoden-API-Aufruffluss

In bestimmten Fällen, wenn die Identität nicht verfügbar ist oder wenn der Benutzer zusätzliche Informationen bereitstellen muss, löst die EAP-Methode ein Benutzeroberflächen Dialogfeld für den Supplicant aus.

In solchen Fällen findet die folgende Rückruf Sequenz statt, um Informationen direkt vom Benutzer abzurufen.

-   Die EAP-Tunnel Methode gibt den Aktions Code zum Aufrufen der Benutzeroberfläche für EAPHost zurück. Supplicant ruft [**eaphostpeer ergetuicontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)auf, um die aktuellen Kontextinformationen für die Benutzeroberfläche für das Dialogfeld Benutzeroberfläche abzurufen.
-   Der Supplicant ruft dann [ **eaphosteterinvokeinteractiveui auf.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Diese Funktion verwendet die UI-Kontextinformationen, um eine interaktive Benutzeroberfläche zu verwenden, die zum erhalten von Anmelde Informationen des Benutzers verwendet wird. Der UI-Prozess lädt Eappcfg.dll und ruft die Zeiger auf "eappeerinvokeinteractiveui" und "eappeerfrememory" ab.
    > [!Note]  
    > Der UI-Prozess erfasst in der Regel die Benutzeroberfläche oder verarbeitet interaktive Benutzeroberflächen und ist vom Supplicant-Prozess getrennt. Das Trennen der beiden Prozesse ist keine Voraussetzung für EAPHost, aber dies hat den Vorteil, dass der UI-Prozess mit dem Desktop interagieren kann.

     

-   EAPHost ruft [**eappeerinvokeidentityui**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) auf Tunnel Methode auf, um Benutzer Identitätsinformationen zu erhalten.
-   Zum Abrufen der Benutzeridentität aus der inneren Methode ruft die Tunnel Methode [**eaphostpeer-invokeidentityui**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) auf dem inneren EAPHost auf.
-   Inner EAPHost ruft [**eappeerinvokeidentityui**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) auf der inneren Methode auf, um die Benutzeroberfläche für Benutzer Identitäten aufzurufen.
-   [**Eaphostpeerot-Kontext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) stellt der EAP-Peer Methode, die auf EAPHost geladen wird, nach dem Auslösung der Benutzeroberfläche neue oder aktualisierte Benutzeroberflächen-Kontextinformationen bereit.

Im folgenden Diagramm wird die API-Rückruf Sequenz für Tunnel Methoden erläutert.

![Tunnel Methoden-API-Rückruf Sequenz](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Rückruf Sequenz](about-eaphost-call-sequences.md)
</dt> <dt>

[Supplicant-API-Rückruf Sequenz](supplicant-api-call-sequence.md)
</dt> <dt>

[EAPHost-Supplicant-API-Referenz](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




