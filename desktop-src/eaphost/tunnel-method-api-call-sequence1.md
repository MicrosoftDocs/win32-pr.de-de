---
title: Tunnel Methoden-API-Aufrufsequenz
description: Erfahren Sie mehr über die API-Aufrufsequenz für Tunnel Methoden. Sehen Sie sich eine Übersicht an, und zeigen Sie zusätzliche verfügbare Ressourcen an.
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca32a889229b6cdbdb3f008ebea8b838f9b6d64fba36bc2a30c4ddd9d62ac83d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272792"
---
# <a name="tunnel-method-api-call-sequence"></a>Tunnel Methoden-API-Aufrufsequenz

In diesem Thema wird die API-Aufrufsequenz für Tunnel behandelt.

## <a name="tunnel-method-call-sequence-overview"></a>Tunnel Methodenaufrufsequenz – Übersicht

Wenn Supplicant eine Anforderung für benutzeridentitäts- und benutzerdaten abruft, tritt in der Regel der folgende API-Aufruffluss auf.

-   Der Supplicant ruft EapHostPeerProcessReceivedPacket auf EapHost auf, um das vom Authentator empfangene Paket zu verarbeiten.
-   Bei der Verarbeitung dieses Pakets bestimmt EAPHost es als IdentityRequest-Paket und ruft [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) für die Tunnelmethode auf, um die Benutzeridentität für die Authentifizierung zu erhalten.
-   Wenn die Tunnelmethode die Benutzeridentität von der inneren Methode abrufen muss, ruft sie [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) auf dem inneren EAPHost auf, der wiederum [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) für die innere Methode aufruft.

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>Benutzerinteraktion mit dem TUNNEL-Methoden-API-Aufruf Flow

In bestimmten Fällen, wenn die Identität nicht verfügbar ist oder der Benutzer zusätzliche Informationen bereitstellen muss, löst die Eap-Methode ein Benutzeroberflächendialogfeld auf dem Supplicant aus.

In solchen Fällen erfolgt die folgende Aufrufsequenz in der Regel, um Informationen direkt vom Benutzer zu erhalten.

-   Tunnel Die Eap-Methode gibt Aktionscode zum Aufrufen der Benutzeroberfläche für EapHost zurück. Supplicant ruft [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)auf, um die aktuellen Kontextinformationen der Benutzeroberfläche für das Dialogfeld "Benutzeroberfläche" zu erhalten.
-   Supplicant ruft dann [ **EapHostPeerInvokeInteractiveUI auf.**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) Diese Funktion verwendet die Kontextinformationen der Benutzeroberfläche, um eine interaktive Benutzeroberfläche zu erstellen, die verwendet wird, um Anmeldeinformationsinformationen vom Benutzer zu erhalten. Der Benutzeroberflächenprozess lädt Eappcfg.dll und erhält die Zeiger auf EapPeerInvokeInteractiveUI und EapPeerFreeMemory.
    > [!Note]  
    > Der Benutzeroberflächenprozess erfasst in der Regel die Benutzeroberfläche oder behandelt die interaktive Benutzeroberfläche und ist vom supplicant-Prozess getrennt. Das Trennen der beiden Prozesse ist keine Anforderung von EAPHost, hat aber den Vorteil, dass der Benutzeroberflächenprozess mit dem Desktop interagieren kann.

     

-   EapHost ruft [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) für die Tunnelmethode auf, um Benutzeridentitätsinformationen zu erhalten.
-   Um die Benutzeridentität von der inneren Methode zu erhalten, ruft die Tunnelmethode [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) auf dem inneren EAPHost auf.
-   Inner EAPHost ruft [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) für die innere Methode auf, um die Benutzeroberfläche der Benutzeridentität aufzugeben.
-   [**EapHostPeerSetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) stellt eine neue oder aktualisierte Benutzeroberflächenkontextinformationen für die auf EAPHost geladene EAP-Peermethode zur Verfügung, nachdem die Benutzeroberfläche ausgelöst wurde.

Im folgenden Diagramm wird die API-Aufrufsequenz für Tunnel erläutert.

![Api-Aufrufsequenz für Tunnelmethoden](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Aufrufsequenz](about-eaphost-call-sequences.md)
</dt> <dt>

[Supplicant-API-Aufrufsequenz](supplicant-api-call-sequence.md)
</dt> <dt>

[EAPHost Supplicant-API-Referenz](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




